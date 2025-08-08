# 🛠 AppSec Offensive Checklist 

## 1️⃣ Recon & Mapping
- [ ] Enumerate all endpoints
  - Tools: `Burp Suite Spider`, `ffuf`, `dirsearch`
- [ ] Identify technologies
  - Tools: `wappalyzer`, `builtwith`
- [ ] Map parameters
  - GET, POST, JSON, hidden form fields
- [ ] Check CORS policy
  - Misconfigured `Access-Control-Allow-Origin`

---

## 2️⃣ Authentication & Session
- [ ] Weak password policy
- [ ] Brute-force login (with/without lockout)
- [ ] Default credentials
- [ ] Session fixation
- [ ] JWT analysis
  - Alg=none, weak secret, expired token reuse
- [ ] Cookie flags
  - `Secure`, `HttpOnly`, `SameSite`

---

## 3️⃣ Access Control
- [ ] IDOR/BOLA
- [ ] Horizontal privilege escalation
- [ ] Vertical privilege escalation
- [ ] Missing role checks in API

---

## 4️⃣ Input-based Attacks
### XSS
- [ ] Reflected
- [ ] Stored
- [ ] DOM-based
- [ ] CSP bypass
  - Inline scripts, JSONP, sandbox escapes
- Payloads:
  - `<script>alert(1)</script>`
  - `<img src=x onerror=alert(1)>`
  - `"><svg onload=alert(1)>`

### SQLi
- [ ] Union-based
- [ ] Error-based
- [ ] Boolean-based
- [ ] Time-based
- Payloads:
  - `' OR 1=1--`
  - `admin'--`
  - `' UNION SELECT null,null--`
  - `1 AND SLEEP(5)`

### SSTI
- Detect:
  - `{{7*7}}`, `${7*7}`
- Exploit:
  - Template language RCE (Jinja2, Twig, Freemarker)

### CSRF
- [ ] No CSRF token in forms
- [ ] Token predictable/reusable
- PoC HTML form to trigger state change

---

## 5️⃣ Server-side Exploits
- [ ] File upload
  - Web shell, bypass extension checks
- [ ] Path traversal
  - `../../etc/passwd`
- [ ] SSRF
  - Access internal services (`http://localhost:8080`)
  - AWS metadata service (`http://169.254.169.254/latest/meta-data/`)
- [ ] Command injection
  - `; id`
  - `&& cat /etc/passwd`
- [ ] Deserialization
  - Java, PHP, Python pickle

---

## 6️⃣ API-specific Attacks
- [ ] No auth on sensitive endpoints
- [ ] Mass assignment
- [ ] GraphQL introspection enabled
- [ ] Lack of rate limiting

---

## 7️⃣ Protocol-level Attacks
- [ ] HTTP request smuggling
- [ ] Response splitting
- [ ] WebSocket handshake manipulation

---

## 8️⃣ Post-exploitation
- [ ] Extract session cookies / tokens
- [ ] Privilege escalation via admin features
- [ ] Pivot to internal network
- [ ] Download database dumps
- [ ] Install persistent JS (stored XSS)

---

## 📦 Toolbelt
- **Proxy**: Burp Suite Pro, OWASP ZAP
- **Fuzzers**: ffuf, wfuzz
- **Wordlists**: SecLists
- **Encoders**: CyberChef
- **HTTP Clients**: curl, httpie
- **Automation**: Python `requests`, Go `http`

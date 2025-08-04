# Burper

# 🧠 BSCP 8-Week Roadmap
**Burp Suite Certified Practitioner**  
*Target: complete before the end of 2025*

---

## 📅 Week 1 – Setup & Fundamentals
**Goal: become a ninja with the Burp Suite Pro interface**

- [ ] Install Burp Suite Pro + activate trial (if not done already)
- [ ] Set up **test environment**: install [PortSwigger Web Security Academy](https://portswigger.net/web-security)
- [ ] Study:
  - Burp Repeater, Proxy, Intruder, Decoder, Comparer
  - How to use **match & replace**, macros, scope
- [ ] Recommended labs:
  - HTTP request smuggling: basics
  - Burp features walkthrough (from Academy)

---

## 📅 Week 2 – SQLi & Authentication Bypass
**Goal: break login forms and SQL queries manually**

- [ ] SQLi in query string, form, and headers
- [ ] Manual exploitation using `OR 1=1`, `' UNION SELECT`, `-- -`
- [ ] Login bypass: account enumeration, logic flaws
- [ ] Recommended labs:
  - SQL injection (UNION)
  - SQLi authentication bypass
  - SQLi blind (time-based)

---

## 📅 Week 3 – IDOR, Access Control, Path Traversal
**Goal: extract data like an admin**

- [ ] Access control (vertical, horizontal)
- [ ] IDOR: tampering with `userId`, `account=`, `filename=`
- [ ] Path traversal: `../../../../../etc/passwd`
- [ ] Recommended labs:
  - Insecure direct object references
  - Path traversal: basic, file include
  - Bypassing access control

---

## 📅 Week 4 – File Upload, File Write, Exploitation Chains
**Goal: upload shells under the radar**

- [ ] Analyze file upload mechanisms (MIME type, extension, magic bytes)
- [ ] File write via LFI + log poisoning
- [ ] Chains: upload → RCE / traversal
- [ ] Recommended labs:
  - File upload: basic, validation bypass
  - Web shell exploitation (Academy or HTB)

---

## 📅 Week 5 – XSS and Client-Side Attacks
**Goal: cause damage through the victim's browser**

- [ ] Reflected, stored, DOM-based XSS
- [ ] Bypasses using `"><script>`, `"><img onerror=...>`
- [ ] Contextual analysis: JS, HTML, attributes
- [ ] Recommended labs:
  - Reflected XSS in search / form
  - Stored XSS via comment
  - DOM XSS via client-side route

---

## 📅 Week 6 – Logic Flaws & Business Logic Attacks
**Goal: break app workflows without “classic” vulnerabilities**

- [ ] Broken workflows: discounts, transfers, coupon logic
- [ ] Tampering: `price=1`, `role=user → admin`
- [ ] Password reset flaws
- [ ] Recommended labs:
  - Logic flaw in multi-step process
  - Password reset poisoning
  - Race conditions

---

## 📅 Week 7 – Exam Simulation + Drill
**Goal: simulate exam conditions and practice under pressure**

- [ ] Simulate a 2–3 hour session with 2 vulnerabilities
- [ ] Repeat BSCP-style labs with no hints
- [ ] Use a timer + write clean PoC documentation

**Resources:**
- [BSCP Exam Guide](https://portswigger.net/certification/practitioner)
- [BSCP exam example lab](https://portswigger.net/certification/example-exam)

---

## 📅 Week 8 – Final Prep & Exam
**Goal: polish, refine, and pass**

- [ ] Review all payloads used (XSS, SQLi, Traversal)
- [ ] Refactor any written reports → improve them
- [ ] Book the exam
- [ ] Final simulation with real-time constraints

---

## 📦 Bonus: Recommended Toolkit

- **Burp Suite Pro** (with Collaborator, Extender enabled)
- `ffuf`, `dirsearch`, `httpx`, `nuclei`
- Browser with FoxyProxy
- Markdown editor for reports

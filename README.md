# Gouthaman G

**Final-Year B.Tech Cyber Security Student**
**Amrita Vishwa Vidyapeetham, Coimbatore (Class of 2027)**

---

## About Me

Final-year Cyber Security student focused on **web and API security**. I'm currently building a reverse-proxy gateway that stops GraphQL BOLA attacks, and I built a CSRF defense with working bypass demos to prove it closes the gaps it claims to. Hands-on with Burp Suite through **130+ PortSwigger Web Security Academy labs** and active bug bounty hunting.

---

## Currently Learning

* Practical Junior Penetration Tester (PJPT) – TCM Security
* Advanced GraphQL &amp; API Security Testing
* Authentication &amp; JWT attack techniques
* Bug bounty hunting on Intigriti

---

## Technical Skills

### Application Security
* OWASP Top 10 & OWASP API Security Top 10
* XSS, SQLi, CSRF, SSRF
* IDOR / BOLA, Broken Access Control
* JWT Security
* Authentication & Session Management
* Threat Modeling

### API Security
* GraphQL and REST Security Testing
* Query Depth and Batching Abuse
* Field-Level Authorization
* Schema Analysis
* Reverse-Proxy Security Controls

### Tools
* Burp Suite
* Nmap
* Wireshark
* Kali Linux

### Languages & Engineering
* Python
* JavaScript (Node.js, Express)
* Git

---

## Featured Security Projects

### Schema-Aware Zero-Trust Gateway for Preventing GraphQL BOLA *(Final-year project — in progress)*

A reverse-proxy gateway that enforces object ownership at runtime in front of an unmodified backend, so a logged-in user changing `order(id:124)` to `125` can't read another user's order.

* Normalizes incoming queries (aliases, fragments with loop detection, variables, base64-encoded IDs) so hidden object references can't slip through.
* Reads the backend schema once at startup and infers who owns each type, with no hand-written policy — unknown types are blocked by default and flagged for review.
* Checks every requested object against its real owner using the caller's own token. One bad object refuses the whole request, and every refusal returns the same "not found" message so IDs can't be guessed.
* Built a vulnerable shop API and a full attack suite to prove attacks leak data without the gateway and are blocked with it, while normal access still works.

### CSRF Protection

A session-bound, signed double-submit CSRF token (HMAC-SHA256) with expiry and timing-safe comparison, applied as reusable Express middleware.

* Second layer of Origin and Fetch Metadata (`Sec-Fetch-Site`) checks, plus session regeneration on login to stop login CSRF.
* Built a vulnerable banking-style app with 4 switchable modes: no protection, weak token, weak Referer check, and fully secure.
* Built a cross-site attacker site with auto-submitting pages, including 2 working bypass demos.

### Aegis-API — Multi-Protocol API Security Testing Framework

An automated API penetration testing framework validating REST, GraphQL, and SOAP microservices end-to-end, with protocol routing and active vulnerability probing against intentionally vulnerable targets.

### Aegis-Web — Multi-Role Access-Control Testing Platform *(public project)*

An automated security assessment platform built to detect OWASP A01:2021 (Broken Access Control) by recording authenticated sessions across roles with Playwright and running cross-role differential replays.


### Network Intrusion Prevention System (NIPS)

A real-time network defense tool inspecting raw packets with Scapy and dynamically blocking abusive IPs through Linux `iptables`.

---

## Hands-on Security Practice

Completed **130+ PortSwigger Web Security Academy labs** across 20+ categories, including full completion of path traversal, file upload, GraphQL, NoSQL injection, and API testing. Also covered SQLi, XSS, CSRF, SSRF, XXE, access control, JWT, insecure deserialization, and business logic flaws.

Also active on **Intigriti** bug bounty, hunting public programs for IDOR/BOLA, authentication, and session flaws.

Full write-ups: [github.com/Gouthaman2465](https://github.com/Gouthaman2465/)

---

## Certifications

**Certified API Security Analyst (CASA)** — APIsec University

**Practical Junior Penetration Tester (PJPT)** — TCM Security *(In Progress)*

---

## Connect

[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=firefox-browser&logoColor=white)](https://gouthaman.me)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gouthaman-g-0296b1288)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Gouthaman2465/)

---

> *"Security is not just about finding vulnerabilities — it's about understanding systems well enough to build them securely."*

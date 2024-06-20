# 🌐 OWASP Top 10: Explained Simply

The OWASP Top 10 is a globally recognized list of the most critical web application security risks. Understanding these helps developers, testers, and security engineers prioritize what really matters.

I've first-hand encountered such issues in dev environments - its more common than people think!!

Here’s a quick breakdown of the latest OWASP Top 10 (2021 version), with simplified explanations and examples:

---

### 1. **Broken Access Control**
> Users can access data or functions they shouldn't.

**Example**: A regular user modifies a URL to access an admin page like `/admin/delete-user?user=123`.

🛡️ *Fix*: Enforce proper role checks on the backend. Don’t rely on just hiding buttons or links.

---

### 2. **Cryptographic Failures**  
> Weak or missing encryption, poor key management.

**Example**: Storing passwords in plain text or using outdated hashing like MD5.

🛡️ *Fix*: Use HTTPS, strong algorithms (AES, bcrypt), and secure storage for secrets.

---

### 3. **Injection (e.g., SQL, NoSQL, OS)**  
> User input breaks your commands or queries.

**Example**: SQL Injection like `' OR '1'='1`.

🛡️ *Fix*: Use parameterized queries. Never trust raw input in commands.

---

### 4. **Insecure Design**
> The app was never secure from the start.

**Example**: A system that lets users upload files anywhere without validation.

🛡️ *Fix*: Apply threat modeling, secure-by-design principles, and proper architectural review.

---

### 5. **Security Misconfiguration**
> Default settings, unnecessary services, exposed error messages.

**Example**: Leaving an admin panel accessible with default credentials.

🛡️ *Fix*: Harden all environments. Disable what you don’t need. Keep configs consistent.

---

### 6. **Vulnerable and Outdated Components**
> Using libraries or plugins with known flaws.

**Example**: Still using a version of jQuery with a known XSS vulnerability.

🛡️ *Fix*: Keep dependencies updated. Use tools like `npm audit` or `Dependabot`.

---

### 7. **Identification and Authentication Failures**
> Broken login, session management, or password flaws.

**Example**: Brute-force login with no rate limiting.

🛡️ *Fix*: Implement MFA, lockout mechanisms, and secure session handling.

---

### 8. **Software and Data Integrity Failures**
> Untrusted code or data can be tampered with.

**Example**: Downloading a script from a 3rd-party CDN without checking its hash.

🛡️ *Fix*: Use signed updates, integrity checks, and proper CI/CD protections.

---

### 9. **Security Logging and Monitoring Failures**
> You don’t know if you’re being attacked.

**Example**: No logs for failed logins or unexpected admin actions.

🛡️ *Fix*: Log important events and monitor for anomalies. Alert on suspicious behavior.

---

### 10. **Server-Side Request Forgery (SSRF)**
> Server fetches a URL controlled by the attacker.

**Example**: App allows users to supply a URL and the backend blindly fetches it — attackers can access internal resources.

🛡️ *Fix*: Whitelist external URLs, validate input, and block internal access.

---

## 💡 Final Note

The OWASP Top 10 is not just a checklist — it's a mindset shift.  
Each item reflects a class of problems that can affect real users, real systems, and real businesses.

👉 Learn it, apply it, and build safer apps.

---

📚 Source: [OWASP Top 10 – Official Site](https://owasp.org/www-project-top-ten/)

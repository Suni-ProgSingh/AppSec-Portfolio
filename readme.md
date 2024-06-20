# 🛡️ SQL Injection: What Went Wrong & How We Fixed It

SQL Injection is one of the most common and dangerous web vulnerabilities — it allows attackers to tamper with your queries and access data they shouldn’t.

This snippet shows a simple login function written in Python (Flask) where things go wrong — and then how to fix it.

---

## 🔍 The Problem: Vulnerable Code

In the first version, we take user input directly and plug it into an SQL query using string formatting. This might look harmless at first, but it opens the door for attackers to inject malicious SQL commands.

```python
query = f"SELECT * FROM users WHERE username = '{username}' AND password = '{password}'"

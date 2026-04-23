# Elevate Labs Cyber Security Internship - Task 6
## Password Strength Evaluation and Security Best Practices

### 🎯 Objective
To evaluate how different levels of complexity and character variety affect password security and crack-time using industry-standard evaluation tools.

---

### 💻 Tool Used
- **Evaluation Tool:** PasswordMeter.com
- **Platform:** Web Browser

---

### 📊 Password Strength Analysis Summary

I analyzed four passwords with decreasing levels of complexity to observe the impact on security scores.

| Level | Complexity | Security Verdict |
| :--- | :--- | :--- |
| **Very Strong** | Mix of Alpha-Numeric + Symbols + High Length | Highly Secure |
| **Strong** | Upper/Lower Case + Numbers + Moderate Length | Secure |
| **Medium** | Simple mix of characters | Vulnerable to targeted attacks |
| **Very Weak** | Only lowercase dictionary words | Instant Crack (Dictionary Attack) |

---

### 📸 Evaluation Screenshots

#### 1. Very Strong Password
![Very Strong](screenshots/01_very_strong_password.png)
*Score: 100%. Maximum complexity achieved.*

#### 2. Strong Password
![Strong](screenshots/02_strong_password.png)
*Score: High. Good mix of characters but shorter length.*

#### 3. Medium Password
![Medium](screenshots/03_medium_password.png)
*Score: Average. Common patterns detected.*

#### 4. Very Weak Password
![Very Weak](screenshots/04_very_weak_password.png)
*Score: 0%. Failed due to dictionary words and lack of variety.*

---

### 📝 Interview Questions & Answers

**1. What makes a password strong?**
A mix of uppercase, lowercase, numbers, and symbols with a minimum length of 12-16 characters.

**2. What are common password attacks?**
Brute Force, Dictionary Attack, Phishing, and Credential Stuffing.

**3. Why is password length important?**
Length increases entropy, making it exponentially harder for automated tools to guess the combination.

**4. What is a dictionary attack?**
An automated attack that uses a list of common words and previously leaked passwords.

**5. What is multi-factor authentication (MFA)?**
A security layer requiring two or more verification methods (e.g., Password + OTP).

**6. How do password managers help?**
They generate and store unique, complex passwords, preventing password reuse.

**7. What are passphrases?**
A long string of random words that are easy for humans to remember but very hard for computers to crack.

**8. What are common mistakes in password creation?**
Using personal info, sequential numbers (1234), and reusing the same password on multiple sites.

---
**Submitted by:** Ayush Kumar Patel
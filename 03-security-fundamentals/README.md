# 🛡️ Security Fundamentals: Access Control, Authentication, Privacy, and Password Management

## Identification, Authentication, and Authorization

In the context of cybersecurity, **Identification**, **Authentication**, and **Authorization** are crucial concepts to ensure secure access to systems and data. Below is the explanation of each concept, along with both physical world and tech world scenarios for better understanding.

### 1. Identification 🆔

Identification is the process of claiming an identity. It is the first step in an access control system, where a user presents a credential (e.g., username, ID number) to prove who they are.

**💡 Example in the Physical World:**

Imagine you're going to a bank. The first thing the bank teller asks is for your **ID card**. You present your ID to **identify** yourself as a customer of the bank.

**🤖 Example in the Tech World:**

When you log into a website or an application, you are asked to provide your **username** or **email address**. This is the **identification** process where the system is trying to identify you as a user in its database. This could also be the case when you use **biometric scanners** on your phone to identify yourself by face or fingerprint.

### 2. Authentication 🔑

Authentication is the process of verifying that the identity claimed during the identification process is valid. This can involve something the user knows (password), something they have (token, smartphone), or something they are (biometric data).

**💡 Example in the Physical World:**

After presenting your **ID card** (identification), the bank teller asks you to **enter your PIN** or **provide a signature**. This is the **authentication** process where the bank ensures that you are the rightful owner of the account.

**🤖 Example in the Tech World:**

In the tech world, after providing your **username**, the system will prompt you for your **password**. This process ensures that the person trying to log in is the legitimate user. If two-factor authentication (2FA) is enabled, you may be required to enter a **one-time code** sent to your phone or email, adding an extra layer of **authentication**.

### 3. Authorization 🛂

Authorization is the process of granting or denying access to a system or resource based on the authenticated identity. It determines what actions a user can perform on the system, such as read, write, or delete data.

**💡 Example in the Physical World:**

After you are authenticated (with your **PIN** or **signature** at the bank), the bank teller will check your **account type** and grant you the appropriate access. For example, if you have a **savings account**, you might be authorized to withdraw money, but if you have a **checking account**, you might also be able to write checks. This is where the bank determines your **authorization** to perform specific actions based on your account type.

**🤖 Example in the Tech World:**

In a web application, once you’ve successfully logged in (authenticated), your account type (admin, user, guest, etc.) is checked to determine what actions you're allowed to perform. For example, a **regular user** may only be able to view data, while an **admin user** has permission to update or delete records. Access control lists (ACLs) or role-based access control (RBAC) are used to manage **authorization** in systems.

## 🛡️ Password Security

### 🔑 **Password Policy Controls**

When setting a password policy for your organization, consider the following technical controls to enhance security:

#### 1. **Password Length** 📏

- **Minimum character length** (recommended: at least **8 characters**).
- Longer passwords are more secure and harder to guess.

#### 2. **Password Complexity** 🔠

- Require different **character types**:
  - **Uppercase** and **lowercase letters**
  - **Digits**
  - **Special characters** (e.g., @, #, $, etc.)
- More character types = stronger password

#### 3. **Password Expiration** ⏳

- Force users to change passwords periodically (e.g., every **180 days**).
- Some organizations no longer enforce expiration and allow passwords to stay unless compromised.

#### 4. **Password History** 🕒

- Prevent users from **reusing old passwords**.
- Configure systems to remember previous passwords and block reuse.

#### 5. **Password Reset Process** 🔄

- Ensure a **quick and secure password change process** for users.
- Avoid weak reset mechanisms that could allow unauthorized access.

### 🔐 **Password Management Best Practices**

#### 6. **Avoid Password Reuse** 🔄

- **Discourage password reuse** across multiple sites.
- If a site is compromised, reused passwords could allow attackers to access other accounts.

#### 7. **Use Password Managers** 🧳

- **Password managers** securely store and create **unique passwords** for each site.
- Protect password managers with **biometric security** mechanisms (e.g., fingerprint or facial recognition).
- Allow users to store passwords securely without needing to memorize them.

### 📌 **Summary of Key Points**

- **Longer and more complex passwords** are harder to guess.
- **Periodic password changes** (or on suspicion of compromise) help enhance security.
- **Password managers** help manage unique passwords without the need to remember each one.
- **Avoid password reuse** to prevent attackers from exploiting compromises.

## 🔐 Multifactor Authentication (MFA)

### 🎭 **Understanding Authentication Factors**

Computer systems use different authentication techniques to verify user identities. These techniques fall into three categories:

#### 1️⃣ **Something You Know** 🧠

- A **knowledge-based factor** that relies on information the user remembers.
- Examples:
  - **Passwords** (most common)
  - **PINs (Personal Identification Numbers)**
  - **Security Questions**

#### 2️⃣ **Something You Are** 🧬

- A **biometric factor** that uses physical or behavioral characteristics.
- Examples:
  - **Fingerprint** scanning
  - **Facial recognition**
  - **Voice recognition**

#### 3️⃣ **Something You Have** 📱

- A **possession-based factor** requiring a physical device.
- Examples:
  - **Smartphones** running authentication apps
  - **Security key fobs**
  - **Smart cards**

### 🔑 **Why MFA is Important?**

Each authentication factor has vulnerabilities:

- **Passwords can be stolen** via phishing or brute-force attacks.
- **Biometric data can be spoofed** or fail under certain conditions.
- **Physical devices can be lost** or stolen.

By combining at least **two different factors**, MFA significantly improves security.

### 🛡️ **Multifactor Authentication (MFA) in Action**

- Using a **password + security key** 🔐 (Something You Know + Something You Have)
- **Fingerprint scan + PIN** 🔏 (Something You Are + Something You Know)
- **Smart card + facial recognition** 🏦 (Something You Have + Something You Are)

**🚫 Not MFA:** Combining **two knowledge-based factors** (e.g., password + security question) does not count as MFA.

### 🔄 **Single Sign-On (SSO) Explained**

**SSO (Single Sign-On)** allows users to log in once and gain access to multiple systems without repeated authentication.

- ✅ **Reduces login fatigue** for users.
- ✅ **Improves user experience** and efficiency.
- ✅ **Can be integrated with MFA** for added security.
- ❌ **If compromised, can give attackers broad access** to systems.

### 📌 **Key Takeaways**

- MFA **requires at least two different factors** (e.g., something you know & something you have).
- **Passwords + security questions = NOT MFA** (both are knowledge-based).
- **SSO simplifies authentication** but should be paired with **MFA for security**.
- When evaluating MFA on the exam, **ensure the techniques belong to separate factor categories**.

## 📝 Non-Repudiation

### 🔍 **What is Non-Repudiation?**

**Non-repudiation** ensures that an individual **cannot deny** performing a specific action. It provides **verifiable proof** that an action took place.

📌 **Key Concept:**

- **Repudiation** = Denying an action was taken.
- **Non-Repudiation** = Preventing false denials with proof.

### 🎭 **Real-World Example**

Imagine **buying a car** for **$10,000** with just a handshake. Later, the seller might claim you only agreed to pay **$5,000**, or you could deny agreeing at all.

✅ **Solution:** A **signed contract** acts as proof, preventing either party from backing out of the agreement dishonestly.

### 💻 **Tech Example: Digital Signatures**

A company sends a **confidential contract** via email. Later, the sender denies having sent it.

✅ **Solution:** A **digital signature** confirms the sender’s identity and ensures the document wasn’t altered.

### 🛡️ **Non-Repudiation Techniques**

🔏 **Digital Signatures** – Uses **encryption** to verify sender authenticity and prevent document tampering.  
🛂 **Biometric Authentication** – Fingerprints, facial recognition, or retinal scans provide undeniable proof of identity.  
📹 **Video Surveillance** – Captures **physical presence** at a location to prove access or actions.  
📄 **Audit Logs** – Records **timestamped activities** on a system to track user actions.

### 📌 **Key Takeaways**

- **Non-repudiation ensures accountability** and prevents false denials.
- **Digital signatures provide cryptographic proof** of authenticity.
- **Audit logs, biometrics, and surveillance add extra layers of proof.**
- **Non-repudiation supports legal and compliance requirements** in security policies.

## 🔒 Privacy

### 🧐 **What is Privacy?**

Privacy refers to the protection of **personal information** collected, stored, and processed by organizations. IT professionals play a key role in safeguarding privacy by:  
1️⃣ Protecting **their own private data**.  
2️⃣ Educating users about privacy risks.  
3️⃣ Assisting **privacy officers** in securing data.

### 🔍 **Types of Private Information**

📌 **Personally Identifiable Information (PII)** – Data that can be tied to a specific person (e.g., name, address, Social Security number).  
📌 **Protected Health Information (PHI)** – Healthcare records regulated under **HIPAA** (e.g., medical history, prescriptions).

### ⚖️ **Reasonable Expectation of Privacy**

Privacy is based on the legal principle of **reasonable expectation of privacy**—whether a person **expects** their information to remain private.

📖 **Examples:**

- **Public Posts (No Privacy):** Social media posts are **public** and have **no expectation of privacy**.
- **Private Messages (Some Privacy):** Emails and DMs have **some** expectation of privacy, but they can be intercepted.
- **Government/Health Records (High Privacy):** Personal data given to **tax agencies, banks, and healthcare providers** should be **strictly protected**.

### 🌍 **Real-World Example**

An employee **uses a company computer** to send a personal email, assuming it’s private. However, the employer **monitors network activity**, revealing the email.

✅ **Solution:** Employees should be informed that **company-owned systems** generally do **not** provide privacy protection.

### 💻 **Tech Example: Data Breaches**

A **hospital leaks patient records** due to a cyberattack, violating **HIPAA** and patient privacy rights.

✅ **Solution:** Implement **encryption, access controls, and regular audits** to protect sensitive information.

### 🔐 **Best Practices for Privacy Protection**

✅ **Encrypt sensitive communications** (emails, file transfers).  
✅ **Limit access to private data** (only authorized personnel).  
✅ **Educate users about privacy policies** and risks.  
✅ **Use strong authentication** to prevent unauthorized access.  
✅ **Regularly audit systems** for compliance with privacy laws.

### 📌 **Key Takeaways**

- **Privacy laws like GDPR and HIPAA** set strict rules for handling personal data.
- **Organizations must protect PII and PHI** from unauthorized access.
- **Company-owned devices and networks are not private**—employers can monitor activity.
- **Encryption and access controls** are essential for privacy protection.

### 📌 **Terms**

- **GDPR (General Data Protection Regulation):** A regulation in the European Union that mandates strict guidelines for data protection and privacy for all individuals within the EU.
- **HIPAA (Health Insurance Portability and Accountability Act):** A U.S. law that ensures the privacy and security of individuals' medical information and sets standards for electronic health transactions.

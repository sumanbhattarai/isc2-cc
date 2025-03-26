# 🎯 Cheatsheet to Success: (ISC)² CC Exam

## 🔍 What is (ISC)²?

(ISC)² (**International Information System Security Certification Consortium**) is a non-profit organization that provides cybersecurity certifications and professional development resources. It is best known for its **Certified Information Systems Security Professional (CISSP)** certification, along with other certifications like **CC, SSCP, CCSP, CSSLP, CISSP-ISSAP, CISSP-ISSEP, and CISSP-ISSMP**. (ISC)² focuses on improving cybersecurity standards and promoting ethical practices in the field.

## ⚖️ Code of Ethics Canons (Priority Order)

1️⃣ **Protect society**, the common good, necessary public trust, and confidence.  
2️⃣ **Act honorably**, honestly, justly, responsibly, and legally.  
3️⃣ **Provide diligent and competent service** to principals (clients, employers, or organizations).  
4️⃣ **Advance and protect the profession**.

## 🔐 CIA Triad: The Three Pillars of Cybersecurity

![CIA Triad](./cia.png)

**CIA stands for Confidentiality, Integrity, and Availability**, which are the three core principles of cybersecurity:

- **🔏 Confidentiality** – Ensures that data is accessible only to authorized users and protects it from unauthorized access.
- **🛡️ Integrity** – Ensures the accuracy and reliability of data by preventing unauthorized modifications.
- **⚡ Availability** – Ensures that systems, networks, and data are accessible and operational when needed.

## 🚨 Confidentiality Threats & Solutions

- **🔍 Snooping** – Unauthorized access to someone’s data, files, or communications, often by an insider or hacker looking for sensitive information.  
  💡 **Example:** An employee accesses confidential client data without permission to sell it to a competitor.  
  ✅ **Solution:** **Use encryption** for data at rest and in transit to prevent unauthorized access. Also, clean your work desk before leaving.

- **🗑️ Dumpster Diving** – Searching through trash or discarded materials to find confidential information like passwords, financial records, or company data.  
  💡 **Example:** A hacker finds old bank statements and password lists in the company's dumpster and uses them for identity theft.  
  ✅ **Solution:** **Shred documents** before disposal and implement secure disposal methods for sensitive materials.

- **🎧 Eavesdropping** – Secretly listening to private conversations, either in-person or through electronic means, to gather sensitive information.  
  💡 **Example:** A cybercriminal intercepts a conversation over an unsecured Wi-Fi network to steal login credentials.  
  ✅ **Solution:** Use **end-to-end encryption** for communications and avoid discussing sensitive information in public or over unsecured channels.

- **📞 Wiretapping** – Intercepting and monitoring telephone or network communications to capture conversations or data, often illegally.  
  💡 **Example:** An attacker listens to phone conversations between a CEO and an investor to steal confidential business plans.  
  ✅ **Solution:** Implement **network encryption (e.g., VPN, TLS)** and regularly monitor for unauthorized network taps.

- **🎭 Social Engineering** – Manipulating people into revealing confidential information or performing actions that compromise security, often through deception or psychological tactics.  
  💡 **Example:** A hacker impersonates an IT technician and tricks an employee into revealing their password via email.  
  ✅ **Solution:** Conduct **security awareness training** to educate employees on recognizing and resisting manipulation tactics.

## 🔐 Integrity Concerns & Solutions

- **❌ Unauthorized Modification** – Illegitimate changes to data that compromise its accuracy and reliability.  
  💡 **Example:** A hacker alters transaction records in a bank's database to steal funds while disguising the fraudulent activity.  
  ✅ **Solution:** Implement **access controls**, use **hashing (SHA-256, MD5)**, and enable **version control** to track changes.

- **🕵️‍♂️ Impersonation** – An attacker pretends to be a legitimate user to manipulate or alter data.  
  💡 **Example:** An attacker steals login credentials to impersonate a system administrator and changes user permissions to gain unauthorized access.  
  ✅ **Solution:** Use **multi-factor authentication (MFA)**, enforce **strong password policies**, and monitor for suspicious login attempts.

- **🖥️ Man-in-the-Middle (MITM) Attack** – An attacker intercepts and potentially alters communication between two parties.  
  💡 **Example:** A hacker intercepts login credentials between a user and a website by exploiting an unsecured Wi-Fi network.  
  ✅ **Solution:** Use **end-to-end encryption (TLS, HTTPS)**, enforce **certificate pinning**, and implement **secure network protocols**.

- **🔁 Replay Attack** – An attacker captures and reuses valid data transmission (e.g., login requests) to gain unauthorized access.  
  💡 **Example:** An attacker captures a user’s login session and replays it later to access the user’s account without their permission.  
  ✅ **Solution:** Implement **timestamps**, use **one-time tokens (OTPs)**, and enforce **session expiration policies**.

## 🚨 Availability Threats & Solutions

- **💻 DOS (Denial of Service)** – An attack that prevents legitimate users from accessing a system or service by overwhelming it with traffic.  
  💡 **Example:** A DDoS attack floods a website with traffic, causing it to crash and making it unavailable for users.  
  ✅ **Solution:** Use **rate limiting**, implement **firewalls**, and set up **intrusion detection systems (IDS)** to detect and block malicious traffic.

- **🖥️ Hardware Failure** – Physical failure of a device or component, such as a hard drive, server, or network equipment, causing downtime.  
  💡 **Example:** A hard drive failure causes a database to become inaccessible, disrupting services.  
  ✅ **Solution:** Implement **regular backups**, use **redundant hardware** (e.g., RAID configurations), and ensure **disaster recovery** plans are in place.

- **⚡ Power Outage** – Loss of electrical power, leading to system shutdowns and service interruptions.  
  💡 **Example:** A power outage at a data center causes servers to go offline, making critical systems unavailable.  
  ✅ **Solution:** Use **uninterruptible power supplies (UPS)**, set up **backup generators**, and have **regular power failure drills** for contingency planning.

- **💥 Destruction** – Physical damage to infrastructure, such as fire, floods, or earthquakes, leading to data loss or service disruption.  
  💡 **Example:** A fire at a data center destroys servers, causing a total loss of critical data and services.  
  ✅ **Solution:** Implement **offsite backups**, use **cloud storage**, and ensure **disaster recovery plans** are in place to minimize impact.

- **🌐 Service Outages** – Interruption of service due to issues with the service provider or internal system failures.  
  💡 **Example:** A cloud service provider experiences a network failure, causing users to lose access to critical applications.  
  ✅ **Solution:** Use **multi-cloud providers**, implement **failover systems**, and ensure **service level agreements (SLAs)** are in place with providers.

# Identification, Authentication, and Authorization

In the context of cybersecurity, **Identification**, **Authentication**, and **Authorization** are crucial concepts to ensure secure access to systems and data. Below is the explanation of each concept, along with both physical world and tech world scenarios for better understanding.

## 1. Identification 🆔

Identification is the process of claiming an identity. It is the first step in an access control system, where a user presents a credential (e.g., username, ID number) to prove who they are.

### 💡 Example in the Physical World:

Imagine you're going to a bank. The first thing the bank teller asks is for your **ID card**. You present your ID to **identify** yourself as a customer of the bank.

### 🤖 Example in the Tech World:

When you log into a website or an application, you are asked to provide your **username** or **email address**. This is the **identification** process where the system is trying to identify you as a user in its database. This could also be the case when you use **biometric scanners** on your phone to identify yourself by face or fingerprint.

---

## 2. Authentication 🔑

Authentication is the process of verifying that the identity claimed during the identification process is valid. This can involve something the user knows (password), something they have (token, smartphone), or something they are (biometric data).

### 💡 Example in the Physical World:

After presenting your **ID card** (identification), the bank teller asks you to **enter your PIN** or **provide a signature**. This is the **authentication** process where the bank ensures that you are the rightful owner of the account.

### 🤖 Example in the Tech World:

In the tech world, after providing your **username**, the system will prompt you for your **password**. This process ensures that the person trying to log in is the legitimate user. If two-factor authentication (2FA) is enabled, you may be required to enter a **one-time code** sent to your phone or email, adding an extra layer of **authentication**.

---

## 3. Authorization 🛂

Authorization is the process of granting or denying access to a system or resource based on the authenticated identity. It determines what actions a user can perform on the system, such as read, write, or delete data.

### 💡 Example in the Physical World:

After you are authenticated (with your **PIN** or **signature** at the bank), the bank teller will check your **account type** and grant you the appropriate access. For example, if you have a **savings account**, you might be authorized to withdraw money, but if you have a **checking account**, you might also be able to write checks. This is where the bank determines your **authorization** to perform specific actions based on your account type.

### 🤖 Example in the Tech World:

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

---

### 🔐 **Password Management Best Practices**

#### 6. **Avoid Password Reuse** 🔄

- **Discourage password reuse** across multiple sites.
- If a site is compromised, reused passwords could allow attackers to access other accounts.

#### 7. **Use Password Managers** 🧳

- **Password managers** securely store and create **unique passwords** for each site.
- Protect password managers with **biometric security** mechanisms (e.g., fingerprint or facial recognition).
- Allow users to store passwords securely without needing to memorize them.

---

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

---

### 🔑 **Why MFA is Important?**

Each authentication factor has vulnerabilities:

- **Passwords can be stolen** via phishing or brute-force attacks.
- **Biometric data can be spoofed** or fail under certain conditions.
- **Physical devices can be lost** or stolen.

By combining at least **two different factors**, MFA significantly improves security.

---

### 🛡️ **Multifactor Authentication (MFA) in Action**

- Using a **password + security key** 🔐 (Something You Know + Something You Have)
- **Fingerprint scan + PIN** 🔏 (Something You Are + Something You Know)
- **Smart card + facial recognition** 🏦 (Something You Have + Something You Are)

**🚫 Not MFA:** Combining **two knowledge-based factors** (e.g., password + security question) does not count as MFA.

---

### 🔄 **Single Sign-On (SSO) Explained**

**SSO (Single Sign-On)** allows users to log in once and gain access to multiple systems without repeated authentication.

- ✅ **Reduces login fatigue** for users.
- ✅ **Improves user experience** and efficiency.
- ✅ **Can be integrated with MFA** for added security.
- ❌ **If compromised, can give attackers broad access** to systems.

---

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

---

### 🎭 **Real-World Example**

Imagine **buying a car** for **$10,000** with just a handshake. Later, the seller might claim you only agreed to pay **$5,000**, or you could deny agreeing at all.

✅ **Solution:** A **signed contract** acts as proof, preventing either party from backing out of the agreement dishonestly.

---

### 💻 **Tech Example: Digital Signatures**

A company sends a **confidential contract** via email. Later, the sender denies having sent it.

✅ **Solution:** A **digital signature** confirms the sender’s identity and ensures the document wasn’t altered.

---

### 🛡️ **Non-Repudiation Techniques**

🔏 **Digital Signatures** – Uses **encryption** to verify sender authenticity and prevent document tampering.  
🛂 **Biometric Authentication** – Fingerprints, facial recognition, or retinal scans provide undeniable proof of identity.  
📹 **Video Surveillance** – Captures **physical presence** at a location to prove access or actions.  
📄 **Audit Logs** – Records **timestamped activities** on a system to track user actions.

---

### 📌 **Key Takeaways**

- **Non-repudiation ensures accountability** and prevents false denials.
- **Digital signatures provide cryptographic proof** of authenticity.
- **Audit logs, biometrics, and surveillance add extra layers of proof.**
- **Non-repudiation supports legal and compliance requirements** in security policies.

---

✨ **Stay vigilant, stay secure, and ace your (ISC)² CC Exam!** 🚀

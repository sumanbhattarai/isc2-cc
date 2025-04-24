# 🔐 Data Security

## 🔐 Understanding Encryption

Encryption is a core security control that protects **confidentiality** by transforming readable data into an unreadable format using mathematical algorithms and secret keys.

### 📜 Plain Text vs Ciphertext

- **Plain Text**: Original readable data.
- **Encryption Process**: Applies an **algorithm** + **encryption key** to the plain text.
- **Ciphertext**: The result—an unreadable, scrambled version of the data.

To **decrypt** the ciphertext, an authorized user must have:

- The **decryption algorithm**
- The **decryption key**

If the **key** is unknown, the data remains protected and inaccessible.

### 🧱 Key Components

- **Encryption Algorithm**: Mathematical formula used to scramble data.
- **Encryption Key**: Secret value (like a password) required to encrypt or decrypt.

### 📂 Data at Rest

Encryption protects **stored data**, such as:

- Individual files
- Full disks (e.g. BitLocker, FileVault)
- Mobile device contents

Even if a file is stolen, the data stays safe unless the attacker has the key.

### 🌐 Data in Transit

Encryption protects **moving data** across networks, including:

- **HTTPS** (vs HTTP) encrypts web traffic
- **VPNs** secure entire connections
- **Encrypted emails** prevent message interception
- **Mobile app communication** to servers

### ✅ Summary for Exam

- Encryption transforms **plain text → ciphertext**
- Used to protect:
  - **Data at rest** (stored files, disks, devices)
  - **Data in transit** (network communications)
- Decryption requires the **correct key**

## 🔐 Symmetric vs. Asymmetric Cryptography

Cryptographic algorithms fall into two major categories based on how they handle encryption and decryption keys: **symmetric** and **asymmetric**.

### 🔁 Symmetric Cryptography (Shared Secret)

- **Same key** used for both encryption and decryption.
- Also called **shared secret encryption**.
- Best for **speed** and **efficiency**, often used for bulk data encryption.

#### ✅ Example

If Alice encrypts a message using the key `apple`, Bob must use the same key `apple` to decrypt it.

#### 🔐 Challenge

Key distribution is difficult:

- For **N** users, you need `N(N-1)/2` unique keys for private communication.
  - 2 users → 1 key
  - 3 users → 3 keys
  - 10 users → 45 keys

#### 🔑 Common Algorithm

- **AES (Advanced Encryption Standard)** – widely used symmetric encryption algorithm

---

### 🔁 Asymmetric Cryptography (Public Key)

- **Two different keys**: one for encryption and one for decryption
- Also called **public key encryption**
- Uses a **key pair**:
  - **Public key**: freely shared
  - **Private key**: kept secret

#### ✅ How it works

- Alice wants to send Bob a private message.
- She encrypts it using **Bob’s public key**.
- Only **Bob’s private key** (from the same key pair) can decrypt it.

> ❗ Important: The keys must be from the **same pair** for encryption/decryption to work.

#### 🔑 Common Algorithm

- **RSA (Rivest-Shamir-Adleman)** – most common asymmetric encryption algorithm

---

### 🧠 Exam Tips

- **Symmetric = One key** (AES is the example)
- **Asymmetric = Key pair** (RSA is the example)
- If a question asks which key to use for **confidentiality**, encrypt with the **recipient’s public key**.

## 🔐 Hash Functions

Hash functions are critical to cryptographic systems, especially for digital signatures and certificates.

### 💡 What Is a Hash Function?

A **hash function** is a **one-way function** that transforms **variable-length input** into a **fixed-length, unique output** known as a **hash value** or **message digest**.

### 🔍 Key Characteristics

#### ➤ One-Way

- Irreversible: You cannot determine the original input from a hash value.

#### ➤ Fixed-Length Output

- No matter the size of the input (one word or a book), the output is always the same fixed length depending on the algorithm.

#### ➤ Unique Output (Collision Resistance)

- It should be computationally infeasible to find two different inputs that produce the same hash output.

### 🚫 How Hash Functions Can Fail

1. **Reversibility** – If a hash can be reversed, it's insecure.
2. **Collision Attacks** – If two different inputs produce the same hash, it breaks integrity protections.

### 🧮 Common Hash Functions

#### 🔹 MD5

- **Length:** 128-bit
- **Status:** ❌ Not secure
- **Notes:** Known collisions, deprecated in secure environments.

#### 🔹 SHA-1

- **Length:** 160-bit
- **Status:** ❌ Not secure
- **Notes:** Replaced by SHA-2 due to vulnerabilities.

#### 🔹 SHA-2 Family

- **Lengths:** 224, 256, 384, 512 bits
- **Status:** ✅ Still widely used
- **Notes:** Theoretical risks due to similarities with SHA-1

#### 🔹 SHA-3 (Keccak)

- **Customizable output length**
- **Status:** ✅ Secure
- **Notes:** Based on different math than SHA-1 and SHA-2

#### 🔹 RIPEMD

- **Lengths:** 128, 160, 256, 320 bits
- **Status:**
  - 128-bit: ❌ Not secure
  - 160-bit: ✅ Still used (e.g., in Bitcoin)

### 🔒 HMAC: Hash-Based Message Authentication Code

- Combines a **symmetric key** with a hash to ensure both:
  - **Authentication**
  - **Message Integrity**

```txt
Sender: message + secret key → HMAC
Receiver: same process → compare HMACs
```

### 🧪 Hash Behavior Example

Even a tiny change in the input text causes a **completely different hash**:

- "This is a message" → `a1b2c3...`
- "This is a message." → `d4e5f6...`

You can't tell the size or nature of the change by comparing hash values.

### 🛡️ Uses of Hashes

- Digital signatures
- Digital certificates
- File integrity checks
- Password hashing
- Blockchain transactions

## 🔐 The Data Lifecycle

The **data lifecycle** represents the journey that data takes within an organization, from initial creation to final destruction. While not every piece of data passes through every stage, this model provides a helpful framework for understanding data management and protection.

### 🟢 Create

- Data is **generated or modified**.
- Can happen on-premises or in the cloud.
- Examples: entering data into a form, capturing sensor data, updating a record.

### 💾 Store

- Data is placed into **storage systems**.
- Includes databases, file systems, cloud storage.
- Key consideration: **data at rest** security.

### 🖥️ Use

- Users or systems **access, read, and process** the data.
- Most vulnerable to **unauthorized access**.
- Requires access controls and monitoring.

### 🔗 Share

- Data is **shared** with other users, systems, or third parties.
- Methods include links, shared folders, API access.
- Involves **data in transit** security (e.g., encryption like HTTPS).

### 🗄️ Archive

- Data is **moved to long-term storage**.
- Not actively used, but can be restored.
- Common in regulatory compliance and historical records.

### 🔥 Destroy

- Data is **securely disposed of** when no longer needed.
- Prevents reconstruction of sensitive information.

### 🧨 Data Destruction Techniques (NIST SP 800-88)

| Technique   | Description                                                           | Reusability |
| ----------- | --------------------------------------------------------------------- | ----------- |
| **Clear**   | Overwrites data using basic write commands. Good for casual reuse.    | ✅ Yes      |
| **Purge**   | Stronger than clear. Uses cryptographic wiping, degaussing, etc.      | ✅ Yes      |
| **Destroy** | Physically destroys the media (shred, incinerate, melt). Most secure. | ❌ No       |

> 🧾 For paper records:

- **Shredding**: Use a crosscut shredder.
- **Pulping**: Breaks paper into pulp using chemicals.
- **Incineration**: Burns paper (less eco-friendly).

### 🛠️ Outsourced Options

- Third-party **data destruction services** are available.
- Must ensure they follow compliant, verifiable sanitization processes.

### ⚠️ Important Notes

- Data may **skip stages** (e.g., created and used in memory, then discarded).
- Not all data reaches **archive** or **destroy** stages.
- Still, this model helps ensure comprehensive **data governance** and **security planning**.

## 🗂️ Data Classification

Data classification is a critical practice that helps organizations **identify, manage, and secure data** based on its sensitivity and importance.

### 🎯 Purpose

- Helps determine appropriate **storage, handling, and access** controls.
- Influences **data security policies**, such as encryption and disposal requirements.

### 🧩 Common Classification Levels

#### Military Example:

- **Top Secret**
- **Secret**
- **Confidential**
- **Unclassified**

#### Business Example:

- **Highly Sensitive** – e.g., trade secrets, PII, financial data
- **Sensitive** – e.g., internal reports
- **Internal** – e.g., employee communications
- **Public** – e.g., marketing materials

> 📌 **Tip**: Classifications are based on both **sensitivity** and **criticality** of the information.

### 🏷️ Labeling Requirements

- Classified information must be **clearly labeled**.
- Ensures users handle data properly.
- Labels can be physical (printed) or digital (metadata or headers).

### 📦 Regulated Data Types

| Type                                          | Description                                                    |
| --------------------------------------------- | -------------------------------------------------------------- |
| **PII** (Personally Identifiable Information) | Data that can identify an individual (e.g., name, SSN, email). |
| **PHI** (Protected Health Information)        | Health records protected under HIPAA.                          |
| **PCI** (Payment Card Information)            | Credit/debit card data protected under PCI-DSS.                |

### 🧹 Secure Disposal Practices

- **Important**: Simply deleting files ≠ secure deletion.
- Risks of **data remnants**: old data recoverable unless securely wiped.

#### Wiping Techniques:

- Use **secure erase tools** to overwrite data.
- Apply NIST-recommended sanitization methods.
- Physical destruction when needed (e.g., shredding, degaussing).

> 🔐 Proper classification and labeling ensure that sensitive information is always treated with the care it requires—whether it's being stored, shared, or destroyed.

## 📝 Logging and Monitoring

Logging and monitoring are essential tools for **incident response, auditing, and threat detection**. When configured properly, logs can provide critical insights into what happened, when, and who was involved.

### 🎯 Goals of Logging

- **Accountability**: Identify _who_ performed an action (e.g. user, IP, location).
- **Traceability**: Link related events across systems and time.
- **Auditability**: Maintain reliable records for investigations and compliance.

### 🤖 The Role of SIEM

**Security Information and Event Management (SIEM)** systems help organizations collect, store, and analyze log data from various sources.

#### SIEM Capabilities

1. **Centralized Log Collection**

   - Aggregates logs from:
     - Operating systems
     - Firewalls
     - Applications
     - Network devices
   - Ensures logs are **secure**, tamper-proof, and accessible.

2. **Log Correlation**
   - Uses AI and rule-based engines to **detect patterns** of malicious activity.
   - Helps identify **security incidents** that may be missed when data is siloed.

### 🧩 Example: Putting Puzzle Pieces Together

| System     | Observation                     |
| ---------- | ------------------------------- |
| IDS        | Detects attack signature        |
| Firewall   | Notes suspicious connection     |
| Web Server | Logs possible SQL injection     |
| DB Server  | Flags unusual data access       |
| Router     | Logs outbound data exfiltration |

➡️ **SIEM** connects the dots and flags a **coordinated attack**.

### 🔄 Summary

- Logging provides **visibility**, but sheer volume requires **automated tools**.
- SIEMs offer **real-time analysis** and **incident detection** by unifying logs.
- Effective monitoring enhances your organization's **security posture** and **response readiness**.

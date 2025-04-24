# 🖥️ Logical Access Control

## 🔐 Account and Privilege Management

One of the **key responsibilities** of information security professionals is **managing user accounts and privileges** to **prevent fraud and unauthorized access**.

### 🔄 **Job Rotation & Mandatory Vacations**

✔ **Job Rotation** – Employees are periodically **moved between roles**, reducing fraud risk.  
✔ **Mandatory Vacation** – Key staff **must take consecutive days off**, preventing continuous access.  
✔ **Security Benefit** – Fraud is harder to sustain when **someone else reviews the work**.

📌 **Bonus Perk?** You get to **disconnect from work in the name of security!** 😎

### 🏷 **Account Naming & Standardization**

🔹 Organizations use **consistent naming conventions** for **user accounts**, making it easy to **identify** and manage accounts.  
🔹 Example: `FirstInitial + LastName` (e.g., `mchapple`). If duplicated, add a number (e.g., `mchapple2`).

### 🔄 **Account Lifecycle Management**

**Security professionals** must ensure proper account handling **from creation to deletion**:

1️⃣ **Provisioning** – **Grant new users** access based on role.  
2️⃣ **Modification** – Adjust access **when roles change**.  
3️⃣ **Review** – Conduct **periodic access audits** (re-certification).  
4️⃣ **Deprovisioning** – **Remove access immediately** upon termination.

📌 **Key Takeaway**: Proper **account and privilege management** ensures **only authorized users have access** and prevents **insider threats**!

## 🔐 Account Monitoring

Security administrators must **monitor user accounts** to **detect unauthorized access and privilege misuses**.

### ⚠️ **Privilege Creep & Inaccurate Permissions**

✔ **Privilege Creep** – Users **accumulate unnecessary permissions** over time when switching roles.  
✔ **Regular Account Audits** – Admins should **review user access** with managers and **revoke unnecessary privileges**.  
✔ **Formal Attestation** – Auditors verify that **managers have approved all access permissions**.

### 🛡 **Unauthorized Access & Anomaly Detection**

🔹 **Continuous Monitoring** – Detects suspicious activity based on user behavior.  
🔹 **Risky Logins** – Unusual login patterns **trigger alerts** (e.g., logins from different continents at the same time).  
🔹 **Impossible Travel Time** – **Two logins from distant locations** in an unrealistically short time.  
🔹 **Network Location Changes** – A user **switching from HR to a guest network** unexpectedly.  
🔹 **Odd Login Times** – Employees **accessing systems at unusual hours** (e.g., a mail clerk logging in at 2 AM).  
🔹 **Unusual File Access** – Sudden access to **restricted files** or **large data downloads** may indicate a breach.

### 🌍 **Geotagging & Geofencing**

📍 **Geotagging** – Logs **geographic location** for each login attempt.  
🛑 **Geofencing** – Defines **virtual boundaries**, triggering alerts when a device **leaves a permitted area**.

📌 **Key Takeaway**: Continuous monitoring **prevents unauthorized access** and ensures users have **only the permissions they need**!

## 🔐 Provisioning and Deprovisioning

Account administrators manage **user onboarding and offboarding** to control system access securely.

### ✅ **Provisioning (Onboarding New Users)**

✔ **Create Authentication Credentials** – Generate usernames, passwords, and multi-factor authentication (MFA) settings.  
✔ **Assign Authorizations** – Grant access based on **job role** and **least privilege principle**.  
✔ **Automate Workflows** – Ensure **consistent** and **efficient** account creation.

### ❌ **Deprovisioning (Offboarding Users)**

🛑 **Immediate Account Removal** – Prevents **former employees from accessing systems** after departure.  
⚡ **Automated Revocation** – Ensures accounts **expire** at the right time, reducing manual errors.

#### 🔄 **Planned vs. Emergency Termination**

| **Scenario**                 | **Action**                                               |
| ---------------------------- | -------------------------------------------------------- |
| 📅 **Planned Departure**     | Auto-expire account on the last working day.             |
| 🚨 **Emergency Termination** | Disable account **immediately** in coordination with HR. |

### 🔄 **Best Practices in Windows (Active Directory)**

✔ **Disable First, Delete Later** – Temporarily suspend accounts before **permanent removal**.  
✔ **Schedule Account Expiration** – Set automatic expiration for **retiring employees**.  
✔ **Monitor Disabled Accounts** – Ensure they’re eventually removed to **free up resources**.

📌 **Key Takeaway**: Timely **provisioning and deprovisioning** strengthens security by preventing **unauthorized access** and ensuring **only active employees have system privileges**. 🚀

## 🔐 Authorization

Authorization is the **final step** in the access control process, determining what resources a user can access **after authentication**.

### 🔑 **Principle of Least Privilege (PoLP)**

🚨 **Users should only have the minimum permissions necessary** to perform their job duties.

✔ **Limits Insider Threats** – Prevents employees from **causing major damage** if they turn malicious.  
✔ **Reduces Attack Surface** – Minimizes an **attacker's access** if they compromise a non-admin account.

### 🔄 **Types of Access Control Systems**

| **Model**                                 | **Description**                                                                    | **Use Case**                                |
| ----------------------------------------- | ---------------------------------------------------------------------------------- | ------------------------------------------- |
| 🔒 **Mandatory Access Control (MAC)**     | **Most strict**; OS enforces permissions, users **cannot modify** access settings. | Military, Government, Highly Secure Systems |
| 📂 **Discretionary Access Control (DAC)** | **Flexible**; users **can assign** access rights to others.                        | Corporate IT, File Sharing                  |
| 🏢 **Role-Based Access Control (RBAC)**   | **Permissions assigned to roles, not individuals**.                                | Enterprises, Large Organizations            |

### ⚖ **Balancing Security & Business Needs**

✔ **Too Strict?** Users struggle to complete tasks, affecting productivity.  
✔ **Too Loose?** Risk of **data breaches** and **unauthorized access**.

📌 **Best Practice**: Implement **RBAC** with **Least Privilege** to maintain **security and efficiency**. 🚀

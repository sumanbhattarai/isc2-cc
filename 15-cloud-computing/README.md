# ☁️ Cloud Computing

## ☁️ What Is the Cloud?

Cloud computing has revolutionized IT by **delivering computing services over a network**, typically the internet. Let’s break it down clearly.

### 🧠 Simple Definition

> Cloud computing is **any service that delivers computing resources to a remote customer over a network**.

- Example 1: Checking your Gmail — Google runs it in the cloud.
- Example 2: Launching a server in AWS — it's a virtual server running in Amazon’s data center.
- Example 3: Automating emails in Salesforce — your code runs in their cloud infrastructure.

You don’t have to manage the hardware or worry about the infrastructure — **the complexity is abstracted away**.

### 📜 NIST Formal Definition

> _"Cloud computing is a model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources... that can be rapidly provisioned and released with minimal management effort or service provider interaction."_ — **NIST SP 800-145**

### 🔍 Let’s Unpack That

- **Ubiquitous & Convenient**
  - Cloud services are available from anywhere with internet access.
- **On-Demand**

  - Spin up or shut down resources whenever needed (self-service model).

- **Network Access**

  - Usually via the internet, though **private clouds** exist too.

- **Shared Resources**

  - Computing power is pooled and shared among users — leading to better efficiency and scalability.

- **Configurable & Scalable**

  - You can tailor services to your exact needs (e.g. more RAM, storage, etc.) and scale up or down quickly.

- **Minimal Management Effort**
  - No need to call tech support or rack a server — it’s mostly automated.

### 💡 Why It Matters

- Reduces costs
- Increases agility
- Scales with your business
- Requires less IT overhead

Cloud computing isn’t a single technology — it’s a delivery model that encompasses **storage, servers, networks, software, and more**.

## ☁️ Cloud Service Categories

Cloud computing is commonly divided into three **service models**, each offering different levels of control and responsibility:

### 💻 Software as a Service (SaaS)

In **SaaS**, the provider delivers a **fully functional application** to end users over the internet.

- **Users don’t manage or control** the underlying infrastructure.
- **Accessed via web browsers**, with minimal setup or configuration.

**Examples:**

- Google Workspace (Gmail, Docs)
- Microsoft Office 365
- Dropbox, Box
- Salesforce
- Online expense or payroll platforms

**Customer Responsibility:** Manage **data** and **user access**.

### 🖥 Infrastructure as a Service (IaaS)

With **IaaS**, providers offer **fundamental computing resources** like virtual machines, storage, and networking.

- Customers configure and manage their own **OS, applications, and data**.
- Offers the most flexibility and control.

**Examples:**

- Amazon Web Services (AWS)
- Microsoft Azure
- Google Compute Engine

**Customer Responsibility:** OS, patches, apps, data, firewall rules, etc.

### 🧱 Platform as a Service (PaaS)

In **PaaS**, the cloud vendor provides a **runtime environment** for applications.

- Customers run their own **code** without managing the underlying servers or OS.
- Simplifies deployment and scalability for developers.

**Examples:**

- Google App Engine
- Microsoft Azure App Service
- Heroku

**Customer Responsibility:** Code and data; vendor handles platform and OS.

---

### 🔐 Shared Responsibility Model

Security responsibilities differ based on the service category:

| Responsibility Area      | SaaS        | PaaS        | IaaS        |
| ------------------------ | ----------- | ----------- | ----------- |
| Application Code         | ❌ Vendor   | ✅ Customer | ✅ Customer |
| Data                     | ✅ Customer | ✅ Customer | ✅ Customer |
| OS & Middleware          | ❌ Vendor   | ❌ Vendor   | ✅ Customer |
| Network & Infrastructure | ❌ Vendor   | ❌ Vendor   | ❌ Vendor   |

Understanding **who is responsible for what** is essential for protecting cloud-based systems.

## ☁️ Cloud Deployment Models

Cloud computing offers **five deployment models**, each suited for different business needs and risk profiles. Here’s a breakdown of each:

### 🏢 Private Cloud

- **Used exclusively** by one organization.
- May be **hosted on-premises** or by a third party.
- Offers **greater control, security, and customization**.
- Ideal for organizations with **sensitive data** or regulatory requirements.

**Example:** A healthcare company running its own virtualized servers in a private data center.

### 🌐 Public Cloud

- Resources are **owned and operated by third-party providers** (e.g., AWS, Azure, Google Cloud).
- Uses a **multi-tenancy** model – customers share infrastructure.
- Highly **scalable**, **cost-effective**, and **easy to deploy**.

**Example:** A startup using Google Cloud for app hosting and storage.

### 🔄 Hybrid Cloud

- Combines **private and public clouds**.
- Allows data and applications to **move between environments**.
- Often used for **balancing performance, cost, and security**.

**Example:** A business runs customer-facing apps in the public cloud but keeps sensitive data in a private cloud.

### 🌍 Multi-Cloud

- Uses **services from multiple public cloud providers**.
- Helps **avoid vendor lock-in** and improves **resilience**.
- Increases **complexity** due to different APIs, tools, and security models.

**Example:** A company uses AWS for compute power and Azure for AI services.

### 👥 Community Cloud

- Shared by **organizations with common goals or compliance needs**.
- Offers **shared infrastructure**, typically governed collectively.
- Less common, but useful in sectors like **education or government**.

**Example:** Multiple universities collaborating on a shared research cloud.

### 🛡 Shared Responsibility Model Reminder

In **public and hybrid/multi-cloud** scenarios, remember:

- **Cloud provider**: Physical security, infrastructure, hypervisor, etc.
- **Customer**: Data, access control, and application security.

Each deployment model fits different risk tolerances, budgets, and operational needs. No model is **inherently better**—it’s about **choosing what works best** for your organization's goals and compliance landscape.

## 🔐 Managed Security Service Providers

Organizations often outsource technology operations to **Managed Service Providers (MSPs)**, and when those services are security-focused, they’re called **Managed Security Service Providers (MSSPs)**.

### What is an MSSP?

- MSSPs are **third-party vendors** that deliver **security services** to client organizations.
- Services range from **comprehensive security management** to **specific security functions**.
- MSSPs must be **monitored closely** to ensure they meet security objectives and uphold trust.

### Common MSSP Services

#### 🔎 Security Monitoring

- **Log analysis**, **SIEM management**, and **alerting**.
- Helps detect suspicious activity across systems.

#### 🌐 Network & Firewall Management

- Configuration and monitoring of **firewalls**, **IDS/IPS**, and **network segmentation**.

#### 👥 Identity and Access Management (IAM)

- Managing **authentication**, **authorization**, and **user provisioning**.

#### 🧰 Security as a Service (SECaaS)

- A term often used when MSSP services are delivered **via the cloud**.
- Example: Cloud-based antivirus, email filtering, or web security platforms.

### ☁️ Cloud Access Security Brokers (CASBs)

CASBs add an **extra layer of protection** to **cloud service usage** and operate in two ways:

#### Network-based CASBs

- Act as a **middleman** between the user and cloud provider.
- **Intercepts requests** and blocks them if they violate policies.

#### API-based CASBs

- Use **cloud APIs** to monitor cloud activity **after the fact**.
- Useful for **visibility and enforcement**, but may **lack real-time blocking**.

### 📝 Best Practices When Using MSSPs

- Develop a **written agreement** that:
  - Clearly outlines **roles and responsibilities**.
  - Defines **service level agreements (SLAs)**.
  - Details **incident notification and response** procedures.

MSSPs can offer powerful capabilities—but **due diligence, clear expectations, and regular evaluation** are key to a secure and successful partnership.

## 🔐 Manage Vendor Relationships

Vendors are an essential part of IT operations—but they also introduce risk. Security professionals must manage vendor relationships to protect their organization's **confidentiality**, **integrity**, and **availability** of systems and data.

### 🔍 Vendor Security Expectations

- Vendors should follow **security policies and procedures** at least as strict as your own.
- **Data handled by vendors** must be protected as if it were handled internally.
- Poor vendor practices can become the **weakest link** in your security chain.

### ☁️ Cloud Vendor Considerations

- Cloud vendor relationships often involve **vendor lock-in**—making transitions difficult.
- Conduct **due diligence**:
  - Evaluate **financial stability**
  - Investigate **reputation and reliability**
  - Confirm **security controls** and compliance

### 🔄 Vendor Management Lifecycle

#### 1. Vendor Selection

- Can involve a **formal RFP process** or an **informal evaluation**.
- **Security team** should:
  - Contribute to requirement definitions
  - Evaluate vendors' **risk management programs**

#### 2. Onboarding

- Ensure all contract terms are clear and security expectations are set.
- Establish:
  - **Encryption protocols** for data in transit and at rest
  - **Security incident notification procedures**
  - **Access control policies**

#### 3. Ongoing Maintenance

- Perform **continuous monitoring** of vendor practices.
- Use tools like:
  - **Site visits**
  - **Security assessments**
  - **Third-party audit reports**
- If a vendor never reports an incident, consider that a **potential red flag**.

#### 4. Offboarding

- Ensure proper **data destruction** by the vendor.
- End access permissions and finalize **contractual closure**.
- May lead back to the beginning of the lifecycle with **new vendor selection**.

### 📘 Recommended Reference

Explore **ISO/IEC 27036**, particularly **Part 4**, for detailed guidance on managing the **security of cloud service provider relationships**.

## 📄 Vendor Agreements

Formal vendor agreements ensure mutual understanding, define service expectations, and protect both parties—especially from a **security and compliance** standpoint.

### 🤝 Common Types of Agreements

#### **Non-Disclosure Agreement (NDA)**

- Ensures confidentiality of information exchanged between organizations.
- Usually the **first agreement** signed during early partnership discussions.

#### **Service-Level Requirement (SLR)**

- Outlines **customer expectations** regarding vendor performance.
- May include:
  - System response time
  - Availability
  - Data retention and backup policies
  - Support timelines

#### **Service-Level Agreement (SLA)**

- A **contractual agreement** that formalizes the SLRs.
- Includes **penalties** for not meeting defined service standards.

#### **Memorandum of Understanding (MOU)**

- Informal document for **non-binding agreements**.
- Often used **internally** between business units or when legal disputes are unlikely.

#### **Business Partnership Agreement (BPA)**

- Defines responsibilities and expectations when two organizations **jointly offer a service or product**.
- Includes details like revenue sharing and project roles.

#### **Interconnection Security Agreement (ISA)**

- Required when two entities **interconnect systems or share data**.
- Specifies:
  - Encryption protocols
  - Data transfer standards
  - Security responsibilities

#### **Master Service Agreement (MSA)**

- An **umbrella contract** that governs overall vendor-customer relationship.
- Used for multiple future projects.
- Each project uses a **Statement of Work (SOW)** to define scope and deliverables under the MSA terms.

### 🔐 Security and Compliance Considerations

- Include **minimum security standards** (e.g., "Data must be encrypted using AES-256").
- Document:
  - **Data handling procedures**
  - **Compliance requirements**
  - **Access controls**

### 🕵️‍♂️ Monitoring and Audits

- Agreements should allow the **customer or third parties** to:
  - Conduct **on-site visits**
  - Review **security policies and practices**
  - Evaluate **documents and system configurations**

### ✅ Summary

Well-structured vendor agreements:

- Ensure **mutual accountability**
- Prevent **misunderstandings**
- Protect the organization from **security gaps** and **compliance issues**

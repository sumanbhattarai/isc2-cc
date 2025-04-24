# 🌐 Computer Networks

## 🌐 Network Types

Computers are powerful alone, but **networks** make them even **more powerful** by allowing communication, file sharing, and remote access.

### 🏢 **Local vs. Wide Area Networks**

| **Network Type**                | **Description**                                | **Example**                  |
| ------------------------------- | ---------------------------------------------- | ---------------------------- |
| 📡 **Local Area Network (LAN)** | Connects devices **within the same building**. | Office, Home Wi-Fi           |
| 🌍 **Wide Area Network (WAN)**  | Connects LANs over **long distances**.         | Internet, Corporate Branches |

LANs connect to WANs to access the **global internet**.

### 🔗 **Wired vs. Wireless Networks**

#### 🖥 **Wired Networks**

✔ **Uses Ethernet cables** (RJ-45 , also called 8 pin connector) for **high-speed**, stable connections.  
✔ Typically used in **offices, data centers, and gaming setups**.

> Note: In traditional telephones, RJ-11(6 pins) connectors were used.

#### 📶 **Wireless Networks**

✔ **Wi-Fi (WLAN)** – Provides **flexible** access without cables.  
✔ **Bluetooth (PAN)** – Short-range (10m) for **peripherals** (headsets, speakers).  
✔ **Near Field Communication (NFC)** – Very short-range (couple of inches) for **payments & access control**.

### ⚖ **Choosing the Right Network**

✔ **Need high speed & reliability?** Use **wired Ethernet**.  
✔ **Need convenience & mobility?** Use **Wi-Fi**.  
✔ **Connecting personal devices?** Use **Bluetooth or NFC**.

📌 **Key Takeaway**: Networks enhance **communication, accessibility, and efficiency** in modern computing! 🚀

## 🔗 Introducing TCP/IP

We use networks every day, but **how do they actually work?** The answer lies in a set of protocols called **TCP/IP**.

### 📦 **What is TCP/IP?**

TCP/IP stands for:  
✔ **Transmission Control Protocol (TCP)** – Ensures **reliable**, ordered, and error-checked delivery of data.  
✔ **Internet Protocol (IP)** – Handles **addressing** and **routing** of data packets between systems.

🖥 **IP (Network Layer)** – Provides unique **IP addresses** and ensures packets reach the correct destination.  
📡 **TCP & UDP (Transport Layer)** – Define **how data is sent** between systems.

### 🔄 **TCP vs. UDP**

| **Feature**           | **TCP(Transmission Control Protocol )** | **UDP(User Datagram Protocol)** |
| --------------------- | --------------------------------------- | ------------------------------- |
| **Connection Type**   | Connection-oriented                     | Connectionless                  |
| **Reliability**       | Reliable (guarantees delivery)          | Unreliable (no guarantee)       |
| **Use Case**          | Email, Web Browsing                     | Streaming, Voice & Video Calls  |
| **Handshake Process** | 3-way handshake (SYN, SYN-ACK, ACK)     | No handshake                    |

🔹 **TCP is used when accuracy matters**, while **UDP is used when speed is more important**.

### 🤝 **TCP Three-Way Handshake**

1️⃣ **SYN** → The client requests a connection.  
2️⃣ **SYN-ACK** → The server acknowledges and responds.  
3️⃣ **ACK** → The client confirms, and communication begins.

### 🏗 **The OSI (Open Systems Interconnection) & TCP/IP Models**

#### **📚 OSI Model (7 Layers)**

| **Layer**           | **Function**                               |
| ------------------- | ------------------------------------------ |
| 7️⃣ **Application**  | User interaction (Web browsers, Email)     |
| 6️⃣ **Presentation** | Encryption & Data Formatting               |
| 5️⃣ **Session**      | Communication Management                   |
| 4️⃣ **Transport**    | Ensures data reliability (TCP, UDP)        |
| 3️⃣ **Network**      | Routing & IP addressing (IP protocol)      |
| 2️⃣ **Data Link**    | Node-to-node communication (MAC addresses) |
| 1️⃣ **Physical**     | Hardware transmission (Wires, Wi-Fi)       |

#### **🌐 TCP/IP Model (4 Layers)**

| **Layer**               | **OSI Equivalent**                                  |
| ----------------------- | --------------------------------------------------- |
| 📤 **Application**      | OSI's Application, Presentation, and Session layers |
| 🚚 **Transport**        | OSI's Transport layer (TCP, UDP)                    |
| 🌍 **Internet**         | OSI's Network layer (IP routing)                    |
| 🖧 **Network Interface** | OSI's Data Link & Physical layers                   |

📌 **Key Takeaway**:  
TCP/IP enables modern **network communication**, balancing **reliability (TCP)** and **speed (UDP)** while using **structured models (OSI & TCP/IP)** for understanding networking. 🚀

## 🌍 IP Addresses and DHCP

For the **Internet Protocol (IP)** to deliver traffic, it needs an **addressing scheme**—just like phone numbers and street addresses.

### 🔢 **Understanding IP Addresses**

✔ **IPv4 Format:** Written in **dotted quad notation** (e.g., `192.168.1.100`).  
✔ **Range:** Each number ranges from **0 to 255** (because **8 bits = 256 values**).  
✔ **Two Parts:**

- **Network Address** (e.g., `192.168`) – Identifies the network.
- **Host Address** (e.g., `1.100`) – Identifies the specific device.

📌 **Private vs. Public IPs**

- **Private IPs** (e.g., `192.168.x.x`, `10.x.x.x`, `172.16.x.x - 172.31.x.x`) can be reused in different networks.
- **Public IPs** are unique across the entire internet.
- **Network Address Translation (NAT)** allows private IPs to communicate over the internet by mapping them to public IPs.

### 🔄 **IPv4 vs. IPv6**

| **Feature**       | **IPv4**                    | **IPv6**                                       |
| ----------------- | --------------------------- | ---------------------------------------------- |
| **Bit Length**    | 32-bit                      | 128-bit                                        |
| **Format**        | Dotted quad (`192.168.1.1`) | Hexadecimal (`2001:0db8:85a3::8a2e:0370:7334`) |
| **Address Limit** | ~4.3 billion                | Virtually unlimited                            |
| **Need for NAT?** | Yes                         | No                                             |

IPv6 adoption is growing as IPv4 addresses become scarce.

### ⚡ **Static vs. Dynamic IP Assignment**

🔹 **Static IP** – Manually assigned, used for **servers, routers, and network devices**.  
🔹 **Dynamic IP (DHCP)** – Automatically assigned via **Dynamic Host Configuration Protocol (DHCP)**.

🚀 **DHCP Benefits:**  
✔ Eliminates manual IP assignment.  
✔ Prevents conflicts by ensuring unique addresses.  
✔ Efficiently manages available IPs.

## 🌐 Network Ports

IP addresses identify a device on a network, but **network ports** direct traffic to specific applications running on that device.

### 🏢 **Analogy: Apartment Building**

- **IP Address** → Street Address (identifies the building).
- **Port Number** → Apartment Number (guides to the right unit).

📌 **Port numbers are 16-bit values** (range: **0 – 65,535**).

### 🔢 **Port Ranges and Usage**

| **Port Range**      | **Name**         | **Purpose**                                                                             |
| ------------------- | ---------------- | --------------------------------------------------------------------------------------- |
| **0 – 1,023**       | Well-Known Ports | Reserved for common protocols (assigned by IANA (Internet Assigned Numbers Authority)). |
| **1,024 – 49,151**  | Registered Ports | Used by vendors (e.g., databases, applications).                                        |
| **49,152 – 65,535** | Dynamic Ports    | Temporary, assigned as needed.                                                          |

### 🔑 **Common Network Ports to Memorize**

| **Port**          | **Protocol** | **Usage**                              |
| ----------------- | ------------ | -------------------------------------- |
| **21**            | FTP          | File Transfer Protocol                 |
| **22**            | SSH          | Secure Shell (Encrypted Remote Access) |
| **25**            | SMTP         | Sending Emails                         |
| **53**            | DNS          | Domain Name System Lookups             |
| **80**            | HTTP         | Web Traffic (Unencrypted)              |
| **110**           | POP3         | Retrieve Emails                        |
| **143**           | IMAP         | Retrieve Emails (Advanced)             |
| **443**           | HTTPS        | Secure Web Traffic (TLS/SSL)           |
| **3389**          | RDP          | Remote Desktop Protocol (Windows)      |
| **137, 138, 139** | NetBIOS      | Windows Network Communication          |
| **1433**          | MS SQL       | Microsoft SQL Server                   |
| **1521**          | Oracle DB    | Oracle Database                        |

📌 **Well-known ports help standardize network communication, ensuring devices find the correct services easily.**

## 🔐 Securing Wireless Networks

Securing wireless networks is essential to protect against unauthorized access and eavesdropping attacks. Below are best practices for ensuring your wireless network stays secure:

### 📡 **SSID (Service Set Identifier)**

- **What is SSID?**
  - It's the name of your wireless network, visible when choosing a network on a device.
- **To enhance security:**
  - **Disable SSID broadcasting** to make the network invisible to devices unless they already know the SSID.

### 🔑 **Change Default Administrative Passwords**

- **What are default passwords?**
  - These are factory-set passwords used to manage wireless access points.
- **Best Practice:**
  - **Immediately change the default passwords** to strong, unique ones to prevent unauthorized access.

### 🛡️ **Types of Wireless Authentication**

1. **Open Networks**
   - Available to anyone, no authentication required.
2. **Preshared Key (PSK)**
   - Users must enter a shared key to connect to the network.
   - **Limitations of PSK:**
     - Difficult to change the key regularly, especially for large networks.
     - No user identification, making it impossible to restrict access based on user identity (e.g., if a user leaves).
3. **Enterprise Authentication**
   - Users authenticate using **individual credentials** (username/password or other methods) via an authentication server.
   - Provides more control over access and allows easier management of user access.
4. **Captive Portals**
   - Common in public places (e.g., hotels, coffee shops).
   - **How it works:**
     - When users connect, they are redirected to a webpage requiring authentication (such as accepting terms or entering a password).

By implementing these practices, you can secure your wireless network and limit unauthorized access.

## 🔐 Wireless Encryption

Wireless encryption is essential to protect network traffic from **eavesdropping** and unauthorized access. Encryption ensures that only users with the decryption key can interpret the transmitted data.

### 📜 **Evolution of Wireless Encryption Standards**

| Encryption Standard                | Status             | Security Level   | Notes                                                                              |
| ---------------------------------- | ------------------ | ---------------- | ---------------------------------------------------------------------------------- |
| **WEP (Wired Equivalent Privacy)** | ❌ **Insecure**    | 🔴 **Weak**      | Contains severe vulnerabilities. **Never use WEP.**                                |
| **WPA (Wi-Fi Protected Access)**   | ⚠️ **Obsolete**    | 🟠 **Moderate**  | Uses **TKIP (Temporal Key Integrity Protocol)** but still has vulnerabilities.     |
| **WPA2**                           | ✅ **Secure**      | 🟢 **Strong**    | Uses **AES-based CCMP encryption**. Still widely used.                             |
| **WPA3**                           | ✅ **Most Secure** | 🟢 **Strongest** | Uses **CCMP + SAE (Simultaneous Authentication of Equals)** for better protection. |

### 🔑 **Key Features of WPA2 and WPA3**

- **WPA2 (2004)**
  - **Uses AES-based CCMP encryption** for strong security.
  - Considered **secure and widely used** despite some vulnerabilities.
- **WPA3 (2020)**
  - Introduces **Simultaneous Authentication of Equals (SAE)** for improved key exchange security.
  - Provides **better protection against brute force attacks**.
  - **Mandatory for new wireless devices** as of 2020.

### ⚠️ **Best Practices**

- **Never use WEP or WPA**—they are outdated and vulnerable.
- **Always use WPA2 or WPA3** for secure wireless communication.
- **Upgrade to WPA3** where possible for the best security.

## 🔍 Ping and Traceroute

Network administrators use **ping** and **traceroute** for troubleshooting and analyzing network connectivity.

### 📡 **Ping Command**

**Ping** checks if a remote system is reachable by sending an **ICMP (Internet Control Message Protocol) echo request** and waiting for an **ICMP echo reply**. It helps diagnose network issues by verifying if a system is accessible and measuring round-trip latency.

#### **How Ping Works:**

1. Sends an **ICMP echo request** packet.
2. Receives an **ICMP echo reply** if the system is reachable.
3. Measures **response time** (latency) in milliseconds.

#### **Usage:**

- **Syntax:**
  ```sh
  ping <IP_address>  # Example: ping 8.8.8.8
  ping <domain_name> # Example: ping www.google.com
  ```
- **Stopping a ping loop:** Press `Ctrl + C`
- **Important Note:** Some servers block **ICMP requests**, causing no response.

### 🛤 **Traceroute Command**

**Traceroute** tracks the path packets take from the source to the destination. It helps identify network bottlenecks and unreachable hops.

#### **How Traceroute Works:**

- Sends **ICMP packets** with increasing **TTL (Time-To-Live)** values.
- Each router along the way **decreases the TTL** and replies when it reaches **0**.
- Displays the **IP address or hostname** of each hop.

#### **Usage:**

- **Mac/Linux:**
  ```sh
  traceroute <domain_name>  # Example: traceroute www.google.com
  ```
- **Windows:**
  ```sh
  tracert <domain_name>  # Example: tracert www.google.com
  ```

#### **Interpreting Traceroute Output:**

| Output                  | Meaning                                       |
| ----------------------- | --------------------------------------------- |
| `X.X.X.X` or `hostname` | The router's IP/hostname along the path.      |
| `* * *`                 | The router does not respond to ICMP requests. |

### 🛠 **Additional Tools**

- **Hping**: A more advanced version of ping that allows custom packet manipulation.
- **Pathping (Windows Only)**: Combines **ping** and **tracert** into one command.
  ```sh
  pathping <domain_name>
  ```

### 🔎 **Best Practices for Troubleshooting**

| **Step**                                               | **Command**           | **Interpretation**                                         |
| ------------------------------------------------------ | --------------------- | ---------------------------------------------------------- |
| **1. Check if a website is up.**                       | `ping <domain>`       | If no response, the website may be down or blocking pings. |
| **2. Check if internet access is working.**            | `ping 8.8.8.8`        | If this fails, there may be an internet issue.             |
| **3. Diagnose network routing issues.**                | `traceroute <domain>` | Identifies where packets are getting dropped.              |
| **4. Use Pathping for a detailed analysis (Windows).** | `pathping <domain>`   | Shows latency at each hop.                                 |

### ⚠️ **Key Takeaways**

- **Use ping** to check if a system is online and measure latency.
- **Use traceroute** to identify network paths and potential bottlenecks.
- **Some networks block ICMP**, so lack of response doesn’t always mean a system is down.
- **Pathping (Windows)** provides additional insights into network issues.

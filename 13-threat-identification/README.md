# 🕵️‍♂️ Threat Identification and Prevention

## 🔐 Intrusion Detection and Prevention

Intrusion detection and prevention systems (IDPS) play a crucial role in defending networks against attackers and security threats. These systems monitor network traffic and can take action when they detect malicious activity.

### 🕵️‍♂️ **Intrusion Detection Systems (IDS)**

An **IDS** monitors network traffic to detect suspicious activity, such as:

- **SQL injection** attempts.
- **Malformed packets** causing potential denial of service.
- **Unusual login attempts** based on time or user behavior.
- A system attempting to contact a **botnet command and control server**.

Once malicious traffic is detected, the IDS alerts administrators for further investigation.

### 🚫 **Intrusion Prevention Systems (IPS)**

An **IPS** is similar to an IDS but with the added ability to take immediate corrective action. For example, it can **block malicious traffic** from entering the network. This is especially useful when administrators are unavailable or overwhelmed by a high volume of alerts.

### ❌ **Types of Errors in IDS/IPS**

Two main types of errors can occur with IDS/IPS systems:

- **False positives**: When the system incorrectly flags benign (normal , harmless) activity as an attack.
- **False negatives**: When the system fails to detect an actual attack.

### 🧬 **Detection Methods**

1. **Signature Detection**  
   This method works like **antivirus software**, using a database of known malicious patterns (signatures). When the IDS/IPS detects traffic matching a signature, it triggers an alert.

   - **Pros**: High reliability with low false positives.
   - **Cons**: Cannot detect new, unknown attacks.

2. **Anomaly Detection**  
   This method establishes a **model of normal network activity** and flags deviations as suspicious.

   - **Pros**: Can detect new and unknown attacks.
   - **Cons**: Higher false positive rate.

   This method is also known as:

   - **Behavior detection**
   - **Heuristic detection**

### 🏗️ **Deployment Methods**

- **In-band (Inline) Deployment**  
  In this setup, the **IPS** sits directly on the network path, meaning all traffic passes through it. It can actively block malicious traffic but also presents a risk since it is a **single point of failure**.

- **Out-of-band (Passive) Deployment**  
  The **IPS** is not in the network path but is connected to a span port on a switch, receiving copies of the traffic. It can **alert** and block future traffic but cannot stop an attack from entering the network in real-time.

### ⚠️ **Choosing the Right System**

As a security professional, understanding the strengths and weaknesses of both **IDS** and **IPS** and choosing the appropriate deployment model (in-band vs. out-of-band) is critical for optimal network security.

## 🔐 Malware Prevention

Malware is a major threat to computer and mobile device security, but a variety of tools can be used to protect systems from these threats. Modern **antimalware software** defends against viruses, worms, Trojan horses, and spyware.

### 🧬 **Antivirus Software Mechanisms**

1. **Signature Detection**

   - **How it works**: Signature-based antivirus software uses databases of known malware patterns to scan system files and memory for any matches.
   - **Action**: If a match is found, the software removes or quarantines the malicious content for further analysis.
   - **Important**: To remain effective, **virus definition files** must be updated regularly to include signatures for newly discovered malware.

2. **Heuristic (Behavior) Detection**
   - **How it works**: Rather than relying on known malware patterns, heuristic detection models **normal system behavior** and reports anomalies or suspicious activities that deviate from that normal behavior.
   - **Use**: This method is often found in **endpoint detection and response (EDR)** solutions, which offer advanced protection.

### 🖥️ **Endpoint Detection and Response (EDR)**

EDR solutions provide **advanced, real-time protection** by:

- Analyzing endpoints for signs of malicious activity.
- Monitoring memory, processor use, registry entries, network traffic, and other system behaviors.
- Triggering **automated responses** to defend against attacks.

EDR systems also provide **sandboxing** capabilities:

- **Sandboxing** isolates suspicious executables before they run, checking their behavior in a safe environment.
- If the executable behaves maliciously, it is blocked from running on the protected system.

### 🛡️ **Windows Defender Example**

**Windows Defender** is built into Windows and provides basic antimalware protection:

- It performs scans to identify malicious activity, with options for **quick, full, or custom scans**.
- Users can **update virus definitions** and review the **history of quarantined items** or past scans.

### 🛠️ **Other Antimalware Packages**

Many other antimalware tools are available across various operating systems, providing comprehensive protection against evolving threats.

## 🔐 Port Scanners

Testing systems for security vulnerabilities is a critical task for security professionals, but it can be time-consuming. Vulnerability assessment tools automate this process. These tools fall into three categories:

1. **Port scanners** – Check for open network ports on a system.
2. **Vulnerability scanners** – Check open ports for known vulnerabilities.
3. **Application scanners** – Probe deep into web applications to detect flaws.

### 🧰 **Port Scanners**

Port scanners are tools that check all 65,535 network ports on a server to see which ones are open. This process is like checking the doorknobs of a server to find any unlocked doors. One popular port scanning tool is **nmap**.

### 📡 **Running an nmap Scan**

In this example, the target of the scan is a Windows server. The scan is initiated with the `nmap` command followed by the target IP address. The tool checks the open ports on the system. This can take anywhere from a few seconds to several minutes depending on network distance and the number of ports being checked.

- Example:
  ```bash
  nmap <IP_address>
  ```

Once the scan is complete, the results show which ports are open. In this case, the server has:

- **Port 80**: Used for a web server.
- **Port 3389**: Remote Desktop Protocol (RDP) port, commonly associated with Windows systems.

### 🌐 **Verifying the Results**

After finding port 80 open, you can verify the web server by typing the IP address into a browser. If you see the default homepage for **Microsoft Internet Information Services (IIS)**, it's confirmed as a Windows web server.

### 🔐 **Security Implications**

For attackers, open ports like **3389** (Remote Desktop Protocol) and **80** (web server) represent potential targets. For security professionals, these results can guide decisions on whether these services should be exposed or if they need to be secured further.

## 🔐 Vulnerability Scanners

**Vulnerability scanners** go beyond simple port scans by delving into the details of services running on open ports and identifying known vulnerabilities associated with those services. These tools help in finding potential security weaknesses in a system, providing valuable **remediation information** for system administrators to patch vulnerabilities. However, in the wrong hands, this information can also serve as a roadmap for attackers.

### 🛠️ **Nessus: A Popular Vulnerability Scanner**

**Nessus** is a web-based vulnerability scanner that identifies potential vulnerabilities in a server. Here's a breakdown of how it works:

- **Scanning Process**  
   Nessus scans servers for known vulnerabilities by using a database of vulnerability exploits and testing services that run on open ports. The scan results help administrators know where to focus their remediation efforts.

- **Scanning Example**  
   When scanning a Windows server, Nessus typically reports:

  - **Medium vulnerabilities** (those that require immediate attention)
  - **Informational vulnerabilities** (less critical)

  In this scenario, Nessus identified vulnerabilities related to SSL/TLS, including:

  - An untrusted SSL certificate (self-signed).
  - Medium-strength cipher suites.

  These findings help administrators know exactly which areas to focus on to enhance security.

- **Vulnerability Details**  
   Nessus not only reports the vulnerabilities but also provides detailed information on:
  - **Detected cipher suites** that may be problematic.
  - **Steps** to fix the issues, such as improving SSL/TLS configurations.

By using a tool like Nessus, organizations can actively monitor their systems for vulnerabilities and take actionable steps to secure their infrastructure.

### 🔒 **The Importance of Regular Scanning**

Regularly running vulnerability scans with tools like Nessus ensures that potential risks are identified early and mitigated before they can be exploited.

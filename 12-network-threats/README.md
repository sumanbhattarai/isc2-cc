# 🛑 Network Threats

## 🔐 Viruses, Worms, and Trojans

**Malware** (short for **malicious software**) is a major cybersecurity threat that infects computer systems to **steal data, damage files, or disrupt operations**. Every piece of malware has two key components:

1. **Propagation Mechanism** – How it spreads between systems.
2. **Payload** – The malicious action it performs.

### 🦠 **Types of Malware**

| Malware Type     | Propagation Mechanism                                                                                               | Attack Method                                   | Prevention Strategy                                                      |
| ---------------- | ------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------- | ------------------------------------------------------------------------ |
| **Virus**        | Requires **user action** to spread (e.g., opening an email attachment, clicking a link, inserting an infected USB). | Infects files and spreads when executed.        | **User education**, email security, antivirus software.                  |
| **Worm**         | Spreads **automatically** by exploiting system vulnerabilities. No user action required.                            | Infects systems and uses them to attack others. | **System updates**, firewalls, intrusion detection systems.              |
| **Trojan Horse** | Disguises itself as **legitimate software** to trick users into installing it.                                      | Executes malicious code once installed.         | **Application control**, downloading software only from trusted sources. |

### ⚠️ **Key Differences**

- **Viruses require user action** to spread.
- **Worms spread automatically** without user intervention.
- **Trojan horses deceive users** by posing as legitimate software.

### 🛡️ **Best Practices for Malware Defense**

✔️ Keep software and operating systems **up to date**.  
✔️ **Avoid suspicious email links and attachments**.  
✔️ Use **trusted antivirus and anti-malware software**.  
✔️ Implement **application control** to restrict unauthorized software.  
✔️ Enable **firewalls and intrusion detection systems**.

## 🔐 Botnets

**Botnets** are networks of **infected computers** (also called **zombies**) controlled by hackers for **malicious activities**. These infected systems remain **dormant** until they receive instructions from a **command and control (C2) network**.

### 🦠 **How Botnets Are Created**

1. **Infection** – Hackers use malware (worms, Trojans, viruses) to **infect systems**.
2. **Recruitment** – Infected systems join the **botnet** and await commands.
3. **Expansion** – Some bots may spread malware to recruit **more systems**.
4. **Command & Control (C2)** – The hacker controls the botnet using **hidden communication channels** (IRC, Twitter, P2P networks).
5. **Execution** – Bots **carry out attacks** as instructed by the hacker.

### ⚠️ **How Hackers Use Botnets**

| Attack Type                              | Purpose                                                        |
| ---------------------------------------- | -------------------------------------------------------------- |
| **Spam Delivery**                        | Sends bulk spam emails.                                        |
| **Distributed Denial of Service (DDoS)** | Overloads websites and services to make them unavailable.      |
| **Cryptocurrency Mining**                | Uses infected systems’ computing power to mine cryptocurrency. |
| **Brute Force Attacks**                  | Tries to crack passwords using automated login attempts.       |

### 🛡️ **How to Defend Against Botnets**

✔️ **Use up-to-date antivirus and anti-malware software** to detect infections.  
✔️ **Monitor network traffic** for unusual outbound connections.  
✔️ **Implement firewalls and intrusion detection/prevention systems (IDS/IPS)**.  
✔️ **Restrict unauthorized software** to prevent malware execution.  
✔️ **Educate users** on phishing attacks and malware threats.

By understanding botnets and their **command-and-control structures**, security professionals can detect **compromised systems** and shut down **botnet activity** before it causes damage. 🚀

## 🔐 Eavesdropping Attacks

**Eavesdropping attacks** occur when an attacker gains access to the communication path between a **client** and **server**, potentially viewing confidential information. This can be done through **physical** or **logical** access to a network.

### 🛠️ **Methods of Eavesdropping Attacks**

1. **Physical Tapping** – Direct access to network cables or devices.
2. **DNS or ARP Poisoning** – Tricks systems into sending traffic to the attacker instead of the intended destination.
3. **Man-in-the-Middle (MitM) Attacks** – The attacker intercepts and relays communication between two systems, often without the sender or receiver knowing.
4. **Man-in-the-Browser Attacks** – The attacker compromises the user's browser or a plugin to gain access to web communications.
5. **Replay Attacks** – The attacker captures previously sent data (e.g., authentication tokens) and replays it to gain unauthorized access.

### 🔒 **MitM Attack Details**

- The attacker intercepts communication between the user and server, acting as a relay.
- The attacker can read, alter, or replay communication between the client and the server.
- **Prevention**: Use of **HTTPS**, where encryption protects communications from eavesdropping.

### 🔄 **Replay Attacks**

- The attacker captures encrypted data (e.g., authentication tokens) and resends it to authenticate a connection without the user’s involvement.
- **Defense**: Use **session tokens** with short expiration times or **timestamps** to prevent replaying old sessions.

### ⚡ **SSL Stripping**

- In this attack, the attacker **downgrades** an encrypted **HTTPS** connection to **HTTP**, stripping away encryption and allowing eavesdropping.
- **Prevention**: Ensure that **SSL/TLS** is enforced and not downgraded by using strict security policies.

### 🛡️ **Protection Against Eavesdropping**

- **Use encryption** (e.g., HTTPS) to secure communications.
- **Regularly update** security protocols (e.g., SSL/TLS).
- **Monitor network traffic** for unusual patterns or unauthorized access.
- **Educate users** about phishing and risks of insecure connections.

With this knowledge, you can detect and prevent **eavesdropping** attacks to keep sensitive data secure. 🔒

## 🔐 Implementation Attacks

Cryptographic systems may have vulnerabilities based on their **design** or how they are **implemented**. These flaws can allow attackers to break the system's security.

### 🛠️ **Fault Injection Attacks**

An attacker tries to compromise a cryptographic device by introducing **external faults**. This might involve high-voltage electricity, temperature changes, or other conditions that cause the system to malfunction. These faults can cause the system to:

- Fail to properly encrypt data.
- Leak unencrypted data.
- Experience other security failures.

### 🏃‍♂️ **Side-Channel Attacks**

Attackers can exploit system activity **footprints** (e.g., power consumption, processor utilization, or electromagnetic radiation) to gain insight into the cryptographic process. These signals can sometimes be captured to retrieve information that is being encrypted.

### ⏱️ **Timing Attacks**

A specific type of side-channel attack where the attacker **measures** how long cryptographic operations take. This timing data may be used to:

- Infer details about the cryptographic process.
- Exploit weaknesses in the system's implementation to gain unauthorized access.

### 🛡️ **Protection Against Implementation Attacks**

- Design cryptographic systems carefully, considering both theoretical and practical security aspects.
- Protect cryptographic devices against **physical manipulation** and **faults**.
- Minimize **leakage of side-channel information** through techniques like constant-time algorithms or shielding.

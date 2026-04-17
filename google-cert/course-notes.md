# Google Cybersecurity Certificate - Course Notes

## ✅ Course 1 - Foundations of Cybersecurity

**What I learned**
- Learned the core purpose of cybersecurity: protecting systems, networks, and data from unauthorized access and attacks.
- Built familiarity with the CIA Triad: confidentiality, integrity, and availability.
- Reviewed major threat actors such as cybercriminals, nation-states, insiders, and hacktivists.
- Introduced to major security frameworks, including NIST CSF, and why organizations use them to manage risk.
- Learned how social engineering, phishing, and malware fit into the broader threat landscape.

**Why this matters**
This course built the base for understanding how organizations think about security, risk, and attacker behavior.

![Course 1 Certification](certificates/course-one-cert.png)

## ✅ Course 2 - Play It Safe: Manage Security Risks 

**What I learned**
- Studied the NIST CSF five functions: Identify, Protect, Detect, Respond, and Recover.
- Learned basic risk management concepts, including how to identify, assess, and prioritize risk.
- Reviewed the role of audits, compliance, and security policies in organizations.
- Learned how SIEM tools help collect and analyze logs for threat detection.
- Practiced understanding how SOC analysts use playbooks and incident response workflows.

**Why this matters**
This course introduced the mindset and structure behind how security teams manage threats and respond to incidents.

![Course 2 Certification](certificates/course-two-cert.png)

## ✅ Course 3 - Connect and Protect: Networks and Security 

**What I learned**
- Learned how networks function, including LAN, WAN, and how devices communicate across layers.
- Built a foundation in the TCP/IP model and common protocols such as TCP, UDP, HTTP, HTTPS, DNS, and FTP.
- Learned basic IP addressing concepts, including IPv4 and IPv6.
- Explored common security tools like firewalls, IDS, IPS, and VPNs.
- Reviewed common network attacks such as DDoS, packet sniffing, and man-in-the-middle attacks.
- Learned why patching and closing unnecessary ports are important for network hardening.

**Why this matters**
This course gave me the networking foundation needed to understand traffic, threats, and security controls in real environments.

![Course 3 Certification](certificates/course-three-cert.png)

## ✅ Course 4 - Tools of the Trade: Linux and SQL 

Key Skills: Linux administration, file management, permissions, user management, SQL querying

**Linux Package Management**
- In this lab I installed Suricata (a network security monitoring tool) using apt package manager, verified successful deployment, then cleanly removed it.

![Installing Suricata](assets/downloading-suricata.png)
![Removal Suricata](assets/removed-suricata.png)

What this shows: Ability to deploy and manage security tools in Linux enviornments.

**Linux File System Navigation & Analysis**
- Navigated directories using pwd, ls, cd, cat. I also used grep with piping (|) to search server logs for "error" patterns. 

![Doing basic navigation](assets/basic-navigation.png)
![Viewing file contents](assets/absolute-path-and-cat.png)
![Basic filtering](assets/grep-filter.png)
![Filtering with grep and piping](assets/grep-piping.png)
![More filtering with grep and piping](assets/more-grep-filtering.png)

What this shows: Log analysis skills critical for SOC analysts investigating incidents. 

**File & Directory Management**
- This lab I created/removed directories (mkdir/rmdir), moved files (mv), deleted files (rm), created files (touch), and edited files with nano. 

![Adding and removing directories](assets/mkdir-rmdir.png)
![Moving a file](assets/mv-move.png)
![Removing and creating a file](assets/rm-touch.png)
![Editing a file](assets/nano-editior.png)
![Output of the file](assets/nano-output-cat.png)

**File permissions & Access Control**
- Viewed permissions of files (ls -l/ls -la), modified with chmod o-w to enforce least privilege, and managed hidden files.

![Showing permissions of the files](assets/showing-permissions.png)
![Changing the permissions of the files](assets/changing-permissions.png)
![Revealing and changing permissions of hidden files](assets/hidden-file-change.png)

What this shows: Understanding of access control fundamental to sysadmin/SOC roles. 

**User & Group Management**
- Practiced creating users (sudo useradd), assigned the user with primary/secondary groups (usermod -g), changed ownership (chown), and handled group deletion issues.

![Creating, assigning, and removing the user](assets/new-user.png)

What this shows: Practical Active Directory/Linux admin skills.

**SQL Database Querying**
- This lab I practiced with SQL by querying login attempts using SELECT, WHERE, ORDER BY, BETWEEN, AND/OR/NOT, and using INNER/LEFT/RIGHT JOINs.

![Getting log in attempts from database](assets/log-in-attempts.png)
![Ordering by the login date](assets/order-by-login-date.png)
![Filtering the login date and login time](assets/filtering-login-date-login-time.png)
![Finding a specific word](assets/more-sql-filter.png)
![Finding the specific pattern](assets/like-operator-percen.png)
![Finding data after a specific date](assets/data-after-date.png)
![Pulling data between two different times](assets/between-time.png)
![Failed login attempts after 18:00](assets/failed_login_attempts.png)
![Finding a specific department within an office](assets/finding-department-and-where-office.png)
![Excluding IT](assets/anywhere-but-IT.png)
![Inner join](assets/inner-join.png)
![Left join](assets/left-join.png)
![Right join](assets/right-join.png)

What this shows: Log analysis and investigation skills used in SIEM platforms. 

**Tools Used/Practiced With**
- Bash shell (CLI navigation, grep, piping)
- Package management (apt)
- Text editors (nano)
- File permissions (chmod, chown)
- User management (useradd, usermod, groupdel1)
- SQL (SELECT, WHERE, LIKE, ORDER BY, JOINs)
- Suricata IDS (installation/testing)

![Course 4 certification](certificates/course-four-cert.png)

## ✅ Course 5 - Assets, Threats and Vulnerabilities 

Key Skills: Risk assessment, cryptography, threat analysis, vulnerability management

**Asset Management & Risk Analysis**
- Classified assets by sensitivity (Restricted/Internal/Public) and data states (Use/Transit/Rest).
- Built risk register scoring bank's funds using Likelihood x Severity matrix.
- Condicted home asset inventory to map personal attack surface.

**Linux Cryptography Labs**
SHA-256 File Integrity Verification
- Generated file hashes with sha256sum, compared to detecting tampering which is a core SOC analyst skill for malware detection. 

![Hashing files using sha256sum](assets/hashing-sha.png)
![Comparing hash](assets/difference-hash.png)

**File Decryption & Analysis**
- Used the tr command for text translation and openssl for decryption, revealing hidden messages in encrypted files. 

![Using the tr command to understand text file](assets/decreptying-text-tr.png)
![Using openssl to decrypt files](assets/decrypted-file-found.png)

What this shows: Command-line handling of encrypted data during investigations

**Real-World Threat Scenarios**
- Reviewed a data leak incident where a sales representative accidentally shared a link to an internal folder with a business partner who then posted it publicly on social media. Applied NIST SP 800-53 AC-6 guidance on least privilege and recommended restricting access to sensitive resources based on user role and regularly auditing user privileges to prevent similar exposure.

**Parking Lot USB Exercise**
- Analyzed a scenario where a hospital employee named Jorge found a USB drive in a parking lot and plugged it in. The drive contained personal and work files including PII of coworkers and hospital operational data. Identified how an attacker could use this information to craft targeted phishing emails impersonating coworkers or relatives. Recommended managerial controls like employee awareness training, operational controls like routine antivirus scans, and technical controls like disabling AutoPlay on company computers to prevent automatic execution of malicious code.

![Exemplar review](assets/Exemplar-review-usb.png)

**Playbook Incident Documentation**
- Used a security playbook to document a simulated incident, following 
structured steps to record what happened, who was involved, and what 
actions were taken in response. This mirrors the real workflow a Tier 1 
SOC analyst follows when triaging and responding to alerts.

**Phishing Email Triage**
- Identified red flags: domain mismatch, urgent language, suspicious links, credential requests. 

**Security Concepts Mastered**
- Asset classification & data lifecycle
- Risk = Likelihood × Severity scoring
- SHA-256 integrity verification
- Symmetric/asymmetric encryption (PKI)
- OWASP Top 10 (injection, XSS, broken access control)
- Social engineering lifecycle (prepare/trust/persuade/disconnect)
- Malware taxonomy (11 types including fileless/rootkits)
- Defense in depth (5 layers)
- Threat modeling (PASTA, attack trees)

## ✅ Course 6 - Detection & Response

Key Skills: Packet analysis, SIEM workflow, IDS rules, incident triage, log analysis

**What I Built & Practiced**
Packet Analysis Lab - Wireshark Traffic Investigation
- In this Wireshark lab I analyzed website browsing PCAP: filtered DNS (udp.port == 53), TCP streams, inspected IPv4 headers (source.dest IPs, TTL, protocol).

![Wireshark applying a filter](assets/applying-fillter-wireshark.png)
![Finding the packet arrival time](assets/packet-arrival.png)
![Seeing the destination source](assets/destination-source.png)
![Seeing the IP source destination](assets/ip-source-destination.png)
![Finding the same source IP](assets/source-ip-command.png)
![Finding packets being sent to the IP](assets/packets-sent-to-ip.png)
![Filtering ethernet mac traffic](assets/eth-mac-traffic-filter.png)
![IP addresses associated with the website](assets/addresses-associated-google.png)

What this shows: Core SOC skill for investigating network-based alerts.

**tcpdump Live Capture**
- In the Linux terminal I captured Linux traffic, identified interfaces (-i eth0), saved PCAPs (-w), filtered by port/host (port 80, host 192.168.1.1).

![Identifying network interfaces in Linux](assets/identify-network-interfaces-linux.png)
![Capturing 5 packets](assets/captured-5-packets.png)
![tcpdump with command explanations](assets/tcpdump-command-extra-options.png)
![Capturing the packet data](assets/packet-data-captured.png)

**IDS Rules & Log Analysis**
Suricata Custom Rule Testing
- Wrote/tested custome detection rules against sample.pcap. Analyzed fast.log (alert summary) and eve.json (detailed telemtry)

![Suricata Signature](assets/suricata-signature.png)
![Suricata commands and explanations](assets/suricata-commands.png)
![Sruicata log alert](assets/log-alert-suricata.png)
![jq command](assets/jq-command.png)

What this shows: Rule creation and log interpretation for threat hunting. 

**Advanced SOC Concepts Practiced**
- SIEM workflow (collect/normalize/analyze)
- Packet structure (header/payload/footer)
- Wireshark filters (ip.addr==, udp.port==53, http contains)
- tcpdump syntax (-i, -w, -c, port, host)
- IDS rule anatomy (action/header/options)
- Suricata logs (fast.log, eve.json)
- Threat hunting vs reactive monitoring
- Chain of custody documentation
- TTPs analysis
- False/true positive triage

## Course 7 - Automate Cybersecurity Tasks with Python *(In progress)*


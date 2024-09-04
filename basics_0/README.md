## Networking basics #0

## **1. OSI Model (Open Systems Interconnection)**

### **What is it?**
The OSI model is a reference framework that standardizes the functions of a communication system in a network into seven distinct layers. It was developed by the International Organization for Standardization (ISO) to facilitate interoperability between different network systems and manufacturers.

### **Number of layers**
The OSI model consists of **7 layers**.

### **Layer organization**

1. **Layer 1: Physical**
   - **Function:** Transmits bits over a physical medium (cables, fiber optics, radio waves).
   - **Example:** An Ethernet cable connecting a computer to a switch.

2. **Layer 2: Data Link**
   - **Function:** Provides error-free data transfer between two directly connected devices.
   - **Example:** MAC addresses that uniquely identify each device on a local network.

3. **Layer 3: Network**
   - **Function:** Determines how data is routed from the source to the destination across multiple networks.
   - **Example:** IP addresses and routers that direct traffic between different subnets.

4. **Layer 4: Transport**
   - **Function:** Manages end-to-end data transfer, ensuring integrity and order.
   - **Example:** TCP and UDP protocols that control how data is sent.

5. **Layer 5: Session**
   - **Function:** Establishes, maintains, and terminates sessions between applications.
   - **Example:** Dialogue control between applications, like a chat session.

6. **Layer 6: Presentation**
   - **Function:** Translates data between the network format and the format understood by the application.
   - **Example:** Data encryption and compression, like SSL/TLS for secure connections.

7. **Layer 7: Application**
   - **Function:** Provides network services directly to user applications.
   - **Example:** HTTP protocols for web browsing, SMTP for email.

### **Practical Example of the OSI Model**

Imagine you are sending an email from your computer:

1. **Layer 7 (Application):** You use an email client (like Outlook) to draft the message.
2. **Layer 6 (Presentation):** The email is encrypted for security.
3. **Layer 5 (Session):** A session is established with the mail server.
4. **Layer 4 (Transport):** TCP ensures the email is sent correctly.
5. **Layer 3 (Network):** The IP address directs the email to the destination server.
6. **Layer 2 (Data Link):** The MAC address ensures the email reaches the correct device within the local network.
7. **Layer 1 (Physical):** Data is transmitted via Ethernet cables or Wi-Fi.

---

## **2. Types of Networks**

### **LAN (Local Area Network)**

#### **What is a LAN**
A LAN is a local area network that connects devices within a limited geographical location, such as an office, school, or home.

#### **Typical use**
- Sharing resources like printers and files.
- Local multiplayer gaming.
- Shared internet connection.

#### **Typical geographical size**
- Usually covers a building or a campus.

#### **Example:**
In an office, all computers are connected to a LAN that allows file sharing and access to a common printer.

### **WAN (Wide Area Network)**

#### **What is a WAN**
A WAN is a network that covers a large geographical area, such as a city, country, or even worldwide. WANs connect multiple LANs.

#### **Typical use**
- Connecting offices of a company located in different cities.
- Access to cloud services.
- International communication.

#### **Typical geographical size**
- Can span entire continents.

#### **Example:**
A multinational company with offices in New York, London, and Tokyo uses a WAN to connect all its branches, allowing communication and access to shared resources in real-time.

### **Internet**

#### **What is the Internet**
The Internet is a vast global network that interconnects millions of private, public, academic, business, and government networks. It is a network of networks that enables communication and information exchange worldwide.

#### **Example:**
When you access a website, your computer communicates with servers located in different parts of the world through the Internet to display the requested page.

---

## **3. MAC Address (Media Access Control)**

### **What is a MAC address**
A MAC address is a unique identifier assigned to a device’s network interface. It operates at the data link layer of the OSI model and is used for communication within a local network.

### **Format**
- Typically represented as six pairs of hexadecimal characters, e.g., `00:1A:2B:3C:4D:5E`.

### **Example:**
When you connect your computer to a Wi-Fi network, the router identifies your device by its MAC address to allow or deny access.

---

## **4. IP Address (Internet Protocol)**

### **What is an IP address**
An IP address is a unique identifier assigned to each device connected to a network that uses the Internet Protocol for communication.

### **Types of IP addresses**

#### **1. IPv4 Address**
- **Format:** 32 bits, represented in four octets separated by dots (e.g., `192.168.1.1`).
- **Example:** Your router's IP address might be `192.168.1.1`.

#### **2. IPv6 Address**
- **Format:** 128 bits, represented in eight groups of four hexadecimal characters separated by colons (e.g., `2001:0db8:85a3:0000:0000:8a2e:0370:7334`).
- **Example:** An IPv6 address might be `fe80::1ff:fe23:4567:890a`.

### **Private and Public IP Addresses**

#### **Private Address**
- **Definition:** Addresses used within a private network that are not routable on the Internet.
- **Common ranges:**
  - `10.0.0.0` to `10.255.255.255`
  - `172.16.0.0` to `172.31.255.255`
  - `192.168.0.0` to `192.168.255.255`
- **Example:** Your computer at home might have a private IP address like `192.168.1.100`.

#### **Public Address**
- **Definition:** Unique addresses across the entire Internet, assigned by Internet Service Providers (ISP).
- **Example:** Your home's public IP address might be `203.0.113.45`.

### **Localhost**
- **Definition:** A special IP address that refers to the local computer.
- **Address:** `127.0.0.1` in IPv4 and `::1` in IPv6.
- **Example:** If you run a local web server on your computer, you can access it by browsing to `http://localhost` or `http://127.0.0.1`.

### **Subnet**
- **Definition:** A logical subdivision of a larger IP network.
- **Example:** In a corporate network with the IP address `192.168.1.0/24`, subnets can be created like `192.168.1.0/26`, `192.168.1.64/26`, etc., to segment different departments.

### **Why IPv6 was created**
Due to the depletion of IPv4 addresses, IPv6 was developed to provide a much larger address space and to solve scalability and security issues.

---

## **5. TCP and UDP Protocols**

### **TCP (Transmission Control Protocol)**
- **Function:** Provides reliable, connection-oriented communication between devices.
- **Characteristics:**
  - Establishes a connection before transmitting data.
  - Ensures data delivery in the correct order.
  - Flow control and error correction.
- **Example:** Web browsing (HTTP/HTTPS), email (SMTP).

### **UDP (User Datagram Protocol)**
- **Function:** Provides faster but less reliable, connectionless communication.
- **Characteristics:**
  - No prior connection establishment.
  - No guarantee of data delivery or order.
  - Lower overhead and latency.
- **Example:** Real-time transmissions like live video, online gaming, VoIP.

### **Key differences between TCP and UDP**
| Characteristic          | TCP                               | UDP                               |
|-------------------------|-----------------------------------|-----------------------------------|
| Connection-oriented     | Yes                               | No                                |
| Reliability             | High (retransmission of lost data) | Low (no delivery guarantee)       |
| Flow control            | Yes                               | No                                |
| Order of delivery       | Guaranteed                        | Not guaranteed                    |
| Speed                   | Slower due to verification        | Faster due to simplicity          |

### **TCP/UDP Ports**

#### **What is a port**
A port is a number that identifies a specific application or service on a device within a network.

#### **Common Ports**
- **SSH (Secure Shell):** Port `22`
- **HTTP (HyperText Transfer Protocol):** Port `80`
- **HTTPS (HyperText Transfer Protocol Secure):** Port `443`

### **Example:**
When you access a secure website, your browser uses port `443` to establish an HTTPS connection with the web server.

---

## **6. Network Tools and Protocols**

### **Netstat**
- **Description:** A command-line tool that displays network connections, routing tables, interface statistics, and more.
- **Common usage:**
  - View active connections and ports in use.
  - Diagnose network problems.
- **Example command:**
  ```bash
  netstat -tuln
  ```
  This command shows all TCP and UDP connections listening on numeric ports.

### **Ping**
- **Description:** A diagnostic tool that checks connectivity

 between two devices on a network.
- **Function:** Sends ICMP Echo Request messages and waits for Echo Reply.
- **Example usage:**
  ```bash
  ping google.com
  ```
  This sends a ping to Google's server to check if it's reachable.

### **Traceroute**
- **Description:** A tool that traces the path data takes to reach a destination on a network.
- **Function:** Displays each hop along the route, showing the IP address and response time.
- **Example usage:**
  ```bash
  traceroute google.com
  ```
  This shows the path data takes from your computer to Google's server.

### **DNS (Domain Name System)**
- **Description:** Translates domain names (e.g., `google.com`) into IP addresses (e.g., `172.217.10.46`).
- **Function:** When you type a URL in your browser, DNS resolves it to an IP address.
- **Example:**
  When you visit `https://www.google.com`, DNS resolves the domain to an IP like `172.217.10.46`.

### **DHCP (Dynamic Host Configuration Protocol)**
- **Description:** Automatically assigns IP addresses to devices on a network.
- **Function:** Reduces the need for manual IP address configuration.
- **Example:**
  When you connect your laptop to a Wi-Fi network, DHCP assigns it an IP address like `192.168.1.5`.

### **FTP (File Transfer Protocol)**
- **Description:** A protocol for transferring files between computers on a network.
- **Common ports:** `21` for control commands, `20` for data transfer.
- **Example usage:**
  ```bash
  ftp ftp.example.com
  ```
  This connects to an FTP server where you can upload or download files.

### **SSH (Secure Shell)**
- **Description:** A protocol for secure remote access to devices over a network.
- **Common port:** `22`.
- **Example usage:**
  ```bash
  ssh user@server.com
  ```
  This connects securely to a remote server using the SSH protocol.

### **HTTP (HyperText Transfer Protocol)**
- **Description:** The protocol used for transferring web pages and data on the web.
- **Common port:** `80`.
- **Example:**
  When you visit `http://www.example.com`, your browser communicates with the web server over HTTP.

### **HTTPS (HyperText Transfer Protocol Secure)**
- **Description:** A secure version of HTTP, encrypting data between the client and server.
- **Common port:** `443`.
- **Example:**
  When you visit `https://www.example.com`, your browser uses HTTPS to secure the connection.

---

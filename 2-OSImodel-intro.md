# Computer Networking and the OSI Model
### History, Architecture, Working, Protocols, and Limitations

## Table of Contents

1. Introduction to Computer Networking
   - What is networking?
   - How two computers communicate
   - Unidirectional and bidirectional communication
   - Why protocols are needed

2. Evolution of Computer Networking
   - Early computer communication
   - ARPANET and packet switching
   - The problem of incompatible systems
   - IBM, DEC, and proprietary networking systems
   - Development of the OSI model
   - Development of TCP/IP
   - OSI and TCP/IP: how they became different approaches

3. What Is the OSI Model?
   - Definition and purpose
   - Why a layered model was needed
   - Features and benefits
   - Limitations

4. The Seven Layers of the OSI Model
   - Layer 7: Application
   - Layer 6: Presentation
   - Layer 5: Session
   - Layer 4: Transport
   - Layer 3: Network
   - Layer 2: Data Link
   - Layer 1: Physical

5. How Data Travels Through the OSI Layers
   - Encapsulation and decapsulation
   - Example: sending data from Computer A to Computer B
   - Data units at different layers
   - Devices operating at different layers

6. TCP/IP Model
   - What TCP/IP means
   - The four layers
   - Main protocols and their functions
   - How TCP/IP communication works
   - OSI versus TCP/IP

7. Important Networking Concepts
   - IP address and MAC address
   - Switch, router, and modem
   - Ports and sockets
   - Connection-oriented and connectionless communication
   - TCP and UDP
   - DNS, DHCP, and ARP

8. Features, Uses, and Limitations of Networking
   - Advantages
   - Common problems
   - Security and reliability

9. Conclusion

---

## 1. Introduction to Computer Networking

### What is networking?

Computer networking is the process of connecting two or more computers or devices so they can exchange data and share resources.

These resources may include files, printers, applications, internet connections, and storage. The devices can be connected through cables, fibre-optic links, or wireless signals such as Wi-Fi.

Networking is a part of **computer science and information technology**, particularly the field of computer networks and data communications.

For example, when Computer A sends a file to Computer B, the data must travel through a communication medium, reach the correct destination, and be interpreted correctly by the receiving computer.

### How two computers communicate

For two computers to communicate successfully, several things are required:

1. **Sender:** The computer that sends the data.
2. **Receiver:** The computer that receives the data.
3. **Transmission medium:** The path used to carry the data, such as Ethernet cable, fibre, or radio waves.
4. **Addressing:** Information that identifies the intended destination.
5. **Protocols:** Rules that define how data is formatted, transmitted, received, and interpreted.

Both computers must use compatible communication rules. If one computer sends information in a format that the other cannot understand, the communication will fail even if the physical connection is working.

### Unidirectional and bidirectional communication

Communication can be classified according to the direction in which information travels.

- **Simplex:** Data travels in one direction only. For example, a traditional broadcast transmission.
- **Half-duplex:** Both sides can transmit, but not at the same time. A walkie-talkie is a common example.
- **Full-duplex:** Both sides can transmit and receive at the same time. A typical modern Ethernet connection supports full-duplex operation.

These are communication modes, not stages in which all computer networks developed. Early systems already supported different forms of two-way communication.

### Why protocols are needed

A protocol is a set of rules used by devices to communicate.

Protocols define matters such as message format, addressing, error detection, delivery, and the response expected from another device.

For example:

- Ethernet helps devices communicate over a local wired network.
- IP provides logical addressing and routing between networks.
- TCP provides reliable, ordered delivery of a byte stream.
- HTTP defines how web clients and servers exchange web requests and responses.

Without agreed protocols, different computers and network devices would have difficulty communicating reliably.

## 2. Evolution of Computer Networking

Networking developed gradually as computers became more common and organizations needed to exchange information over greater distances.

### 2.1 Early computer communication

In the early days of computing, computers were often large, expensive machines used by universities, research laboratories, government departments, and businesses.

Communication was frequently handled through dedicated connections, terminals, or separate systems. Connecting computers from different manufacturers was difficult because hardware, software, and communication methods were not always compatible.

As computer use expanded, organizations wanted to share computing resources and exchange information without having to use the same type of computer.

### 2.2 ARPANET and packet switching — 1960s

During the 1960s, researchers explored ways to connect computers and share resources across different locations. One important idea was **packet switching**.

Instead of reserving a complete communication path for an entire message, packet switching divides data into smaller units called packets. These packets can travel through a network and be reassembled at the destination.

In 1969, ARPANET became operational with four initial nodes. It was funded by the U.S. Advanced Research Projects Agency (ARPA), which was renamed DARPA in 1972.

ARPANET connected research computers and allowed researchers to communicate and share resources. Packet switching also helped networks continue operating when a particular route or node became unavailable, provided an alternative route existed.

The common statement that ARPANET was built specifically to survive a nuclear attack is misleading. Resilience was relevant to networking research, but ARPANET's main purpose was not simply to create a nuclear-war-proof communication network.

**Why this development mattered:** It demonstrated that geographically separated computers could communicate through a packet-switched network rather than relying only on separate, dedicated communication paths.

### 2.3 The problem of incompatible systems

As networks expanded, another problem appeared: different organizations used different computers, hardware, operating systems, and networking technologies.

For example, IBM developed its Systems Network Architecture (SNA), while Digital Equipment Corporation (DEC) developed DECnet. These systems helped computers and equipment within their respective environments communicate, but connecting different networking systems could require special arrangements or gateways.

The problem was not that these systems could not communicate at all. Rather, there was no single universal approach that automatically made every vendor's system compatible with every other system.

Organizations therefore needed common standards that would allow equipment from different manufacturers to exchange data.

### 2.4 Development of the OSI model — 1977 onward

In 1977, the International Organization for Standardization (ISO) established a working group under its technical committee to develop an architecture for Open Systems Interconnection (OSI).

The main aim was to provide a common reference framework for networking and help standardize the functions and protocols needed for communication between different systems.

The OSI model separated network communication into seven layers. Each layer had a defined role and interacted with the layers above and below it.

The seven-layer architecture was developed during the late 1970s. A formal reference model was published in 1984 as **ISO 7498**, titled *Information Processing Systems — Open Systems Interconnection — Basic Reference Model*.

It is important to understand that the OSI model is a reference model, not one single protocol. The model describes how networking functions can be organized; separate standards and protocols define the actual details of communication.

### 2.5 Development of TCP/IP — 1970s and early 1980s

While OSI standardization was developing, researchers were also working on protocols that could connect different packet-switched networks.

In the early 1970s, Robert Kahn and Vinton Cerf worked on the design of protocols for communication across interconnected networks. Their work led to TCP and IP.

The goal was to allow different networks, even those using different underlying technologies, to communicate through a common internetworking system.

TCP/IP was adopted by ARPANET on 1 January 1983, replacing the earlier Network Control Program as the standard host communication protocol suite.

TCP/IP later became the foundation of the modern internet.

### 2.6 OSI and TCP/IP became different approaches

OSI and TCP/IP both address computer communication, but they developed in different ways.

- **OSI:** A formal reference model developed through international standardization. It divides communication into seven layers.
- **TCP/IP:** A practical protocol suite developed through research and implementation. It is commonly described using four layers.

The OSI model is widely used for teaching, design, and troubleshooting. TCP/IP is the protocol architecture used for communication across the internet.

The two models are related conceptually, but they are not identical, and their layers do not map together perfectly.

## 3. What Is the OSI Model?

OSI stands for **Open Systems Interconnection**.

The OSI model is a seven-layer reference model that describes the functions involved when data moves between networked devices.

It divides a complicated communication process into smaller parts. Each layer handles a particular group of tasks and provides services to the layer above it.

### Why was the OSI model needed?

Without a common framework, networking could become difficult to design and troubleshoot. A problem with a cable, a network address, or an application might all appear to the user as a failed connection, even though each problem has a different cause.

The OSI model helps organize these functions so they can be understood and investigated separately.

### Main features

- **Layered architecture:** Communication tasks are divided into seven layers.
- **Standardization:** Provides a common framework for discussing networking functions.
- **Interoperability goal:** Helps designers develop standards that allow different systems to communicate.
- **Modularity:** Changes to one layer may be possible without redesigning every other layer, provided interfaces remain compatible.
- **Troubleshooting:** Helps identify where a communication problem may be occurring.
- **Protocol independence:** The reference model does not require every network to use one particular protocol at every layer.

### Limitations

- The OSI model is theoretical; real networking implementations do not always follow its seven layers separately.
- Some functions overlap between layers or are handled differently by different protocols.
- It can be unnecessarily complicated when used to describe simple network operations.
- It does not itself provide a working internet connection or guarantee security, speed, or reliability.

## 4. The Seven Layers of the OSI Model

The seven layers are usually listed from Layer 7 down to Layer 1 when studying the model. When data is sent, it generally moves down the layers at the sender and up the layers at the receiver.

A common way to remember them, from Layer 7 to Layer 1, is:

**All People Seem To Need Data Processing**

| Layer | Name | Main responsibility |
|---|---|---|
| 7 | Application | Network services used by applications |
| 6 | Presentation | Data representation, encoding, compression, and encryption functions |
| 5 | Session | Establishing and managing logical communication sessions |
| 4 | Transport | End-to-end transport, segmentation, and delivery functions |
| 3 | Network | Logical addressing and routing between networks |
| 2 | Data Link | Local link delivery, frames, and media access |
| 1 | Physical | Transmission of raw bits through the medium |

### Layer 7: Application Layer

The Application layer is the layer closest to the user's network applications. It provides network-related services that applications use to communicate.

**Functions**
- Provides interfaces for network services.
- Supports web access, email, file transfer, and name resolution.
- Helps applications request information from remote systems.

**Examples of protocols**
- HTTP and HTTPS for web communication.
- SMTP for sending email.
- DNS for translating domain names into IP addresses.
- FTP for file transfer.

**How it works**

When a browser requests a webpage, it uses application-layer protocols to communicate with a web server. The request is then passed down the networking stack for delivery.

**Limitations**

The Application layer does not physically transmit the data or choose every route through the network. Lower layers perform the necessary transport, addressing, and transmission tasks.

Also, applications such as browsers and email clients are not themselves protocols. They use protocols to communicate.

### Layer 6: Presentation Layer

The Presentation layer concerns how data is represented so that the receiving system can interpret it correctly.

**Functions**
- Data format conversion.
- Character encoding.
- Data serialization and representation.
- Compression and decompression.
- Encryption and decryption functions, conceptually.

**Example**

One system may represent text using one encoding format and another system may use a different format. A compatible representation allows the receiver to interpret the information correctly.

Encryption and compression can also be discussed at this layer in the OSI model.

**Limitations**

In real TCP/IP networks, these functions are often implemented inside applications or libraries rather than in a separate Presentation layer. For example, TLS encryption is commonly associated with secure application communication and does not map neatly to one independent OSI layer.

### Layer 5: Session Layer

The Session layer is responsible, conceptually, for establishing, managing, and ending communication sessions between applications.

**Functions**
- Establishes and terminates logical sessions.
- Helps coordinate an ongoing exchange of information.
- May support synchronization points and recovery within a session.

**Example**

An application may need to maintain a logical interaction with a remote service while several requests and responses are exchanged.

**Limitations**

Many modern applications manage sessions themselves, using application protocols, tokens, or libraries. Therefore, session management is not always provided by a distinct network layer.

### Layer 4: Transport Layer

The Transport layer provides communication between processes running on different hosts. It can handle segmentation, reassembly, and transport-related reliability functions.

**Main functions**
- Divides data into smaller units when required.
- Uses port numbers to identify application processes.
- Supports reliability and ordered delivery when the protocol provides those features.
- May use flow control and congestion control.
- Reassembles data at the receiving end when appropriate.

**Main protocols**

**TCP (Transmission Control Protocol)** is connection-oriented. It provides a reliable, ordered byte stream using acknowledgements, retransmissions, sequencing, and flow and congestion control.

**UDP (User Datagram Protocol)** is connectionless and sends datagrams without guaranteeing delivery, order, or duplicate protection.

**Example**

When downloading a file over TCP, missing data can be retransmitted so the application receives the byte stream reliably. UDP is useful for applications that prefer low overhead or can handle loss themselves, such as many real-time audio and video systems.

**Limitations**

TCP's reliability can introduce additional delay and overhead. UDP does not provide the same delivery guarantees, so an application that requires reliability must implement suitable mechanisms itself.

TCP and UDP do not determine the route through the network. Routing is handled by the network layer.

### Layer 3: Network Layer

The Network layer handles logical addressing and moving packets between different networks.

**Main functions**
- Uses logical addresses such as IP addresses.
- Determines paths through interconnected networks.
- Forwards packets toward their destinations.
- Supports communication beyond a single local network.

**Main protocol**

IP (Internet Protocol) is the main example. IPv4 and IPv6 provide addressing and packet delivery across networks.

**Example**

If Computer A sends data to a computer on another network, routers examine the destination IP address and forward the packet toward the next network.

**Limitations**

IP provides best-effort delivery. It does not, by itself, guarantee that packets arrive, arrive only once, or arrive in the correct order. Protocols such as TCP can provide additional reliability when needed.

A router primarily operates at Layer 3, although real devices may also perform functions associated with other layers.

### Layer 2: Data Link Layer

The Data Link layer handles communication across a local link. It organizes data into frames and manages how devices use the link.

**Main functions**
- Framing.
- Local link addressing, commonly using MAC addresses on Ethernet and Wi-Fi.
- Error detection, such as frame checks.
- Media access control.
- Delivery between devices on the same local link.

**Examples**

Ethernet and Wi-Fi define important data-link functions.

**Example**

When Computer A sends data to another computer on the same Ethernet network, the data is placed into an Ethernet frame containing link-layer addressing information.

**Limitations**

A MAC address is generally used for delivery on a local link. It does not replace an IP address for routing across multiple networks.

Error detection can identify certain transmission errors, but it does not automatically repair every error or guarantee end-to-end delivery.

### Layer 1: Physical Layer

The Physical layer deals with transmitting raw bits through a physical or wireless medium.

**Main functions**
- Defines electrical, optical, or radio signaling characteristics.
- Specifies physical connectors and transmission requirements.
- Defines aspects of bit timing and signal transmission.
- Carries the bit stream over the communication medium.

**Examples**
- Copper Ethernet cabling.
- Fibre-optic cable.
- Radio signals used by Wi-Fi.
- Physical signaling and connectors specified by networking standards.

**Example**

When data travels through an Ethernet cable, the physical layer represents the transmitted bits using electrical signals according to the applicable standard.

**Limitations**

A working physical connection does not guarantee that the computers have valid addresses, compatible protocols, or functioning applications. A cable can be connected correctly while communication still fails at a higher layer.

## 5. How Data Travels Through the OSI Layers

### 5.1 Encapsulation

When an application sends data, each networking layer adds the information needed for its part of the communication. This process is called **encapsulation**.

A simplified example:

1. The Application layer creates the message.
2. The Transport layer adds transport information, such as TCP or UDP ports.
3. The Network layer adds IP addressing information.
4. The Data Link layer adds local-link framing information.
5. The Physical layer transmits the bits.

At the destination, the reverse process is called **decapsulation**. Each layer interprets and removes the information relevant to it before passing the remaining data upward.

### 5.2 Example: Computer A sends data to Computer B

Suppose Computer A sends a request to a website hosted on Computer B.

**At Computer A**
- The browser creates an application request.
- The transport protocol prepares the data for process-to-process communication.
- IP adds the source and destination IP addresses.
- Ethernet or Wi-Fi prepares a frame for the next link.
- The physical connection transmits the bits.

**Across the network**
- Switches forward frames within local networks.
- Routers examine IP information and forward packets between networks.
- At each routed hop, the local link-layer frame is normally replaced for the next link. The IP packet is forwarded, subject to normal network processing.

**At Computer B**
- The physical layer receives the signal.
- The data-link layer processes the frame.
- IP processes the packet.
- The transport layer delivers data to the appropriate application process.
- The application interprets the request and prepares a response.

The response travels back through the networking stack toward Computer A.

This example is simplified. Real communication may involve DNS lookups, encryption, multiple routers, proxies, firewalls, and several other protocols.

### 5.3 Data units at different layers

| Layer | Common data unit |
|---|---|
| Application, Presentation, Session | Data |
| Transport | Segment for TCP; datagram for UDP |
| Network | Packet or IP datagram |
| Data Link | Frame |
| Physical | Bits |

Terminology can vary by protocol, but this table is a useful starting point.

### 5.4 Devices and their typical layers

- **Hub or repeater:** Mainly Physical layer.
- **Ethernet switch:** Mainly Data Link layer.
- **Router:** Mainly Network layer.
- **Firewall:** May operate at several layers, depending on its design and features.
- **Gateway or proxy:** Can operate at higher layers when it understands application protocols.

These are common classifications, not strict rules for every device. Modern network equipment often combines several functions.

## 6. TCP/IP Model

### What is TCP/IP?

TCP/IP stands for **Transmission Control Protocol/Internet Protocol**. It refers to a suite of communication protocols used to connect devices across networks, including the internet.

The TCP/IP model describes the main functional layers of this protocol suite. A common teaching version uses four layers.

### The four layers of TCP/IP

| TCP/IP layer | Main function | Examples |
|---|---|---|
| Application | Network services used by applications | HTTP, DNS, SMTP, DHCP |
| Transport | Communication between application processes | TCP, UDP |
| Internet | Logical addressing and packet routing | IP, ICMP |
| Network Access / Link | Local-link delivery and physical transmission | Ethernet, Wi-Fi |

Some textbooks divide the bottom layer into separate Data Link and Physical layers, creating a five-layer teaching model. The four-layer version combines these functions into one Network Access or Link layer.

### 6.1 Application layer

This layer includes the functions that the OSI model discusses across its Application, Presentation, and Session layers.

It supports services such as web browsing, email, file transfer, and domain-name resolution.

Examples include HTTP, DNS, SMTP, and DHCP.

The exact work performed depends on the protocol and application. Encryption, for instance, is commonly provided by TLS libraries and application protocols.

### 6.2 Transport layer

This layer provides communication between application processes on different devices.

- TCP provides reliable, ordered delivery of a byte stream.
- UDP provides datagram delivery without guaranteeing reliability or ordering.

Port numbers help the receiving computer deliver data to the correct process.

The choice of transport protocol depends on the application's needs.

### 6.3 Internet layer

This layer is responsible for logical addressing and routing packets between networks.

IP allows a packet to travel across different underlying network technologies. Routers examine the destination IP address and forward packets toward their destinations.

IP itself does not guarantee successful delivery.

### 6.4 Network Access or Link layer

This layer covers local-link communication and the physical transmission of data. It includes functions such as framing, local addressing, and signaling.

Ethernet and Wi-Fi are common technologies associated with this layer, although each technology includes specifications covering more than one narrow OSI function.

## 7. Important Networking Concepts

### 7.1 IP address and MAC address

An **IP address** is a logical address used to identify an interface for communication across IP networks. Examples include IPv4 addresses and IPv6 addresses.

A **MAC address** is a link-layer address commonly used on Ethernet and Wi-Fi networks for local frame delivery.

Their roles are different:

- IP addresses help route packets between networks.
- MAC addresses help deliver frames over a local link.

When Computer A communicates with a remote computer, the destination IP address usually identifies the remote endpoint, while the frame's destination MAC address identifies the next local-link recipient, often the local router.

### 7.2 Switch, router, and modem

**Switch:** Connects devices within a local network and forwards frames based mainly on MAC addresses.

**Router:** Connects different IP networks and forwards packets according to routing information.

**Modem:** Modulates and demodulates signals for a particular communication technology, such as certain cable or DSL services. The exact role depends on the access technology.

Home devices often combine a router, switch, wireless access point, and modem or optical network interface into one unit, although these are separate functions.

### 7.3 Ports and sockets

A port number helps identify a particular application process or service on a device.

For example, HTTPS commonly uses TCP port 443. DNS commonly uses port 53, with both UDP and TCP used in different circumstances.

A network socket is an operating-system interface used by applications to send and receive network data. In common TCP/IP usage, a connection is identified by information such as source and destination IP addresses and port numbers, along with the transport protocol.

Port numbers are not physical connectors. They are logical identifiers used by networking software.

### 7.4 Connection-oriented and connectionless communication

**Connection-oriented communication:** A logical connection is established before data exchange. TCP is the common example.

**Connectionless communication:** Data is sent without establishing a transport connection first. UDP is the common example.

Connectionless does not mean that the network has no physical connection. It describes how the protocol handles communication.

### 7.5 DNS, DHCP, and ARP

**DNS (Domain Name System)** translates domain names, such as `example.com`, into records that can include IP addresses.

**DHCP (Dynamic Host Configuration Protocol)** allows a device to obtain network configuration automatically, often including an IP address, subnet information, a default gateway, and DNS server details.

**ARP (Address Resolution Protocol)** is used on IPv4 local networks to discover the link-layer address associated with an IPv4 address on the local link. IPv6 uses Neighbor Discovery rather than ARP.

These protocols solve different problems and work together to make network communication easier.

## 8. Features, Uses, and Limitations of Networking

### Advantages

- **Resource sharing:** Computers can share files, printers, and other resources.
- **Communication:** Users can exchange messages and information across distances.
- **Centralized management:** Organizations can manage accounts, policies, and resources centrally.
- **Scalability:** Networks can be expanded as the number of devices increases.
- **Remote access:** Users can reach services without being physically present at the server location.
- **Distributed services:** Applications can use resources hosted on different computers.

### Limitations and common problems

- **Security risks:** Poor configuration or vulnerable software can expose systems to attack.
- **Dependence on connectivity:** Network failures can interrupt access to remote resources.
- **Congestion:** Too much traffic can increase delay and reduce throughput.
- **Compatibility issues:** Devices may use different capabilities or configurations.
- **Cost:** Cabling, network equipment, maintenance, and security require resources.
- **Troubleshooting complexity:** A failure can occur at the physical, link, network, transport, or application level.

Networking standards improve compatibility, but they do not guarantee that every device will work together automatically. Correct configuration, compatible protocols, suitable hardware, and security measures are still required.

## 9. Conclusion

Computer networking developed because standalone computers were not enough for organizations that needed to exchange information and share resources. Packet switching and ARPANET demonstrated practical ways to connect computers over a network, while the growth of different vendors and technologies created a need for common communication standards.

The OSI model provided a seven-layer framework for understanding these communication tasks. TCP/IP developed as a practical protocol suite and became the foundation of the internet.

The main point is that communication does not depend on one component or protocol alone. It involves physical transmission, local-link delivery, logical addressing, transport services, and application-level rules. Understanding these layers makes it easier to understand how networks work and to identify where a problem may be occurring.
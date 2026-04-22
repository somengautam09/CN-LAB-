# Experiment 9: Transport Layer Simulation: UDP, TCP, and SCTP Comparison

**Institution:** K.R. Mangalam University

---

## Objective
Implement a transport layer simulation to demonstrate process-to-process communication using UDP, TCP, and SCTP protocols, and compare them in terms of connection establishment and data transmission.

## Theory

* **TCP (Transmission Control Protocol):** A connection-oriented, reliable protocol that guarantees delivery. It establishes a connection via a **3-way handshake (SYN, SYN-ACK, ACK)** before sending data, ensuring the receiver is ready.
* **UDP (User Datagram Protocol):** A connectionless, unreliable protocol. It sends data immediately without verifying readiness or guaranteeing delivery, making it faster with less overhead.
* **SCTP (Stream Control Transmission Protocol):** A message-oriented protocol that combines features of both TCP and UDP, providing multi-homing and multi-streaming capabilities.



---

## Network Topology
![Transport Layer Topology](./screenshots/topology.jpeg)  
*(Above: A topology with client PCs and a Server to simulate process-to-process communication).*

---

## Step-by-step Procedure

1. **Topology Design:** Designed a network topology with PCs and a Server connected via a Switch.
2. **IP Addressing:** Assigned static IP Addresses to the PCs and the Server.
3. **TCP Simulation:** Configured an HTTP service on the Server. Accessed the server via the PC's web browser to generate TCP traffic.
4. **UDP Simulation:** Configured a DNS service on the Server. Ran a domain query from the PC to generate UDP traffic.
5. **Traffic Filtering:** Switched to Simulation Mode and filtered the Event List to show only TCP and UDP packets.
6. **Header Inspection:** Clicked on the respective Protocol Data Units (PDUs) to inspect the transport layer headers, port numbers, and connection flags.

---

## Configuration Commands
**N/A** (Configurations handled via the Server's Service tab and PC desktop applications).

---

## Observations / Results
![TCP Handshake Headers](./screenshots/output.jpeg)  
* **TCP:** Inspection of the TCP PDUs revealed the explicit 3-way handshake process establishing the connection prior to the HTTP data payload transfer.
* **UDP:** The UDP PDUs were transmitted immediately without any prior handshake or acknowledgment mechanisms, showing a smaller header size.

---

## Conclusion
The simulation successfully demonstrated the behavioral differences between transport layer protocols. TCP's connection-oriented features provide necessary reliability for applications like web browsing, whereas UDP's lack of overhead is ideal for fast, connectionless queries like DNS.

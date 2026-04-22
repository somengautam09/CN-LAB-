# Experiment 4: Error Detection and Correction Mechanisms Using Block Coding and CRC

**Institution:** K.R. Mangalam University  


---

## Objective
Implement error detection and correction mechanisms using block coding and Cyclic Redundancy Check (CRC), and simulate a communication system to demonstrate how errors are detected and corrected during data transmission.

## Theory

### Block Coding
Data is divided into discrete blocks, and redundant parity bits are appended to detect and correct single-bit errors. By adding these extra bits, the receiver can verify if the data received matches the data sent.

### CRC (Cyclic Redundancy Check)
A mathematical division process used to detect accidental changes to raw data. The sender calculates a check value based on binary division and appends it to the frame as the **Frame Check Sequence (FCS)**.

---

## Network Topology
![Topology](./screenshots/topology.jpeg)
*(Above: A simple network topology consisting of End Devices and a Switch to test data transmission and frame headers).*

---

## Step-by-step Procedure

1. **Topology Setup:** Created a new network topology using End Devices (PCs) and a central Switch.
2. **IP Addressing:** Assigned static IP addresses to the PCs.
3. **Documentation:** Used the "Add Note" feature in Packet Tracer to document the theoretical application of block coding and parity bits for error checking within the workspace.
4. **Traffic Generation:** Generated ICMP (ping) traffic using the **Add Simple PDU** tool to simulate data transmission.
5. **Packet Inspection:** Switched to **Simulation Mode** to observe the packet headers, specifically inspecting the Ethernet II frame to view the CRC/FCS trailer used for error detection.

---

## Configuration Commands
**N/A** (This experiment relies on packet inspection rather than CLI configuration).

---

## Observations / Results
![PDU Details](./screenshots/output.jpeg)
* Inspected the outbound PDU details in Simulation Mode.
* While physical bit-flipping isn't manually configurable in the GUI, the simulation allowed for the visualization of the FCS trailer, confirming the implementation of CRC at the data link layer.

---

## Conclusion
Successfully simulated a communication system demonstrating error detection concepts. The experiment highlighted the practical application of CRC in standard Ethernet frames to ensure data integrity over a network.

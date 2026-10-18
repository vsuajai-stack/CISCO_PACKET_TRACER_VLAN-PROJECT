# Secure Office Network Implementation using VLANs & Router-on-a-Stick

An intermediate-level computer networking project designed, configured, and tested in **Cisco Packet Tracer**. 

## 🌐 Project Overview
This project addresses the network management and security limitations of a traditional flat network architecture. By implementing logical segmentation across multiple departments, broadcast domains are constrained, and inter-departmental communication is securely managed through a Layer 3 router.

## 🛠️ Network Architecture & Design
* **Switches:** 2 x Cisco 2960 Switches
* **Router:** 1 x Cisco Router (configured with 802.1Q subinterfaces)
* **End Devices:** 6 PCs distributed across departments:
  * **HR Department (VLAN 10):** `192.168.10.0/24`
  * **IT Department (VLAN 20):** `192.168.20.0/24`
  * **Finance Department (VLAN 30):** `192.168.30.0/24`

## ⚙️ Key Configurations
* **VLAN Creation & Assignment:** Configured VLANs 10, 20, and 30 on both switches, assigning access ports dynamically to respective department endpoints.
* **Trunking:** Enabled IEEE 802.1Q trunking on switch-to-switch links and router-to-switch links to handle multi-VLAN frame propagation.
* **Router-on-a-Stick:** Configured physical router interface `GigabitEthernet0/0` with logical subinterfaces (`.10`, `.20`, `.30`), encapsulating them with dot1Q tags and assigning respective default gateway IP addresses.

## 🔍 Verification & Testing
Network functionality was successfully verified using standard Cisco IOS commands:
* `show vlan brief`
* `show interfaces trunk`
* `show interfaces status`
* `show mac address-table`
* `show ip interface brief`
* `show ip route`
* `show running-config`

## 📁 Repository Contents
* `Jai_VLAN_Routing_Project.pkt`: The fully configured Cisco Packet Tracer simulation file.
* `JAI_VLAN_Routing_Project_Report_2.docx`: The complete professional project report containing topology diagrams, CLI configuration scripts, screenshot proofs, simulation analysis, and verification results.

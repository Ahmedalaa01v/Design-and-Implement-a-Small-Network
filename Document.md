# University Network Configuration Project

## Project Overview
This project is a **university network infrastructure** simulation that includes VLAN configurations, DHCP setup, inter-networking, and routing using **Cisco networking devices**. The network is divided into multiple campuses, each with its own VLAN and routing setup, including a cloud-based server connection.

## Technologies Used
- **Cisco Packet Tracer** (or actual Cisco devices)
- **Routing Protocols:** RIP
- **Switching & VLANs:** Trunking, Access Ports
- **DHCP Configuration**
- **IP Addressing & Subnetting**
- **Network Security Practices**

## Network Setup Steps

1. **VLAN Configuration:**
   - Assign VLANs to each switch.

2. **Multi-Switch Interface Configuration:**
   - Define which interfaces connect to specific VLANs.

3. **Trunking on Multi-Switch:**
   - Configure trunk ports on the switch connected to the router.

4. **Router IP Address Assignment:**
   - Assign IP addresses to each network.

5. **Enable DHCP for Each VLAN/Network:**
   ```shell
   service dhcp
   ip dhcp pool managepool
   network 192.168.1.0
   default-router 192.168.1.1
   dns-server 8.8.8.8
   ```

6. **Enable DHCP on Each Device:**
   - Configure each connected device to obtain an IP address via DHCP.

7. **Assign IPs to Serial Interfaces:**
   - Configure IP addresses for inter-router communication.

8. **Replicate Configurations for Small Campus:**
   - Apply similar configurations to the smaller campus network.

9. **Cloud Network Configuration:**
   - Assign network IPs and configure the server.

10. **RIP Configuration on the Main Campus Router:**
   ```shell
   router rip
   network 192.168.6.0
   network 192.168.7.0
   network 192.168.8.0
   ```

11. **RIP Configuration on the Secondary Router:**
   - Apply RIP routing on the second router as well.

## Recommendations & Future Improvements

### Recommendations:
- **Use OSPF Instead of RIP:**
  - RIP is a basic routing protocol but may not be efficient for large-scale networks. **OSPF (Open Shortest Path First)** would improve scalability and convergence time.

- **Implement VLAN Security Measures:**
  - Use **VLAN Access Control Lists (ACLs)** to restrict unnecessary inter-VLAN traffic.
  - Enable **Port Security** to prevent unauthorized device connections.

- **Enable Network Redundancy:**
  - Use protocols like **HSRP (Hot Standby Router Protocol)** or **VRRP** to improve router failover capabilities.

### Future Improvements:
- **Integrate Network Monitoring Tools:**
  - Implement **SNMP (Simple Network Management Protocol)** for better network monitoring.
  - Use tools like **Wireshark** to analyze traffic patterns and detect anomalies.

- **Implement IPv6 Support:**
  - Future-proof the network by transitioning from IPv4 to IPv6.

- **Enhance Security Features:**
  - Set up **802.1X authentication** to restrict unauthorized device access.
  - Configure **firewall rules** to block external threats.

## Conclusion
This project successfully demonstrates a **multi-campus network setup** with VLANs, DHCP, and routing configurations. The next steps involve **enhancing security, optimizing performance, and expanding scalability** to make the network enterprise-ready.

---
📌 *For any questions or contributions, feel free to submit a pull request!* 🚀

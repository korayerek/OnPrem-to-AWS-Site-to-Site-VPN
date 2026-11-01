# Screenshot index

All screenshots document the actual build sequence. Some early pictures intentionally show intermediate states, including tunnels Down and an initially empty private return-route table.

| No. | Screenshot | What it shows |
|---:|---|---|
| 01 | [01-Onprem-Network-Topology.png](../screenshots/01-Onprem-Network-Topology.png) | Initial GNS3 topology before adding bridged Cloud/eth2. |
| 02 | [02-Vyos-VLAN-Interfaces.png](../screenshots/02-Vyos-VLAN-Interfaces.png) | Early VyOS interface status: VLAN gateways 10/20/30, no eth2 address yet. |
| 03 | [03-Switch-VLAN-Configuration.png](../screenshots/03-Switch-VLAN-Configuration.png) | Switch port 0 uses 802.1Q; ports 1–3 belong to VLANs 10, 20, 30. |
| 04 | [04-Inter-VLAN-Routing-Test.png](../screenshots/04-Inter-VLAN-Routing-Test.png) | Inter-VLAN pings from IT PC (VLAN 20) to Users and Servers. |
| 05 | [05-Source-NAT-Configuration.png](../screenshots/05-Source-NAT-Configuration.png) | Source NAT/masquerade rules 100, 110, 120 via eth0. |
| 06 | [06-VLAN-Internet-Connectivity-Test.png](../screenshots/06-VLAN-Internet-Connectivity-Test.png) | Internet ping tests from all three VPCS hosts. |
| 07 | [07-VyOS-WAN-Static-IP.png](../screenshots/07-VyOS-WAN-Static-IP.png) | Static 192.168.1.10/24 on VyOS eth2 after physical bridge setup. |
| 08 | [08-VyOS-Internet-Connectivity.png](../screenshots/08-VyOS-Internet-Connectivity.png) | VyOS ping to AT&T gateway and external IP. |
| 09 | [09-ATT-Router-IPsec-Port-Forwarding.png](../screenshots/09-ATT-Router-IPsec-Port-Forwarding.png) | AT&T home router UDP 500/4500 port-forward rules. |
| 10 | [10-ATT-Router-VyOS-Device-Verification.png](../screenshots/10-ATT-Router-VyOS-Device-Verification.png) | Physical LAN identifies the bridged/VyOS device at 192.168.1.10. |
| 11 | [11-AWS-VPC-Configuration.png](../screenshots/11-AWS-VPC-Configuration.png) | Create VPC: 10.100.0.0/16, IPv4 only. |
| 12 | [12-AWS-VPC-Created.png](../screenshots/12-AWS-VPC-Created.png) | VPC creation success and CIDR confirmation. |
| 13 | [13-AWS-Public-Private-Subnets.png](../screenshots/13-AWS-Public-Private-Subnets.png) | Public subnet 10.100.1.0/24 and private subnet 10.100.2.0/24. |
| 14 | [14-AWS-Internet-Gateway-Attached.png](../screenshots/14-AWS-Internet-Gateway-Attached.png) | Internet Gateway attached to custom VPC. |
| 15 | [15-AWS-Public-Route-Table-Configuration.png](../screenshots/15-AWS-Public-Route-Table-Configuration.png) | Public route table associated with public subnet; default route to IGW. |
| 16 | [16-AWS-Private-Route-Table-Configuration.png](../screenshots/16-AWS-Private-Route-Table-Configuration.png) | Initial private route table, before VPN return routes were added. |
| 17 | [17-AWS-Virtual-Private-Gateway-Attached.png](../screenshots/17-AWS-Virtual-Private-Gateway-Attached.png) | AWS Virtual Private Gateway attached to VPC. |
| 18 | [18-AWS-Customer-Gateway-Created.png](../screenshots/18-AWS-Customer-Gateway-Created.png) | AWS Customer Gateway created with ISP-facing address (redacted). |
| 19 | [19-AWS-Site-to-Site-VPN-Created.png](../screenshots/19-AWS-Site-to-Site-VPN-Created.png) | AWS Site-to-Site VPN connection created and available (not a tunnel UP claim). |
| 20 | [20-AWS-Site-to-Site-VPN-Details.png](../screenshots/20-AWS-Site-to-Site-VPN-Details.png) | VPN connection details confirm static routing, CGW, and VGW. |
| 21 | [21-AWS-VPN-Tunnel-Status-Before-Configuration.png](../screenshots/21-AWS-VPN-Tunnel-Status-Before-Configuration.png) | Both AWS IPsec tunnels Down before customer-side configuration. |
| 22 | [22-AWS-Site-to-Site-VPN-Tunnel1-UP.png](../screenshots/22-AWS-Site-to-Site-VPN-Tunnel1-UP.png) | AWS Tunnel 1 Up while Tunnel 2 still Down. |
| 23 | [23-AWS-Private-EC2-Instance-Running.png](../screenshots/23-AWS-Private-EC2-Instance-Running.png) | Private-subnet EC2 test instance with private IP 10.100.2.39. |
| 24 | [24-VyOS-IPsec-VPN-Tunnel1-UP.png](../screenshots/24-VyOS-IPsec-VPN-Tunnel1-UP.png) | VyOS Tunnel 1 IPsec SA Up before recorded data transfer. |
| 25 | [25-VyOS-AWS-Static-Route-Vti0.png](../screenshots/25-VyOS-AWS-Static-Route-Vti0.png) | Route lookup shifts from default gateway to the vti0 VPC route. |
| 26 | [26-AWS-Private-Route-Table-Configured.png](../screenshots/26-AWS-Private-Route-Table-Configured.png) | AWS private route table now has return routes to all three VLAN /24s via VGW. |
| 27 | [27-VyOS-to-AWS-EC2-VPN-Ping-Success.png](../screenshots/27-VyOS-to-AWS-EC2-VPN-Ping-Success.png) | VyOS source 192.168.10.1 can ping EC2 10.100.2.39 5/5. |
| 28 | [28-PC1-VLAN10-to-AWS-EC2-VPN-Ping-Success.png](../screenshots/28-PC1-VLAN10-to-AWS-EC2-VPN-Ping-Success.png) | PC1 Users VLAN 10 reaches AWS private EC2. |
| 29 | [29-PC2-VLAN20-to-AWS-EC2-VPN-Ping-Success.png](../screenshots/29-PC2-VLAN20-to-AWS-EC2-VPN-Ping-Success.png) | PC2 IT VLAN 20 reaches AWS private EC2. |
| 30 | [30-PC3-VLAN30-to-AWS-EC2-VPN-Ping-Success.png](../screenshots/30-PC3-VLAN30-to-AWS-EC2-VPN-Ping-Success.png) | PC3 Servers VLAN 30 reaches AWS private EC2. |
| 31 | [31-VyOS-IPsec-VPN-Encrypted-Traffic-Verification.png](../screenshots/31-VyOS-IPsec-VPN-Encrypted-Traffic-Verification.png) | Nonzero IPsec SA encrypted traffic bytes and packets. |
| 32 | [32-VyOS-Both-AWS-IPsec-Tunnels-UP.png](../screenshots/32-VyOS-Both-AWS-IPsec-Tunnels-UP.png) | Both VyOS tunnel IPsec SAs Up. |
| 33 | [33-VyOS-Primary-Backup-Static-Routes.png](../screenshots/33-VyOS-Primary-Backup-Static-Routes.png) | Primary vti0 route distance 1 installed; backup vti1 distance 20 standby. |
| 34 | [34-AWS-Tunnel2-VTI-Ping-Success.png](../screenshots/34-AWS-Tunnel2-VTI-Ping-Success.png) | Tunnel 2 inside peer 169.254.115.69 responds 5/5. |
| 35 | [35-AWS-VPN-Primary-to-Backup-Failover-Verification.png](../screenshots/35-AWS-VPN-Primary-to-Backup-Failover-Verification.png) | Manual disable of vti0 static route causes vti1 to become installed. |
| 36 | [36-AWS-VPN-Backup-Tunnel-EC2-Ping-Success.png](../screenshots/36-AWS-VPN-Backup-Tunnel-EC2-Ping-Success.png) | EC2 ping 5/5 while backup vti1 is the installed path. |
| 37 | [37-AWS-VPN-Primary-Tunnel-Restored.png](../screenshots/37-AWS-VPN-Primary-Tunnel-Restored.png) | Primary static route restored; vti0 again installed as best route. |
| 38 | [38-AWS-Site-to-Site-VPN-Both-Tunnels-UP.png](../screenshots/38-AWS-Site-to-Site-VPN-Both-Tunnels-UP.png) | AWS final view: Tunnel 1 and Tunnel 2 both Up. |
| 39 | [39-Final-OnPrem-GNS3-Network-Topology.png](../screenshots/39-Final-OnPrem-GNS3-Network-Topology.png) | Completed GNS3 on-prem topology with Cloud1/eth2. |

**Privacy:** Home public IPv4, Wi-Fi network name, and AWS account number have been masked in selected public copies. No VPN pre-shared keys are included.

# My Hotel network project 
<img width="960" height="511" alt="Hotel Network" src="https://github.com/user-attachments/assets/e1b3fe29-23d0-4089-8445-21519a5d7701" />

# Specifications:
- ROUTING & CONNECTIVITY: Three routers located in the IT server room, interconnected via serial DCE cables using the 10.10.10.0/30, 10.10.10.4/30, 10.10.10.8/30 subnets.
  
- VLAN SEGMENTATION: Each department is assigned a unique VLAN and subnet to manage broadcast traffic and improve security:
- 1st Floor:Reception(VLAN 80), Store(VLAN 70), Logistics (VLAN 60).
- 2nd Floor:Finance (VLAN 50), HR (VLAN 40), Sales (VLAN 30).
- 3rd Floor:Admin (VLAN 20), IT (VLAN 10).
  
- INFRASTRUCTURE: Each floor utilizes a dedicated switch, with integrated WI-FI access for mobile devices and departmental Printers.

# Technical Implementation
- DYNAMIC ADDRESSING: All devices utilize DHCP, with routers configured as the primary DHCP servers for their respective networks.
  
- ROUTING PROTOCOL: OSPF was implemented as the interior gateway protocol to ensure full reachability between all departments.
  
- NETWORK SECURITY & MANAGEMENT:
- REMOTE ACCESS: SSH is configured on all routers to ensure secure administrative access.
- PORT SECURITY: Implemented on the IT department switch port fa0/1. Used the "sticky" MAC address method with a shutdown violation mode to restrict access specifically to the authorized "Test-PC".

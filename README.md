# Config-Lab-Syslog-2.

My Config Lab: Syslog 2 VIA Cisco Packet Tracer.

Figure 1: Two Routers with IP Addresses.

Initial Configuration.

Examples 1 and 2 show the beginning configuration state of R1 and R2.

hostname R1
!
interface GigabitEthernet0/1
 ip address 172.30.180.193 255.255.255.252
 no shutdown
!
interface GigabitEthernet0/2
 no shutdown
!
router ospf 1
 network 0.0.0.0 255.255.255.255 area 0

Example 1: R1 Config

hostname R2
!
interface GigabitEthernet0/1
 ip address 10.10.10.1 255.255.255.0
 no shutdown
!
interface GigabitEthernet0/2
 ip address 172.30.180.194 255.255.255.252
 no shutdown
!
router ospf 1
 network 0.0.0.0 255.255.255.255 area 0

Lab Answers Configurations:

no logging buffered
!
logging host 10.10.10.100
logging trap critical

no logging buffered 
!
logging host 10.10.10.100
logging trap 2

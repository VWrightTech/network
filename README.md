<h2>👨‍💻 CCNA Static Routing</h2>
<img src="https://i.imgur.com/HuV4YOi.png" height="250%" width="250%">

<br />
- Topology
<br />
Enable Interface of R3, R3 And R3 (Serial and Fast Ethernet)
<br />
Router 1
<br />
Router>Enable
<br />
Router# Configure Terminal
<br />
Router (Config)#hostname R1
<br />
R1 (Config)# interface Se1/0
<br />
R1 (Config-if)# ip address 10.0.0.1 255.0.0.0
<br />
R1 (Config-if)# clock rate 64000
<br />
R1 (Config-if)# bandwidth 64
<br />
R1 (Config-if)# no shutdown
<br />
R1 (Config-if)# int fa0/0
<br />
R1 (Config-if)# ip add 192.168.0.1 255.255.255.0
<br />
R1 (Config-if)# no sh
<br />
R1 (Config-if)# do show ip interface brief
<br />
R1 (Config-if)# ctrl + z
<br />
R1#
<br />
Router 2
<br />
Router>Enable
<br />
Router# Conf t
<br />
Router (Config)#hostname R2
<br />
R2 (Config)#int se1/0
<br />
R2 (Config)#ip add 10.0.0.2 255.0.0.0
<br />
R2 (Config)#no sh
<br />
R2 (Config-if)#int se1/1
<br />
R2 (Config-if)#ip add 20.0.0.1 255.0.0.0
<br />
R2 (Config-if)#clock rate 64000
<br />
R2 (Config-if)#bandwidth 64
<br />
R2 (Config-if)#no sh
<br />
R2 (Config-if)#int fa0/0
<br />
R2 (Config-if)#ip add 172.168.0.1 255.255.0.0
<br />
R2 (Config-if)#no sh
<br />
R2 (Config-if) #^Z
<br />
R2#
<br />
Router 3
<br />
Router>Enable
<br />
Router# Configure Terminal
<br />
Router (Config)#hostname R3
<br />
R3 (Config)# interface Se1/0
<br />
R3 (Config-if)# ip address 20.0.0.2 255.0.0.0
<br />
R3 (Config-if)#no sh
<br />
R3 (Config-if)#int fa0/0
<br />
R3 (Config-if)#ip add 125.168.0.1 255.0.0.0
<br />
R3 (Config-if)#no sh
<br />
R3 (Config-if)#do show ip int br
<br />
R3 (Config-if)#^Z

<h2>👨‍💻 CCNA Static Routing</h2>
<img src="https://i.imgur.com/HuV4YOi.png" height="250%" width="250%">

<br />
<b> Topology </b>
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
<br />
<br />
<br />
<br />
<b>Assign IP Address in All PC</b>
<br />
<b>Step 1 Click on PC , Go to Desktop and click , Click on IP configuration</b>
<br />
<br />
<br />
<img src="https://i.imgur.com/C2l4Xzf.png" height="250%" width="250%"
<br />

<br />
R1
<br />
PC 1 PC 2
<br />
Ip address 192.168.0.2 Ip address 192.168.0.3
<br />
Subnet Mark 255.255.255.0 Subnet Mark 255.255.255.0
<br />
Default Gateway 192.168.0.1 Default Gateway 192.168.0.1
<br />
R2
<br />
PC 3 PC 4
<br />
Ip address 172.168.0.2 Ip address 172.168.0.3
<br />
Subnet Mark 255.255.0.0 Subnet Mark 255.255.0.0
<br />
Default Gateway172.168.0.1 Default Gateway 172.168.0.1
<br />
R3
<br />
PC 5 PC 6
<br />
Ip address 125.168.0.2 Ip address 125.168.0.3
<br />
Subnet Mark 255.0.0.0 Subnet Mark 255.0.0.0
<br />
Default Gateway 125.168.0.1 Default Gateway 125.168.0.1
<br />
Enable or Configure static Router
<br />
R3
<br />
Syntax :- IP route <remote network> <subnet mark> next hop IP
<br />
R1>enable
<br />
R1#conf t
<br />
R1(config)#ip route 172.168.0.0 255.255.0.0 10.0.0.2
<br />
R1(config)#ip route 20.0.0.0 255.255.0.0 10.0.0.2
<br />
R1(config)#ip route 125.168.0.0 255.0.0.0 10.0.0.2
<br />
R1(config)#^Z
<br />
R1#
<br />
write
<br />
Building configuration...
<br />
[OK]
<br />
R1#
<br />
R2
<br />
R2>enable
<br />
R2#conf t
<br />
R2(config)#ip route 192.168.0.0 255.255.255.0 10.0.0.1
<br />
R2(config)#ip route 125.168.0.0 255.0.0.0 20.0.0.2
<br />
R2(config)#^Z
<br />
R2#
<br />
write
<br />
Building configuration...
<br />
[OK]
<br />
R2#
<br />
R3
<br />
R3>enable
<br />
R3#conf t
<br />
R3(config)#ip route 172.168.0.0 255.255.0.0 20.0.0.1
<br />
R3(config)#ip route 192.168.0.0 255.255.255.0 20.0.0.1
<br />
R3(config)#ip route 10.0.0.0 255.0.0.0 20.0.0.1
<br />
R3(config)#^Z
<br />
R3#
<br />
write
<br />
Building configuration...
<br />
[OK]
R3#

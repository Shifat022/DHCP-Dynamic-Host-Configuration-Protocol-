Router(config)#interface FastEthernet0/0 
Router(config-if)#ip address 192.168.10.1 255.255.255.0 
Router(config-if)#no shutdown 

Router(config)#ip dhcp excluded-address 192.168.10.1 192.168.10.10 
Router(config)#ip dhcp excluded-address 192.168.10.254 
Router(config)#ip dhcp pool LAN_POOL_CSE
Router(dhcp-config)#network 192.168.10.0 255.255.255.0
Router(dhcp-config)#default-router 192.168.10.1 

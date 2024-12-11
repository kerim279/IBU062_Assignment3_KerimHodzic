Routers
- Router 1 (Model: ISR4331)
- Interface GigabitEthernet 0/0/0
- Interface GigabitEthernet 0/0/1
- Interface GigabitEthernet 0/0/2

Switches
- Switch1 (Model: 2960-24TT)
- Connected to Router's GigabitEthernet 0/0/0, GigabitEthernet 0/0/1 and GigabitEthernet 0/0/2
- Switch2 (Model: 2960-24TT)
- Connected to Router's GigabitEthernet 0/0/0, GigabitEthernet 0/0/1 and GigabitEthernet 0/0/2

Hosts
- Switch1:
Server0 (Model: Server-PT)
    IP Adress: 168.90.0.2
Laptop0 (Model: Laptop-PT)
    IP Adress: 198.90.0.4
PC0 (Model: PC-PT)
    IP Adress: 168.90.0.3
PC1 (Model: PC-PT)
    IP Adress: 168.90.0.5
PC3 (Model: PC-PT)
    IP Address: 168.90.0.6

-Switch2:
Server1 (Model: Server-PT)
    IP Adress: 210.3.14.3
Server2 (Model: Server-PT)
    IP Adress: 210.3.14.2
PC2 (Model: PC-PT)
    IP Adress: 210.3.14.4
PC4 (Model: PC-PT)
    IP Address: 210.3.14.5


Commands used to set up DHCP on the Router:
- "enable" and "configure terminal": To establish terminal configuration in Command Line Interface on the Router.
- ip dhcp pool Pool1, Pool2: To set up pools

To set up network
- network 168.90.0.0 255.255.0.0
default-router  168.90.0.1

- To configure the Router Interface
interface GigabitEthernet 0/0/0
ip address 168.90.0.1
no shutdown

interface GigabitEthernet 0/0/1
ip address 210.3.14.1
no shutdown

interface GigabitEthernet 0/0/2
ip address 168.90.1.1
no shutdown

- To verify the Configuration
show ip dhcp binding
ipconfig
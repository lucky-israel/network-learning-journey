# static routing

 configured and siumulated a  static route 

#R1
int g0/1 - 192.168.1.254
int g0/0 - 192.168.12.1
ip route 192.168.13.0 255.255.255.0
ip route 192.168.3.0 255.255.255.0 192.168.12.2

#R2
int g0/0 - 192.168.12.2
int g0/1 - 192.168.13.2
ip route 192.168.3.0 255.255.255.0 192.168.13.3
ip route 192.168.1.0 255.255.255.0 192.168.12.1


#R3
int g0/0 192.168.13.3
int g0/1 - 192.168.3.254
ip route 192.168.12.0 255.255.255.0 192.168.13.2
ip route 192.168.1.0 255.255.255.0 192.168.13.2


![Image Alt](https://github.com/lucky-israel/network-learning-journey/blob/main/routing/static/01_static%20rooute%20config.jpg)

PC 0 is able to ping and communicate PC 1

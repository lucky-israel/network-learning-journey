I was simulating a network, after designing and configuring the network 
PC-SW2-SW1-Main access layer switch-l2-l3(gateway)

The PC connected to SW2 in VLAN 159 could not ping the default gateway (10.100.159.1) hosted on the L3 switch SVI. The network consisted of multiple access, distribution, and core switches carrying VLAN 159.

for network aspect :

VLAN 159 is not consistently allowed on trunks

Misconfiguration of access vs trunk ports

Mixing native VLAN (3) and VLAN 1 across switches

vlan ID across the network where not active

Misuse of VLAN 1 for management IP

while for the security aspect, because I tend to build a secure network that protects against VLAN double tagging:
VLAN 1 should not be used as a user VLAN.

what i learnt new: 
I fully grasped the difference and usage of trunk(allowed and native) and access port.
Switches uplinks are meant to be trunked whether carrying multiple traffic or not, because a good network design must be scalable and secure.


This lab reinforced that most enterprise network failures are caused by Layer 2 misconfigurations rather than routing issues. Consistent VLAN design and trunk policies are critical for scalable and secure network architectures.



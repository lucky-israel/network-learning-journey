In this section i configured OPSF lAB ,with prior similar environment but different configuration .

i use command sample:
R1#config t
R1(config)#int g0/0
R1(config-if)#ip ospf 1 area 0


I encountered some issue with PC can't ping any R in a R1-R2-R4-SW-PC or R1-R3-R4-SW-PC topology,

so i retraced my system and found some issues with router-id it was taking interfcae ip and also reconfigured the OSP4 on R4.

<img width="1915" height="756" alt="image" src="https://github.com/user-attachments/assets/32e0e8d7-dc0b-4002-98e7-336f79a6429b" />


<img width="1905" height="783" alt="image" src="https://github.com/user-attachments/assets/a7ab8896-b52e-4150-9eb6-11de1f342195" />

Practicing Spanning tree and Root Guard


Spanning tree lab simulatino between service provider and customer - 

Using root guard to prevent topology change and superior BPDUS from Service provider

<img width="1908" height="678" alt="image" src="https://github.com/user-attachments/assets/f5fba499-5898-445c-864e-77f01db51681" />



LAB CONFIG 

SW0- en
config
spannig-tree vlan1 priority 0



SW4 -en
config
spannig-tree vlan1 priority 0


<img width="1909" height="726" alt="image" src="https://github.com/user-attachments/assets/dd5e5f77-8ff3-4abb-8538-4cb0121585a8" />


Topology Changed due to Supereior BPDUs - The mac address of teh customer edge

Root bridge has moved form Service provider to Customer
<img width="1360" height="480" alt="image" src="https://github.com/user-attachments/assets/95fddc26-4c0c-4513-a469-1b37ef8cd4fb" />


<img width="1916" height="727" alt="image" src="https://github.com/user-attachments/assets/ee0e862f-62c2-4978-bbab-3e413009f270" />

Implementing Root Guard on Sw 1 and SW2 (int f0/3) to prevent such issue - port blocked .

<img width="1908" height="736" alt="image" src="https://github.com/user-attachments/assets/0aa58bae-817b-4f9f-ab9e-dd7f3502b632" />



Note : To Resolved the port blocking issue tell Customers to increase their switch priority .

<img width="1919" height="700" alt="image" src="https://github.com/user-attachments/assets/ee6bc246-06ba-4b0c-8862-f1c74a5ec113" />


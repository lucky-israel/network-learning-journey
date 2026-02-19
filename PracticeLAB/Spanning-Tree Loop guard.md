HI,

In this lab i am practicing and simulating loop guard  .

Sw 1

<img width="1814" height="889" alt="image" src="https://github.com/user-attachments/assets/4c5ca5b2-3e21-48ae-88a5-8689ce481941" />


SW 2
<img width="1802" height="916" alt="image" src="https://github.com/user-attachments/assets/db8644bf-c9e3-4fc2-a42b-974d6f7f5d90" />

SW 3

<img width="1807" height="952" alt="image" src="https://github.com/user-attachments/assets/2cd93b49-bf5d-4298-a80f-4589e78764ed" />

Loop Guard is specifically designed to protect against loss of BPDUs on non-designated ports due to unidirectional failure.

It keeps the port in a loop-inconsistent state instead of allowing it to move to forwarding.

On the SW3 port toward SW2
(the port that is currently non-designated / blocking)

Because:

That port is blocking due to inferior BPDU.

If BPDUs stop arriving, it might transition.

Loop Guard prevents that.

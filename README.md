# About-STP-Spanning-Tree-Protocol-

# Spanning Tree Protocol

Before Starting, there are few terms that needs to be defined, and understood.

Redundancy: Network Redundancy is the process of providing multiple path for traffic (backup path) so that data can keep forwarding or flowing evne if the primary path fails. 

here, Redundancy has different meaning depending on the topic that is being discussed, but in terms of networking it is understood as finding multiple path for the packets to flow and keep on operating the business even in the case of event failure.

Layer 2 loop: Layer 2 (data link layer), which consist of switches, and if two or more switches are connected with each other for Redundancy (multiple path), there is high chances that can create a proble called Layer 2 loop.

Let's understand how does the Layer 2 looping occures in case of Redundancy.
<img width="727" height="402" alt="image" src="https://github.com/user-attachments/assets/2a6011a6-14ef-4d2b-9520-9d74a2ec6be3" />

Here, there are 3 switches which are interconnected with eachother, and to remember the part that switch only has the capabilities to understand MAC address and nothing else, so now while sending a packet from PC1 (consider: connected to swithch 0), it sends to the swithch 0 which forwards to switch 1 and switch 2 and again switch 2 to switch 0 or any switch that is connected with each other creating an endless loop, and making the network restless.
and to solve that type of proble the concept of STP (Spanning Tree Protocal) comes: which acts as the loop-preventing protocol that allows redundancy (multiple paths), while creating loop-free layer 2 topology

Now the concept of Root bridge, Secondary Root Bridge, Root Port, Designated Port and also Alternate port.
Here in short, the meaning of each topic. <br>
Root Bridge: The STP managing Switch <br>
Secondary Root Bridge: The backup Root Bridge <br>
Root Port: The interface directly connected to the Root Bridge <br>
Designated Port: The interface which is in traffic forwarding state <br>
Alternate Port: The interface which is in blocking state. <br>

How the Spanning Tree Protocol Works?
There are total of 4 ways on how the spanning tree protocol works and they are:
<img width="765" height="461" alt="image" src="https://github.com/user-attachments/assets/ccd11686-0268-434b-8c4f-3231859f1de1" />
<br>
let's continue with the Root Bridge, <br>
it is a selected Primary LAN (SWITCH), from which the STP is managed.
<br>
The selection of this process goes through two cases: 
<br> 1. The priority value of Switches, and the lowest priority value is selected <br>
In case if the LAN (Switch), has the same priority values, this has high chance of happening, and if it occurs than the second case from which the Root Bridge is determined because:
<br> 2. Low MAC address, as the switch can only understand the MAC address.
<img width="669" height="399" alt="image" src="https://github.com/user-attachments/assets/1922aeab-498b-4e4c-89bb-75134d277178" />
<img width="870" height="67" alt="image" src="https://github.com/user-attachments/assets/eaffed1c-90a8-475d-8daf-6de0b97cee14" />
<img width="972" height="62" alt="image" src="https://github.com/user-attachments/assets/f0342db7-767c-4200-bc80-45c69626e348" />
<br>
Now whay choosing the Lowest Priority value or LOW MAC address for the selection of Root Bridge?


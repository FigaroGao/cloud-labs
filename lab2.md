Please use a [free Google] virtual machine in a cloud data center with a public IP address as the lighthouse to set up the connectivity for computers behind NATs 

Recommendations:
0. https://cloud.google.com/free/docs/free-cloud-features#compute
   ionos.com
   https://bandwagonhost.com/

1. https://github.com/slackhq/nebula

[Read Getting started (quickly)]

2. use a data comparison utility such as Meld and [Beyond Compare] to compare the configuration files attached to see where the changes should be made.

3. configure the config.yaml for the lighthouse and all participating computers.

4. some useful example commands for MAC OS:
 brew install nebula
 nebula-cert -version
 nebula-cert ca –name #it will report error. No worries.
 nebula-cert ca –name "LeiNetwork"
 nebula-cert sign -name "lighthouse" -ip "192.168.100.1/24"
 nebula-cert sign -name "MBP15" -ip "192.168.100.15/24"
 nebula-cert sign -name "mini" -ip "192.168.100.10/24"
 sudo nebula -config ~/.nebula/config.yaml

Download:  
<img width="1134" height="479" alt="image" src="https://github.com/user-attachments/assets/0673355f-f013-41e6-9c94-8ebef7079338" />

Edit the address:  
<img width="710" height="115" alt="image" src="https://github.com/user-attachments/assets/f9cae184-64ad-4841-a43c-0183e9d0e87e" />

Connect:  
<img width="960" height="439" alt="image" src="https://github.com/user-attachments/assets/b14c92c9-df0f-446d-8d4c-4a5742a4fae6" />  

Ping successfully:  
<img width="543" height="267" alt="image" src="https://github.com/user-attachments/assets/9f3bef1d-0b32-430e-880c-8c698ef36531" />

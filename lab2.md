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
<img width="1051" height="253" alt="image" src="https://github.com/user-attachments/assets/46e7948f-a607-4a25-b06a-10a7c4437768" />

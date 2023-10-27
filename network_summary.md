# network_summary

## Accessibility

Wazuh dashboard is accessible through https://chat.doclai.com

## List of nodes in network for attack

After joining into tailscale network, these are information of some nodes

IP of CS students' nodes:

1. 100.105.95.139 (duy-anh.tailbb898.ts.net)
2. 100.83.8.147 (vu-nguyen.tailbb898.ts.net)
3. 100.98.143.148 (me.tailbb898.ts.net)

IP of the nodes for being attacked (will be updated):

1. Node1: 100.84.43.137
2. ...
3. ...

IP of Wazuh manager: __100.90.133.143__ (wazuh-full.tailbb898.ts.net)

IP of reverse proxy: 100.113.95.35 (reverse-proxy.tailbb898.ts.net)


These nodes need not to be online 24/7. You can host one by ubuntu server and DVWA and add them to the network by sending me tailscale login link. Whenever you need to attack the node(s), just simply turn on the VM(s) and Internet connection, then the alert data will be send to the Wazuh manager

## Node agent setup

1. Install nginx, DVWA in one virtual machine.
2. Clone this machine and change each hostname of new host to a different one (if you want to have multiple machines, else skip this step).
3. Install tailscale, send me the login link.
4. __After joining the network__, install Wazuh node agent.

To setup  Wazuh node agent, change the IP of Wazuh manager in config file of node agent to the IP above.
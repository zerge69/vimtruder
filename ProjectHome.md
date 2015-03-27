Normal trojans are a known threat, and we know how to mitigate them. But what about virtual machine trojans?
This is a proof-of-concept Virtual Machine Trojan
Visit www.infosegura.net/vimtruder.html for details


Virtualization technology is such an efficient way of managing IT resources that there’s no doubt that in a very short time it will become the only way of doing it. But virtualization is still a new technology, and security is still lagging behind.

Normal trojans are a known threat, and we know how to mitigate them. But what about virtual machine trojans? A VMT comes embedded within a virtual machine. When a user downloads a virtual machine from the Internet, and then runs it on his/her computer, the antivirus installed in the host machine simply does not have access to the virtual machine, so the virtual machine does not get scanned.

ViMtruder consists of a client which is installed within a virtual machine, and a control server, which sits in a host on the Internet. The virtual machine, running Linux, is configured to automatically run the VMT client in the background upon boot up. The VMT tries periodically to contact the control server through the Internet using port 80 outbound. Once the control server links with the VMT, you can send it Nmap commands to scan the target LAN where the VMT is connected.
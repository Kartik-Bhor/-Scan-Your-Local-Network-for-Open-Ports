Task 1: Scan-Your-Local-Network-for-Open-Ports

--->Scanned local network to find open ports and services running on the ports and their potential threats and captured packets on the network with wire shark to analyse them. 

**Refer to screenshots for proof of original results.**
Nmap scan : Scanned network with Nmap and found 3 IP address operating.

198.168.31.1 --> WIFI IP address
192.168.31.7 --> mobile IP address
192.168.31.92 --> laptop IP address

Scanned ==> 192.168.31.1 (WIFI IP address) Found open ports and services.

Results : Open Ports   services
	  
	     53 	domain
	     80		http
	     443	https
	     7443	oracleas-https
	     8080	http-proxy
	     8443	https-alt

All ports are open and using TCP protocol.

services : Domain-> domain name system (DNS) Requests.
		Threat==>DNS spoofing, DNS tunnelling etc.

	   http and https -> request and response protocols.
		Threat==> http-> MITM attack, injection attacks.
			  https-> certificate forgery, phishing sites.

	   oracleas-https-> https service used by oracle application server.
		Threat==> Weak ssl, unprotected admin panels.

	   http-proxy-> proxy port used when port 80 is busy
		Threat==> open proxy exploits, injection Attacks.

	   https-alt-> used when port 443 is busy as an alternative.
		Threats==> Brute force on login panels, insecure TLS configurations.


Wireshark Scan : 

 		+Captured diffrent packets fro the network.
		+applied filters for specific ip packet capture.
		+protocols:ARP
			   UDP
			   ICMP
			   DHCP .etc.
		+Noticed conversation between multiple devices in my network.


# TLS
# PGP
# HTTPS
- =HTTP(safe version)
- Hyper text transport protocol
# HTTP 
- protocol which allows the fetching of resources, such as HTML documents.
- foundation of data exchange on Web and client-server protocol, which means request are initiated by the recipient(usually web browser).
- Base on TCP\IP 
- HTTP 1.0 base on TCP
- HTTP 3.0 base on UDP
# TCP\IP
- transmission control protocol
- used on the top of IP to ensure reliable transmission of packets
- 
# SSL
## SSL (Secure Sockets Layer)
- digital certificate that authenticates a website's identity and enables an encrypted connection. 
- A security protocol that creates an encrypted link between a web server and a web browser.
- Companies needs to add SSL certificates to their websites to secure online transaction and keep customer information private and secure.
### How does SSL work?
- SSL works by ensuring that any data transferred between users and websites , or between two systems, remains impossible to read.
- using encryption algorithms t oscramble data in transit, which prevents hackers from reading it when delivering.
#### The process work like this:
1. A browser server attempts to connect to a website (secured with SSL)
2. The browser or website requests the web server identifies itself
3. The web server sends the browser or server its SSL certificate response
4. browser\server check SSL. If trusted, a signal will be sent to the server
5. Web server returns with digital acknowledgement to start SSL encrypted session
6. encrypted data shared between browser\server\webserver
   
# IPSec


# DOS (attack)
- denial of service
- cyberattack on devices, information systems or other network resources that prevent legitimate users form accessing.
- In a DoS attack, rapid and continuous online requests are sent to a target server in order to overload the server's bandwidth.
- Distributed denial-attack-of-service(DDOS) leverage a wide web of computers or devices infected with MALWARE to launch a coordinaed barrage of meaningless online requests, blocking legitimate users.
## SYN Flooding
- commom form of DDOS attack that can target any system (connected to the Internet and providing Transmission Control Protocol(TCP) services).
- A type of TCP State-Exhaustion Attack that attempts to consume the connection state tables present in many infrastructure components(load balancers, firewalls, Intrusion Prevention Systems(IPS) and application servers)
- This type of DDoS attack can take down even high-capacity devices capable of maintainging millions of connections

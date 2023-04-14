    # TLS
    # PGP
# HTTPS
- =HTTP(safe version)
- Hyper text transport protocol
- default port: 443
    # HTTP 
    - protocol which allows the fetching of resources, such as HTML documents.
    - foundation of data exchange on Web and client-server protocol, which means request are initiated by the recipient(usually web browser).
    - Base on TCP\IP 
    - HTTP 1.0 base on TCP
    - HTTP 3.0 base on UDP
    # TCP\IP
    - transmission control protocol
    - used on the top of IP to ensure reliable transmission of packets
    
# TCP 
- Protocal for connection
- before a APP using TCP, it should build up TCP connection in priority
- after the data transmission is finished, the TCP connection must be released.
- ***each TCP connection can only have 2 port(point to point)
- TCP is quite reliable, data through TCP are : 
  no mistakes\no package loss\no overlapping(repeat)\arrived by orders
- TCP allows both sides sending data whenever they  want. Both sides have [sending buffer] and [recevinging buffer]settled, in order to store data for binary communication.
- TCP ***cannot*** ensure the sending data = received data   
  1. for example: A send B 10 data bulk, but its receiver may already delivered them to the upper-class APP when 4 of 10 bulks are received.
  2. order:  sender write data into buffer, and TCP notes are added to the front of the data, then data was received by receive buffer, receiver take the data from buffer
  3. just like someone wants to give you ammo, he puts it into a mag(=buffer), then give it to you (=tcp connection), you take the mag(= buffer), and load it into your rifle.
  4. TCP is differed from UDP, while TCP does not care how much bytes are loaded in the buffer at once, it makes its decision by checking the valuing receive port and the network congestion level. 
   (just like if A wants to give you ammo, beforehand he will check which type of mag you're using, and check if the resupply-line is congested, if it's in a traffic jaw, he will load less ammo in a mag )
  5. if there are too much data waiting for the APP putting into TCP buffer, TCP will cut it into smaller part and send.  If the APP put only 1 byte each time, TCP could wait until enough bytes are loaded.
   ( just like A gives you ammo, but there are too much ammo to load, so he has to cut them into groups and load it into mag,  but if the ammo supply only provide him one bullet each time, then he could wait until the bullets are enough to load into mag, and send it away----just to be more efficent)
- the port of TCP connection is called ***socket***
- port number ***concatenated*** with IP address= socket
- ***EXAMPLE*** TCP connection = {socket1, socket2} = {(IP1 : port1), (IP2: port2)}     which is    (IP address: port number)
- ***TCP allows APP accessing API(Application Programming Interface), which is called socket API, in simplication: socket***
  ### Why is TCP dependable
  1. an ideal transport condition is like :
  - the channel is perfect and makes no mistakes
  - whatever how fast the data was deliverd, the receiver can always receive it punctually.
  - but actually network can't reach these premise. So some reliable protocols are needed, to enable sender delivering data again when a mistake occurs. 
  - meanwhile, when the receiver cannot cna't handle the data at once, it could tell the sender to curtail data efficiency---- so that the unstable channel will be reliable.
  - ***STEP*** A send B data, B recall 'confirm' , then A send another, but if B didn't respond, then **[timeout]** 
  2. by using this mode, we could build up reliable communications while using a not so dependable network.
  3. protocal like this is usually called **ARQ(Automatic Repeat reQuest)**
  this request is done automatically, the receiver don't need the requester resend an error group.
  4. ***Using Streamline in TCP*** in order to reach higher efficiency, streamline can be used like: sender send couples of data consecutively, which means A sends B messages without reply, so that the channel can be filled up.
  5. ***consecutive ARQ protocol***
  data in sending port will be send consecutivly, without confirm replied.
  when a 'confirm' is received, the port move forward and send another group of data.
  The receiver usually use **accumulating confirm** , which means the receiver don't have to reply for each data group, but replying after receiving the last group of data.
  
  
# SSH
- Secure Shell
- accord base on apps
- use for loginingremoted conversations and other network service
- useful for preventing information- leaking

# Explorer Setting
## Internet
- for Internet website, do not fit trusted & restricted website
## Intranet
- for all web in Intranet(private network)
## Trusted site
- only for trusted
## restricted site
- for website may harm your devices

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

# ARP attack
- using fake IP & MAC address, create lots of ARP communications that clogs the Network
- forging IP & MAC address will makes all IP Packages unable to reach the gateway, lead to cross-network-segment communition failure
- to handle ARP attack, need to break Network between the attacker, and use ***arp-d*** order to clear the ARP buffer

# Repeater
- Network hardware device
- work at the physical layer of OSI model, amplify or regenerate signals before retransmitting it
- Known as "Signal Boosters"
- physical layer
  
# Router
- network layer


# Communicataion
- In TCP/IP network, setting communications and links should be on transmission part 
- so do OSI/RM

# IP address
## Example : 222.125.80.128/26
1. how many available host contains
- 128's decimal=  10000000
- it has 6*0, so it could be formed by 2^6-2= 62 host
- 2^6-2=62
- 
2. address type
- 222.125.80.10xxxxxx 
- (minimum 222.125.80.10000001=222.125.80.129)
- (maximum 222.125.80.10111110=222.125.80.190)
3. how many 

# ARP
- Address resolution protocol
- Network accord

# network class
1. Class A network
- 0.0000000(7*address).000....00(24*host)
2. Class B network
- 10.0000..(14*address).0000(16*host)
3. Class C network
- 110.0000(21*network).0000(8*host)
4. Class D network
- 1110.(no diversify of address and host)
- public address(224.0.1.0 ~ 238.255.255.255)
- private address(239.0.0.0 ~ 239.255.255.255)
- special address(224.0.0.0 ~ 224.0.0.255)
5. Class E address
- no diversify of address and host 
- 240.0.0.0.1 ~ 255.255.255.254


# two-layer switch
- base on MAC address(data link layer) transfer data
- use VLAN to segregate broadcast-domian
- because it use VLAN to segregate, only terminal devices under same VLAN can transfer data
- so if different VLAN terminal devices has has a request, another router is needed
- <font color=red>IN ALL: two-layer switch must corperate with router to make a ***cross-VLAN*** communication</font>

# three-layer switch
- Most Common used
- base on IP address(network layer) , to enable functions like:  choosing router & group filter
- used for Intranet, and router is for gateway connecting Internet
- ***Structure***
1. control surface(CPU,Memory,Supervisor IOS)
- wholesome control base on CPU software
- ***Work***: system management, Administrator\User interface , router protocol choosing 
2. Data surface(ASIC. TCAM)
- Data transformation base on ASIC,FPGA, Network handler **(ALL hardware)** 
-  two-layer switch finishing MAC data transmission
-  three-layer switch finishing IP group transmission.
-  (handle necessary management in transmission like: Visiting control list/QoS)
3. Backboard
- data transmission base on port in 3 ways:
share bus, share memory, crossway
- Intranet standard : IEEE 802.3ap, IEEE 802.3ba
4. port
- receive/send data between other hardware.
- use RJ-45 or SFP port in three-layer switch

when hardware structure was divided into control surface and data surface, FIB(Forwarding information base) & AT(adjacency table) will be meeded for transmission
- this is call super-fast forward
### FIB
- Forwarding Information Base
- Formed base on router's information on control surface, by sufficient subnet, output port's information 's combination  

### adjacency table
- 

**<font color= red>Difference between router and three-layer switch:<font>**
1. Three-layer switch _only_ support ethernet protocol and IP network protocol
2. Base on ASCI hardware management,  but router base on CPU software
3. 3-layer switch do not support VPN\NAT .etc
4. router do not support private VLAN\ LAN tracking, RSTP/STP .etc
5. Router Use CPU to forward, BUt three-layer switch use ASCI( faster )
### Structure
### EXAMPLE
- a router, connecting a layer(with 4 divices), and a concentrater(with  devices)
- then there are 2 boardcast domain, 5 collision domain
- each port of layer = 1 collision domain
- each Net connected by router= one boardcast domain

# PPP protocol
- (point-to-point protocol), a kind of DLL(data link layer)protocol
- <font color=red>most popular Internet protocol are TCP/IP , no matter what protocol the DLL uses, it can connect to Internet with TCP/IP<font>
- PPP only allows users to communicate, but unable to access other host or device like Intranet/
- PPP format:
FLAG   Address  Control   Protocol   Upper data    FCS    FLAG
## FLAG
- in PPP protocol there's a Flag at the front and end

## FTP protocal
- port :  20 and 21
- 20 for data, 21 for control
  
## SNMP protocal
- for application-layer
- its transmission-layer protocal is UDP
  
## UDP
- 
## ARP & ICMP protocal
- for networl-layer

## X.25 protocal
- for exchange network

## explorer 
- when typing a correct address in explorer, local host will enquire its related IP address in ***local hosts file***
- order: local host---local DNS buffer---local DNS server---root name server


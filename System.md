

# vulnerability scanning
- the process of discovering, analysing, and reporting on security flaws and vulnerabilities. 
- via scanning tools to identify potential risk exposures and attack vectors across an organizations's networks, hardware, software, and systems.

# Firewall
## Packet Filtering firewall
- operate at the network of OSI model. It make processing decisions based on <font color=red>network addresses, ports, or protocols</font>.
- Very fast, not  much logic going behind the decisions they make.
- They **DO NOT** do any internal inspection of the traffic, **NOT** store any state information.
- You have to manually open ***ports*** for all traffic that will flow through the firewall.
- <font color=red>Does NOT contain: MAC address filter</font>
## Firewall defense Priority
- From **highest level to the lowest** : _LAN Area_ > DMZ > Internet


# Virus
## boot virus(boot infector/ MBR virus/DBR virus)
- targets and infects a specific, physical section of a computer system that contains information crucial to the proper poeration of the computer's operating system(OS).
## infecting virus
- infecting execution files(including .exe & .com)
## complex virus
- virus with feature of boot&infect
## Catalog virus
- virus that modify address of files
## Trojan horses virus
- a type of malware that downloads onto a computer disguised as a legitimate program.
## worms virus
- malware or malicious software that can replicate rapidly and spread across devices within a network.
- As it spreads, a worm consumes bandwidth, overloading infected systems and making them unreliable or unavailable.


# Certificate security
1.HTTPS
- HTTP（safe）
- PGP
- MIME: has nothing to do with security, it's just a standard 

# Cyber Attack
1. Replay attacks/ Freshness Attack
- attacker send the targeted a pack (that already received before) to deceive the system
- mainly used for identity verification
- Kerberos system use "time stamp"to prevent

# Input/Output
## running process (step)
1. hardware (executing I/O operand) 
2. interruppt handler(revoke ***Device Driver*** when the I/O is finished)
3. device driver (set device register, check condition)
4. other software (named\protet\clog\buffer\allocate)
5. user process(use I/O , formatting I/O, spooling )

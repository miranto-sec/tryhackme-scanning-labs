# tryhackme-scanning-labs
# Overview:
  completed hands-on scanning labs on TryHackMe focusing on passive and active recon techniques

# Skills Learned:
  - Passive recon(OSINT)
  - Active scanning
  - Network enumeration
  - Service detection

# Tools Used:
  - Nmap
  - Whois
  - Nslookup
  - Dig
  - DNSDumpster
  - Shodan
  - Netcat
  - Telnet

# Labs Completed:
  1. Passive Scanning
     ## Commands Used:
          whois tryhackme.com
          nslookup -type=MX tryhackme.com
          dig @1.1.1.1 tryhackme.com MX

     ## What I Learned:
          - Gather info without touching the target
          - Understand domain + DNS info
          
  2. Active Scanning
      ## Commands Used:
          ping -c 10 <MACHINE_IP>
          traceroute <MACHINE_IP>
          telnet <MACHINE_IP> 80
          nc <MACHINE_IP> 80

      - What I Learned:
          + Identify if a host is up
          + check for the path taken by the packet from my system to another host
          + discover more information about a web server on a particular port
          + collecting banners
          + client and server TCP / UDP

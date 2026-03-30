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


      # Nmap
       1. mportant flags:
            - sC  : for default scripts(safe enum)
            - sV  : for service version detection
            - -p- : scans all 65535 ports
            - sS  : stealth SYN scan (faster than TCP scan and less noisy)
            - A   : aggressive scan (os , version detect , scripts , traceroute)
            - sU  : UDP scan finds DNS , SNMP
            - --script vuln  : vulns detection scripts
            - -p <port> : for targeted port scans . e.g nmap -p 22,80,443
            - oN  : saves results , good for reporting

        2. Real-world workflow:
             ## Fast scan:
                  nmap -T4 -F <trget>
            ## Full scan:
                  nmap -p- <target>
            ## Detailed scan on ports:
                  nmap -sC -sV -p <ports> <target>
            ## Vuln scan:
                  nmap --script vuln -p <ports> <target>
                       
          
         

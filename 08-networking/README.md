# Networking Commands

1. ping -

2. netstat -
   - to check the active connections
3. ifconfig
   -lo - means loop back -internally - localhost
   -eth0 - nic
4. traceroute
   - used to trace route to check the ip hooping

5. tracepath
   -
6. mtr
   - my trace route

7. nslookup
   - gives info about the ip-address details of the particular website

8. telnet
   - helps to connect to website-particular port-number
     -443 - https
     -8080 - http
9. hostname
   - cat /etc/hosts
10. ip address show

11. iwconfig
    - gives wireless attachments info

12. ss - same as netstat
    Netid State Recv-Q Send-Q Local Address:Port Peer Address:Port Process

13. dig
    - dig is a command-line tool used for querying Domain Name System (DNS) servers to retrieve domain information such as IP addresses, DNS record types (A, AAAA, MX, TXT, NS, etc.), and troubleshoot DNS issues. It is part of the BIND (Berkeley Internet Name Domain) software suite and is widely used by network administrators for DNS diagnostics and configuration verification.

14. whois
    - gives info about your domain name

15. nc (netcat)

16. arp
    - Address Resolution Protocol
    - to know the mac address of the hardware (host, router etc)

17. ifplugstatus
    - detect the link status of a local Ethernet or wireless network interface, determining whether a cable is physically connected (link beat detected) or disconnected (unplugged).

## Most commonly used networking commands

1. curl vs wget
   - curl - is used to call the api-endpoints - to get the data from teh server
     eg: curl -X GET https://example.com/api/test | jq
   - jq - beautifies the data from the endpoints

2. wget
   - command used to download the file from the internet

3. iptable-
   - The iptables command is a powerful user-space utility in Linux used to configure the kernel's Netfilter firewall, enabling administrators to set up, maintain, and inspect packet filtering and NAT rules.

4. watch
   - watch top

5. nmap\*
   - network mapped
   - nmap -v website -? -v means verbose
   - network scanning

6. route
   -

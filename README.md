# writeup_toolsrus

Practise using tools such as dirbuster, hydra, nmap, nikto and metasploit


This CTF challenge is one of the basic challenges to start your pentesting career with. Give it a shot yourself before going through the solution.


Step 1:

Run nmap to enumerate all the ports and services running on the server.

![GitHub Logo](/nmap.png)
Format: ![Alt Text](url)

Step 2:

Run Dirtbuster to enumerate all the directories on the vulnerable machine

![GitHub Logo](/dirbuster.png)
Format: ![Alt Text](url)

I noticed a stustus of 401 forbidden hinting a login page.

Step 3:
basic http auth 
Run Hydra with wordlist(for password) and name('bob' as displayed in /guidelines) to authenticate.. 

![GitHub Logo](/hydra.png)
Format: ![Alt Text](url)


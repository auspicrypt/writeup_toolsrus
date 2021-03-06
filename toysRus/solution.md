# writeup_toolsrus

Practise using tools such as dirbuster, hydra, nmap, nikto and metasploit

This CTF challenge is one of the basic challenges to start your pentesting career with. Give it a shot yourself before going through the solution.

Landing page:

![GitHub Logo](/toysRus/images/landing_page.png)
Format: ![Alt Text](url)

## Step 1:

Run nmap to enumerate all the ports and services running on the server:

![GitHub Logo](/toysRus/images/nmap.png)
Format: ![Alt Text](url)

## Step 2:

Run Dirtbuster using 'directory-list-1.0.txt' to enumerate all the directories on the vulnerable machine:

![GitHub Logo](/toysRus/images/dirbuster.png)
Format: ![Alt Text](url)

I noticed a (401 forbidden) status hinting a login page.

Upon checking the ZAP traffic, it was basic-auth indeed.

![GitHub Logo](/toysRus/images/basic_auth.png)
Format: ![Alt Text](url)

## Step 3:
Upon navigating to '/protected', it uses basic-http-authentication. 
Run Hydra with wordlist(dictionary attack) and name('bob' as displayed in /guidelines) to authenticate:

![GitHub Logo](/toysRus/images/hydra.png)
Format: ![Alt Text](url)

## Step 4:

Use metaspolit to check possible exploits.

![GitHub Logo](/toysRus/images/exploits.png)
Format: ![Alt Text](url)

Upon checking sequentially, 63/tomcat_mgr_upload exploit worked upon setting the respective parameters.

![GitHub Logo](/toysRus/images/set_options.png)
Format: ![Alt Text](url)

The exploit was successful to check last flags.

![GitHub Logo](/toysRus/images/last_flags.png)
Format: ![Alt Text](url)

[FLAGS]

Flag1: guidelines
Flag2: bob
Flag3: protected
Flag4: bubbles
Flag5: 1234
Flag6: Apache tomcat/7.0.88
Flag7: 5
Flag8: Apache/2.4.18
Flag9: 1.1
Flag10:  root
Flag11: ff1fc4a81affcc7688cf89ae7dc6e0e1

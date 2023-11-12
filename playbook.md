# Enumeration

- nmap
- gobuster
- nikto
- metasploit Auxilary
- version information
- enumerate ssh
- enumerate smb

## NMAP

### Interesting Services/Ports

- smb - port 139/137/445/138
- http - port 80/8080/8000
- ssl/https - port 443

## Site?

- Places of input
- cross-site scripting vulns
- sql injection
- robots.txt
- source code

## SSH

- ex: ssh 255.255.255.255 -oKexAlgorithms=+diffe-hellman-group1-sha1 -c aes128
- banner might be exposed after connection

## Metasploit

- info - give info of a module
- use {number/directory path} - use a specified module
- options - gives the options of a specified module
- set {option of module} {value} - sets a value to specified option in a module
- run - runs the module
- set payload {directory path} - set payload options

### Source Code

- comments
- javascript
- javascript sources

# Exploitation

- hydra - for brute forcing - ex: hydra -l root -P /usr/share/wordlists/metasploit/unix_password.txt ssh://255.255.255.255:22 -t 4 -V
- smbclient - ex: smbclient -L \\255.255.255.255\\ADMIN$ - can use linux-like commands
- msfvenom
- metasploit - try changing payload if the initial payload does not work
- metasploit brute forcing on ssh - use auxilary/scanner/shh/ssh_login
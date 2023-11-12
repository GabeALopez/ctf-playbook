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

- smb - port 139
- http - port 80/8080/8000
- ssl/https - port 443

## Site?

- slaces of input
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

### Source Code

- comments
- javascript
- javascript sources

# Exploitation
 
- smbclient - ex: smbclient -L \\255.255.255.255\\ADMIN$ - can use linux-like commands
- msfvenom
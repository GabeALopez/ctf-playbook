# Overall

- file upload
- cross-site scripting for input
- look for what you have access to
- inspect element
- use obfuscations

# Sensative Data Exposure

**Check for:**
- security headers
- ssl ciphers - ex: nmap --script=ssl-enum-ciphers -p 443 tesla.com

# Broken Authentication

**Check for:**
- tokens
- forgot my password
- if site does not say "wrong password or username"
- if forgot my password allows for certain fields to open or closed based off of password or username

# SQL Injection

**Regular type**
- ex: ' OR '1

**Error based payload:**
- ex: OR 1=1

**Time based:**
- sleep(5)#

**Union Select:**
- ex: ORDER BY SLEEP(5)

**Auth Bypass:**
- ex: '-'


# Broken Access

**Check for:**
- any id in url - ex: ?id=5 
- any direct access through the URL directories - ex: blah/blah/admin
- can find id after inspect element and removing hidden. Can possibly change value
- cookies

# XXE Issues

- can submit XML files that put data from system like /etc/passwd

**ex:**

<?xml version="1.0" encoding="ISO-8859-I"?>
    <!DOCTYPE foo [
        <!ELEMENT foo Any>
        <!ENTITY xxe SYSTEM "file:////etc/passwd">
        ]> <foo>&xxe;</foo>

# Security Misconfiguration

- default credentials
- bypass file upload

# Cross-Site Scripting (XSS)

*Note: look for any input - Includes URL*

**reflected**
- get back something from site
- client side
- ex: `<iframe src="javascript:alert('xss')">` - `<script>alert('1')</script>`

**Stored**
- stored on server
- server side
- if filtering try using differing combinations of input to bypass

**DOM (Document object model)**
- client side

# Insecure Deserilization

- 

# Using Components with Known Vulnerablities

- 

# Network Traffic Analysis Report

## 1. Overview
network traffic analysis to capture login credentials transmitted over HTTP Not HTTPS.

## 2. Objective

Capture and extract sensitive login data like username and password from **unencrypted HTTP**.


## 3. Environment
- **OS**: Kali Linux
- **Tool**: Wireshark
- **Interface**: eth0
- **Target Website**: http://testphp.vulnweb.com/login.php


## 4. Steps Performed
1. Open Wireshark and capture on eth0.
2. Visited the login page on the http://testphp.vulnweb.com/login.php.
3. Enter test credentials:
   - Username: `wateen`
   - Password: `1234567`
4. Stopped the capture after submitting.
5. Filtered the captured traffic using the `http` filter.
6. I Clicked on **POST** request then I found credentials.

## 5. Findings
- Username and password were transmitted in cleartext via HTTP.
- No SSL/TLS encryption (no HTTPS used).

## 6. Risks
-Potential the attackers know this sensitive data then exploit it .
-Expos of user credentials.

## 7. Recommendations
- Use HTTPS.
- Ensure that the site uses an encrypted and secure protocol like HTTPS it use **(SSL/TLS)**.



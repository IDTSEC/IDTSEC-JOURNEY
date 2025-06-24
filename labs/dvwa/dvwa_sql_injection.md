# DVWA - SQL Injection (Login Bypass)  

**Vulnerability:** SQL Injection
**Target:** DVWA - Login Bypass
**Security Level:** Low

## Payload used:  
1' OR '1'='1

## Steps Taken:  
1. Open DVWA in browser
2. Set sec level to **Low**
3. Go to **SQL Injection** Module
4. Enter the payload 1' OR '1'='1 in the input box
5. **Submit**

## Result?
- the app returned user data without authentication
- SQL query was bypassed using the payload

## Defence  
Safe coding practices needed - devs should use:  
- prepared statements/parameterized queries (keeping data & SQL commands separate - even if the input is malicious, it won't change the meaning of the query, basically being treated just as text)
- input validation & sanitization: checking that the user input is what we expect (letters/numbers for username), and cleaning it to remove dangerous characters
Spotting input such as **1' OR '1'='1** is a RED flag    

## Final notes  
A classic authentication bypass using SQL injection - in a real world scenario, this could lead to full account takeover/data leakage

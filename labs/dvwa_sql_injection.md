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

## final notes  
A classic authentication bypass using SQL injection - in a rea lworld scenario, this could lead to full account takeover/data leakage

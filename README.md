### EX NO 2

### AIM:
The aim is to configure SELinux to allow access to web content served from port 82 located in the /var/www/html directory without altering or removing any files in that directory.

### PROCEDURE:

1. Check SELinux Status:
Before making any changes, it's important to check the status of SELinux

3. Identify SELinux Context:
Check the SELinux context of the /var/www/html directory to understand its current configuration

4. Set SELinux Context for Port 82:
Since your web content is configured to be served from port 82, you need to update SELinux to allow access to this port. 

5. Reload SELinux Policies:
After making changes, it's essential to reload SELinux policies for the changes to take effect.

6. Verify Configuration: 
Verify that SELinux is now allowing access to port 82 and the /var/www/html directory.

7. Test Access: 
Finally, test access to your web content served from port 82 to ensure that SELinux is configured correctly and allowing access without any issues

### PROGRAM / COMMANDS:
```
Developed by: Samyuktha S
Register Number: 212222240089
```
```
sestatus
ls -Z /var/www/html
semanage port -a -t http_port_t -p tcp 82
restorecon -Rv /var/www/html
semanage port -l | grep http
```
### OUTPUT:
![image](https://github.com/SamyukthaSreenivasan/Configuration-of-SELinux/assets/119475703/a066fe5e-ec5f-40f9-a472-96d164e23a7f)

## RESULT:
Thus the program to configure SELinux is been successfully implemented.

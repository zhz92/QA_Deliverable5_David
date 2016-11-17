# QA_Deliverable5_David
This deliverable is to use OWASP ZAP to detect and analyze vulnerability in testing website
    https://techguile.wordpress.com/2012/11/25/list-of-demo-websites-of-security-testing-purpose/
3 vulnerabilities found are listed below toghether with analysis and descriptions:

Vulnerability 1

Answers to Questions

1.	This vulnerability attacks confidentiality, because unauthorized person can get access to the admin account.
2.	Interception can exploit this vulnerability because people can do eavesdropping.
3.	Attacks exploit this vulnerability is passive since it is majorly for eavesdropping, not modify or delete any data.
4.	Due to exploiting this vulnerability, unauthorized access can be grabbed.
5.	Solutions:
Do not concatenate strings into queries in the stored procedure, or use 'exec', 'exec immediate', or equivalent functionality!
Do not create dynamic SQL queries using simple string concatenation.
Apply a 'whitelist' of allowed characters, or a 'blacklist' of disallowed characters in user input.
Apply the principle of least privilege by using the least privileged database user possible.
Grant the minimum database access that is necessary for the application.

Additional Information

1.	URL
http://demo.testfire.net/bank/login.aspx
Description: Unauthorized access as admin

2.	Steps for reproduction
2.1	Go to the web site using the link: http://demo.testfire.net/bank/login.aspx
2.2	Enter admin as Username
2.3	Enter ZAP' OR '1'='1' – as Password and click Login button

3.	Screenshot of vulnerability
Before penetration testing: 
![picture1](https://cloud.githubusercontent.com/assets/16587395/20372591/4df71068-ac3a-11e6-91c9-2574c14a1e88.png)

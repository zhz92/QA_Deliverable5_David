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

Before testing: 
![picture1](https://cloud.githubusercontent.com/assets/16587395/20372591/4df71068-ac3a-11e6-91c9-2574c14a1e88.png)

After testing:
![picture1](https://cloud.githubusercontent.com/assets/16587395/20372613/80e24f1a-ac3a-11e6-9c51-610adf9cf9c6.png)



       Vulnerability 2

Answers to questions

1.	This vulnerability attacks integrity, and is called cross-site script (XSS), because it passes invalidated input sent through requests back to the client.
2.	Fabrication can exploit this vulnerability because attacker can insert data to the browser and show the invalidated information to client.
3.	This attack is active because a user must initiate the action by submitting the form.
4.	Due to this attack, it injects script to the site and can read, modify and transmit any sensitive data accessible by the browser.
5.	Solutions:
Preventing XSS from exploiting a system is centered around filtering user input. Proper filtering alone can prevent about 95% of XSS holes. In addition to filtering, there are many commercial solutions available to protect web applications. 



Additional Information

      1.	URL:
http://testphp.vulnweb.com/guestbook.php

      2.	Steps for reproduction

2.1.	Go to the site in the above link

2.2.	Input </strong><script>alert(1);</script><strong>  in the add message textbox.

2.3.	Click on add message button

      3.	Screenshot of vulnerability

Before testing
![picture1](https://cloud.githubusercontent.com/assets/16587395/20372751/8a69bd9c-ac3b-11e6-9594-ba0b3628f58a.png)

After testing:
![picture1](https://cloud.githubusercontent.com/assets/16587395/20372772/a03a4b28-ac3b-11e6-96e8-af583e68795d.png)

            
                 Vulnerability 3

   Answers to questions

1.	This vulnerability is called remote File Include (RFI). It is an attack technique used to exploit "dynamic file include" mechanisms in web applications. It attacks integrity because it direct user to another web.
2.	Any kinks of attacks can exploit this vulnerability, like interruption, modification, fabrication. Because web site can be tricked into including remote file or website with malicious code, thus can modify, delete or insert data.
3.	This is passive attack because user need to initiate the attack by inputting the username and password, and then be redirect to another website or some malicious code will start to run.
4.	Due to this vulnerability, user may suffer data loss, content manipulation, data insertion, etc.
5.	Solutions:
When the set of acceptable objects, such as filenames or URLs, is limited or known, create a mapping from a set of fixed input values (such as numeric IDs) to the actual filenames or URLs, and reject all other inputs.

Assume all input is malicious. Use an "accept known good" input validation strategy, i.e., use a whitelist of acceptable inputs that strictly conform to specifications. Reject any input that does not strictly conform to specifications, or transform it into something that does. Do not rely exclusively on looking for malicious or malformed inputs (i.e., do not rely on a blacklist). However, blacklists can be useful for detecting potential attacks or determining which inputs are so malformed that they should be rejected outright.

When performing input validation, consider all potentially relevant properties, including length, type of input, the full range of acceptable values, missing or extra inputs, syntax, consistency across related fields, and conformance to business rules. As an example of business rule logic, "boat" may be syntactically valid because it only contains alphanumeric characters, but it is not valid if you are expecting colors such as "red" or "blue."

For filenames, use stringent whitelists that limit the character set to be used. If feasible, only allow a single "." character in the filename to avoid weaknesses such as CWE-23, and exclude directory separators such as "/" to avoid CWE-36. Use a whitelist of allowable file extensions, which will help to avoid CWE-434.


Additional questions

          1.	URL:

http://testasp.vulnweb.com/Login.asp?RetURL=http%3A%2F%2Fwww.google.com%2F

          2.	Steps for reproduction

Precondition: user has registered an account, and the username is 123, password is 123.

2.1.	Go to the website in the above link.

2.2.	Type in Username: 123

2.3.	Type in Password: 123

2.4.	Click on Login button

          3.	Screenshot of vulnerability

Before testing:
![picture1](https://cloud.githubusercontent.com/assets/16587395/20372799/dc1ee892-ac3b-11e6-8860-425863503418.png)

After testing:
![picture1](https://cloud.githubusercontent.com/assets/16587395/20372815/f0660f74-ac3b-11e6-9ef5-d83bdf742879.png)

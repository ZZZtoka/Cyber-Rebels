## B20_Enhance the Security of a GitHub Project

## Description
I enhanced the security of a web-based GitHub project by creating a secure contact form demo for Little Way. The project focused on improving web form security by implementing input validation, format checking, suspicious content filtering, and Google reCAPTCHA v3 protection to reduce bot submissions and common web attacks.

# Project Repository

View the full source code and implementation here:

[Little Way Secure Contact Form Demo](https://github.com/ZZZtoka/littleway)

## Findings
- Implemented Google reCAPTCHA v3 to detect and reject automated bot submissions
- Added format validation for name, email, phone number, and message fields
- Rejected invalid inputs that did not match the required format
- Detected and blocked suspicious script content such as <script>alert(1)</script>
- Tested automated form submission using PowerShell Invoke-WebRequest
- Verified server-side rejection responses and reCAPTCHA failure detection


## Evidence
Figure 1: Secure contact form demo with Google reCAPTCHA v3 enabled.
![1](Evidence/1.png)

Figure 2: Invalid name, email, and phone inputs rejected by the system.
![2](Evidence/2.png)

Figure 3: Suspicious script injection attempt detected and rejected.
![3](Evidence/3.png)

Figure 4: Automated bot-style submission tested using PowerShell.
![4](Evidence/4.png)

Figure 5: Server log showing failed reCAPTCHA verification response.
![5](Evidence/5.png)

## Analysis
Web contact forms are common targets for spam, automated bot submissions, SQL injection, and cross-site scripting attacks. By implementing Google reCAPTCHA v3, the project added a behavioural protection layer that helps distinguish legitimate users from automated requests. Input validation also improved security by ensuring that submitted data followed expected formats before being processed by the application.

The project successfully rejected malformed inputs such as invalid email addresses and phone numbers. It also detected suspicious script payloads, reducing the risk of cross-site scripting attacks. The PowerShell automated submission test demonstrated how attackers may attempt to submit forms using scripts instead of a normal browser session. The failed reCAPTCHA verification showed that the system was able to identify and reject suspicious automated activity. These controls show how layered security measures can reduce common web application risks.

## Reflection
This activity improved my understanding of secure web application development and defensive cybersecurity practices. I learned that protecting a form requires more than just a visible user interface; server-side validation, input filtering, and bot detection are also important. Implementing and testing these protections helped me understand how developers can proactively reduce risks such as spam, XSS, SQL injection attempts, and automated abuse in real-world web applications.
# LetsDefend Alert: Phishing Alerts

## Phishing

Phishing is a social engineering attack designed to to get a user to reveal sensitive information or download malware.

## Alert 1

This alert was generated due to a suspicious email.

<img width="1556" height="762" alt="phishing-alert" src="https://github.com/user-attachments/assets/bfbcc17b-ad80-42ba-9f33-a93095b30804" />

Looking through the specific email, the sender is attempting to get the user to click a link which downloads and attachment.  This is a common way attacks infect machines with malware.

<img width="1085" height="541" alt="phishing-email" src="https://github.com/user-attachments/assets/c46acc11-52da-4fd2-bac1-6d1ca5efb789" />

<img width="1065" height="472" alt="phishing-email-2" src="https://github.com/user-attachments/assets/34999a39-d0f5-491c-b9e8-080f4d687be1" />

After copying the link and posting it into Virus Total, it looks like there's already an entry for this specific attachment.  It's classified as malicious.

<img width="1386" height="882" alt="virus-total" src="https://github.com/user-attachments/assets/888c5ca2-f542-4e77-96ac-7b54b163ab60" />

The sender's IP address is also classified as malicious.

<img width="1433" height="832" alt="virus-total-1" src="https://github.com/user-attachments/assets/651db847-6097-4b7d-87fe-e7fca15632b1" />

Since this email was allowed, we better check the user's machine and see if it's infected.  Using the endpoint security tab, I can see that the "coffee.exe" process is running on the user's machine.  This confirms that the link was clicked and the user's machine is infected.

<img width="982" height="248" alt="endpoint" src="https://github.com/user-attachments/assets/065dd73b-fc85-41cc-92dc-a26f4a241a1b" />


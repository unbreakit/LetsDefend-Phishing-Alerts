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

## Alert 2

This alert was generated due to an email potentially having a malicious attachement.

<img width="947" height="310" alt="Screenshot 2026-11-12 101401" src="https://github.com/user-attachments/assets/b18b7576-70d7-4736-8c71-b8b67865c766" />

<img width="1047" height="221" alt="Screenshot 2026-11-12 101448" src="https://github.com/user-attachments/assets/873b926c-a74b-4277-8fa2-3df0e9db38d2" />

After finding the specific email that generated the alert, I can see that there is in fact an attachment.  It looks like some sort of document.  These can sometimes have malicious macros that are executed when opening the doc.

<img width="903" height="548" alt="Screenshot 2026-11-12 101550" src="https://github.com/user-attachments/assets/b0c7d5cd-a52b-4af3-8eaa-31054a6ff066" />

To find out whether or not this document is malicious, I opened it up in a malware analysis sandbox with AnyRun.  AnyRun flagged the doc as malicous. We can look at the DNS queries that the malware sent out and compare it to our endpoint's outbound traffic to see if there's any similarities.  If there is, it's likely that this doc was opened and the endpoint is infected.  In this case, I can see a DNS request for "royalpalm.lk" and I see that same request on our endpoint so this machine is likely infected.

<img width="1907" height="872" alt="Screenshot 2026-11-12 103738" src="https://github.com/user-attachments/assets/0a91ccda-07a9-4f5e-a29f-0ab4971ef1c0" />


<img width="1457" height="556" alt="Screenshot 2026-11-12 103925" src="https://github.com/user-attachments/assets/53166a1c-3bfc-422c-b349-a0bc981a288a" />

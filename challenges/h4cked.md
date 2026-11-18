# Challenge: H4cked (16-11-2026)

## Incident summary

- The alert: a lot of login failed attempts in a user, a successful one and an upload to the server.
- Verdict: true positive, the attacker brute-forced the password and installed a a reverse shell in the host.

## Investigation timeline

- I did it really manually, I didn't know how to begin, so I watch the packets and I see the brute force attack to ftp, and then the upload of a file to the server. The file was a reverse shell, the attacker use to install a rootkit.
- Then I use Hydra to access the same way to the server and change the reverse shell to become root and see the flag in the Reptile folder(the folder where the repository was installed)
- Before been able to accomplish it, I destroyed the shell.php file and I have to recover it from the templates. I thought about recovering it from the pcap file, but I didn't have it in the attackbox machine.

## Indicators of Compromise (IoCs)

- Compromised account, web shell in /var/www/html

## MITRE ATT&CK mapping

- brute force, web shell, rootkit.

## What was hard / What I learned

- Absolutely everything, this has been my first ever challenge room and I felt really confused.
  I didn't know how to move, what to look for, what tool to use. On other hand, it was my first time using red team tools and doing something about the topic.
- I think that I was more focus on avoiding failure, than I was in discover the problem because it was a safe environment. Although, I have learned something about pentesting an some other things on how to analyse packets to discover brute force attacks.

# Challenge: Juicy Details (18-11-2026)

## Incident summary

- The alert: has been trigered by a network scan and a lot of failed login attempts, also, some hacking tools can be seen in the access logs. 
- Verdict: true positive, the host has suffered a brute force attack and some data have been stolen.

## Investigation timeline

- I filter the logs in search of attack hints an it has been obvious with the first nmap logs in access.log & auth.log and also the multiple failed login attempts
- I go to the access log in search of the tools the attacker used. I looked at the diferent user-agent and spot, nmap, hydra, sqlmap and feroxbuster(it would be easier a script but for my first times i want to get my hands dirty with the logs).
- Then i search the endpoints that was vulnerable to brute force, the one vulnerable to SQL injection and the one that was used to retrieve files, all of them in the access logs by the user agent and the success return of the log.
- Finally, I did a research of the stolen data, the affected files, where did the attacker obtain the credentials and where he did the injection. Also a service and username analisys and that was all.

## Findings

| Type | Value (defanged) | Where I found it | MITRE |
|------|------------------|------------------|-------|
| Attacker IP | 192.168.10.5 | access.log — source IP de las requests sospechosas |  |
| Recon: directory/file scan | feroxbuster (User-Agent) |  | T1595.002 |
| Network service scan | nmap (User-Agent) | access.log | T1595.001 |
| Brute force | hydra (User-Agent) — endpoint /rest/usesr/login | access.log — repetición de POSTs al mismo endpoint | T1110.001 |
| SQL injection | sqlmap — endpoint /rest/products/search | access.log | T1190 |
| Attempted file download | coupons_2013.md.bak, www-data.bak | access.log | T1005 |

## Recommendations

- **Brute force (hydra on the login endpoint):** enforce rate limiting and account lockout on authentication endpoints
- **Attack-tool traffic (nmap/feroxbuster/sqlmap user-agents):** alert on the use of this type of tools in the SIEM
- **SQL injection (sqlmap):** migrate to parameterized queries/prepared statements (in Hibernate/JPA named parameters or PDO in PHP)

## What was hard / What I learned

- At the first time, i don't think about the use of console tools to search the things in the docs.
- I learnt how to look at the logs and what to look for in them.

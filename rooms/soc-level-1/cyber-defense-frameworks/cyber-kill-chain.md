# Room: Cyber Kill Chain (18-11-2026)

## Objective

- To understand the Cyber Kill Chain, and its use to evaluate the security in a network and defend against attacks.

## Key concepts

- The reconnaisance phase in in the chain, the tools(OSINT, email scrappers,...) and how a deep work here can make an attck to be successful
- The weaponization is where the attacker transform the data into tools via malware, exploits and payloads.
- The delivery phase, is when the attacker decide how to infect the victims host here we learn: phising(email with malicious software or links, spear-phising, qhen is directed), usb drop(in public places or sophisticated, when the attacker make it consciously to a company) and watering hole where the victims visits are studied and the attcker clone the website to fool the objective.
- Exploitation is where the attacker make executes code(malicious macro, zero days or CVEs), to detect them you have to look at proccesses spawns, suspicious command line prompts in logs or registry changes or new services created.
- Installation is where the attacker gain persistence, via web shell, modifying services(or executing a payload with a service name, that is known as masquerade), with a backdoor or with add run keys. Usings timestomping he can change the timestamp to clean his trace
- Command & Control, the compromised host would communicate with an external setted up by the attacker(usually the attackers use HTTPS & DNS tunneling)
- Exfiltration is the end, where the attacker can take action on the host(collect credentials, delete backups and shadow copies, make an internal reconnaissance,...)

## Tools / commands used

Queries or commands that mattered (e.g. SPL/KQL syntax, filters).

## What was hard

It is a really theorical room, so I tried to extract all the important things.

Where I got stuck and how I got out.

## MITRE ATT&CK mapping (if any)
N/A

## What I concluded / Assumption I got wrong / What I still don't understand

- Is a must to understand the attack framworks, to know how to react to the diferents actions that the attacker will do and to prevent his next steps
- N/A
- I don't think there's much to missunderstand

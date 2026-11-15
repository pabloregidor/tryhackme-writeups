# Room: Pyramid of pain (15-11-2026)

## Objective

- Learn about the pyramid of pain framework, used to improve cti efficience.

## Key concepts

- the uses of hash to identify malicious software, and how easy it is to change it with only a line append.
- The hash algorithms that have been used and are being used nowadays, as SHA-2 or SHA-3.
- The importance of IP in threat defense(by blocking the host via firewall or deniying packages) and how the atackers manage to change their address with fast flux.
- DNS used by attackers, that is more complex to fake, the use of url-shortening and punycode to fool.(Usually the malicious sites, check the connection to internet or try to launch proccesses to C&C)
- host artiffacts as a way to detect attacks an how it annoy the attackers making them use more resources
- Network artifacts also annoying to the attackers, make them go backwards and rethink. Can be discovered using pcap to see user-agent headers, c2 info, URI patterns
- Tools is the challenging level to the attacker, once you have detect the tools, he has to invest a lot in make another that has potential.
- TTP is the tough level, if you can detect the tacticts,techniques & procedure, you left the attacker almost helpless.

## Tools / commands used

- any.run reports
- MalwareBazaar y Malshare
- SOC Prime Threat Detection Marketplace -> for detection rules
- SSDeep for fuzzy hashing comprobation
- MITRE ATT&CK matrix web, that has the TTPs

## What was hard

The tools level, didn't make sense to me at the beginning.
It is a lot of information that is relevant to proccess

## MITRE ATT&CK mapping (if any)

N/A

## What I concluded / Assumption I got wrong / What I still don't understand

- This topic has to be in mind whenever dealing with an alert.
- I thought it would be way more easy to map the proccess to follow in my mind.
- How to procced during an attack or an alert or how can i detect one, watching the flow of some packages.

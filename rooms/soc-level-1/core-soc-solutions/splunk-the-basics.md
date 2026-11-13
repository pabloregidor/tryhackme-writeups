# Room: Splunk: The basics (12-11-2026)

## Objective
To learn how to add a data log in Splunk, and some basic ways of filtering the data.

## Key concepts
-Splunk stores events in indexes, you query them from the Search & Reporting app.
-Events carry fields that Splunk extracts automatically 
-Basic pipeline: search | stats <function> — filtering happens in the search, aggregation in stats.

## Tools / commands used
index=<index> | stats count by <UserName|Source_IP|Source_Country>

## What was hard
I tried myself to make the filtering command in the way i thought it would work and i failed.
My command was an error itself, i have all the function wrong, so it did nothing.

## MITRE ATT&CK mapping (if any)
N/A

## What I concluded / Assumption I got wrong / What I still don't understand
Concluded:Knowing the software and the good managing of the data, makes you lot more capable.
Assumption:I think this will be an almost useless room.
Dont understand:How to structure the SPL commands, and how to make the logs easy of scrap.

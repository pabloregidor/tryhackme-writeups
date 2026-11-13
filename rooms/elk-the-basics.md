# Room: Elastic Stack: The Basics (13-11-2026)

## Objective

Understand and explore the features of ELK.
Investaigate VPN logs to identify anomalies.

## Key concepts

- ELBK components and essentials.
- Filter creation and KQL
- The use and creation of dashboards and graphs to manage data

## Tools / commands used

- Kibana date filter top right
- Kibana add filter options
- Kibana visualization creation and compose tables

```bash
  Source_Country : "United States" and UserName : "James" or UserName : "Albert"
  UserName : "John Brown"
```

## What was hard

- I didn't know how to see only the data from one day, i finally figured out that it was clicking in the date chart
- I have not been able to create a KQL query to filter by the timestamp.

## MITRE ATT&CK mapping (if any)

N/A

## What I concluded / Assumption I got wrong / What I still don't understand

- That a good use of the tools, make you more capable and efficient.
- That ELK was another almost prehistorical tool impossible to understand and would make my life a hell.
- What the KQL queries are capable of.

## Other commands teached

- Logical operators: AND, OR and NOT
- wildcard query: * (like SQL)
- Field:value -> to search a value in a field

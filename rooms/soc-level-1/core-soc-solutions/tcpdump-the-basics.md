# Room: TCPDUMP: The Basics (12-11-2026)

## Objective

Learn how to capture, save and managed captured packets from tcpdump.
Lear the useeful commands that let us control de app.

## Key concepts

How the packets can be read and the numerous options that you have to find the pieces of information that you need.
its basically an introduction to the terminal packet reading apps.

## Tools / commands used

```bash
- wc -l(Para contar la salida de otro comando)
- tcpdump   -nn(Tell to the app to not resolve DNS and PORT, -n is for only DNS)
            -vvv(Make the response more verbose whit each "v" until three of them)
            -i INTERFACE(The app will begin to hear that interface. any, will capture all of them)
            -w FILE(Will save the packets heared in that file, usually a .pcap)
            -r FILE(Let you read the packets in a file)
            -c COUNT(Tell the app, how many packets you want to hear)
  FILTERS:  <src/dst>(To filter between source or destiny in other filters)
            host IP(Filter by IP)
            port PORT(filter by PORT)
            PROTOCOL(filter by PROTOCOL)
  OTHER:    greater LENGTH(More than LENGTH bytes)
            less LENGTH(Less than LENGTH bytes)
            proto[expr:size](proto = PROTOCOL, expr=OFFSET, size=BYTES INTERESTING)
            tcp[tcpflags]
  LOGICAL:  <and/or/not>
  BINARY:   <&,|,!>

  DISPLAY:  -q(Quick display)
            -xx(Hexadecimal)
            -A(ascii)
            -e(Link level header info)
            -X(Hexadecimal and ascii)

tcpdump -r traffic.pcap "tcp[tcpflags] == tcp-rst"
```

## What was hard

I forgot to use the logical operators in the construction of the filters.
I didn't know how to see the first DNS query, because i didn't think where i should capture.
I try to imagine myself how to filter by tcpflags and i got wrong.

## MITRE ATT&CK mapping (if any)

N/A

## What I concluded / Assumption I got wrong / What I still don't understand

- tcpdump is an incredibly powerfull app that might be really usefull to see what happened in a communication between hosts or troubleshooting in a network.
- i did not know the existence of this app so i dindn't assume anything.
- isn't this do the same that wireshark can do?

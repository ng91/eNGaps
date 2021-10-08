# eNGaps  
Lightweight software tool for encapsulating IP traffic  
into embedded data modems, wire/wireless links.

## Why?  
Big industries use vendor-specific, closed-source devices difficult  
to even operate without using whole vendor ecosystem.  
This device solves that problem, making data tunneling over serial link  
(and then wire or radio transmission) possible.

## What is that?  
This software makes use of:
* TUN/TAP device driver
* Threads  
It consist of:
* Decoding and encoding of network packet
* Custom but non-proprietary protocol  
for serial line transmission  
* Basic mechanism for error detection(TBD)


# eNGaps  
Lightweight software tool for encapsulating IP traffic  
into embedded data modems, wire/wireless links.

## Why?  
Big industries use vendor-specific, closed-source devices difficult  
to even operate without using whole vendor ecosystem.  
This device solves that problem, making data tunneling over serial link  
(and then wire or radio transmission) possible, even by end user.

## What is that?  

This software makes use of:
* TUN/TAP device driver
* Threads    

It consist of:
* Decoding and encoding of network packet
* Custom but non-proprietary protocol  
for serial line transmission  
* Basic mechanism for error detection(TBD)

## The protocol  

90 | LEN2 LEN1 | NUM2 NUM1 | DATAGRAM ... DATAGRAM_END | 90        (numbers in DEC)  
  
* every entry is one byte(excluding "|", and "()" signs).  
* symbol 90 is reserved and cannot occur in any part of packet
* if 90 occurs, the SPECIAL_CHARACTER(89) and then HIDDEN_PREAMB(02) is introduced instead  
* if 89 occurs, the SPECIAL_CHARACTER(89) and then HIDDEN89(01) is introduced instead  

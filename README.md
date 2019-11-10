
# Implementation-of-Eifel-Retransmission-Timer-ns-3

## Course Code: CO300

## Assignment: # 5

### Overview

Eifel retransmission timer is an alternative to the default Retransmission TimeOut (RTO) mechanism of TCP. Instead of using two constants like TCP retransmission timer: alpha and beta, Eifel retransmission timer uses one constant called gamma. Gamma is defined as a ratio between current sample of RTT and RTO. Depending on the value of gamma, the value of RTO is calculated. This project aims to implement Eifel retransmission timer in ns-3.

### Simulating Eifel

To simulate Eifel algorithm, the attribute eifel must be set to true, as shown below:

`Config::SetDefault("ns3::TcpSocketBase::Eifel",BooleanValue(true));
 Config::SetDefault("ns3::RttMeanDeviation::Eifel",BooleanValue(true));`

### Eifel example

An example program for Eifel has been provided in

`scratch/tcp-variants-comparison.cc`

and should be executed as

`./waf --run "scratch/tcp-variants-comparison -tracing=true -eifel=true"`

### References:

[1] R. Ludwig and K. Sklower. 2000. The Eifel retransmission timer. _SIGCOMM Comput. Commun. Rev._ 30, 3 (July 2000), 17-27. DOI=http://dx.doi.org/10.1145/382179.383014

[2] The Eifel Detection Algorithm for TCP (RFC 3522)
(Link: ​ [https://www.rfc-editor.org/rfc/rfc3522.txt](https://www.rfc-editor.org/rfc/rfc3522.txt)​ )

[3]  [https://www.nsnam.org/ns-3-29/](https://www.nsnam.org/ns-3-25/)

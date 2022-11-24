## Definitions
**Hamnet**: HAM network, not reachable from internet, often used for HF links
**44net**: internet routable network, used for ham services that need to be reachable from inet

## Goal

Minimize the overall number of internet routable subnets. This is part of a deal with the German? hamnet folks.

## Proposal
- each site uses their normal internet upstream (nat) for anything default route that is not specifically announced for 44 (as we choose)
- we remove the default route announced by LX0BGP, announce only 44 addresses 
- use a single routing table on the spokes, remove (most/all) routing rules
- identify what services we want to expose that need to be reachable from the internet, if any
- for services that need to be reached from internet, use a specific ip range, and either routing rules or a separate router on the sites that need it

## Next action
- Sam to experiment on rtr-16.lx2sg....
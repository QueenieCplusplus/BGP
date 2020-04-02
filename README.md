# BGP

# eBGP

eBGP exchanges routes between ASs. And it is commonly used between enterprises and their service providers.


          AS100                AS200              AS300
            R1                   R2                 R3
            
            
            
                                  R
                               /      \
                             peer      peer
                            /    iBGP    \     
                          R ---  peer ---  R 
                                
                                AS500






# iBGP(Peering), IGB and eBGB

it is a term that describes the peering between BGP neighbors in the same AS. It is usually used in transit ASs. Transit ASs means to forward traffic from one external AS to another AS. 

If the transit AS does not use above mentioned iBGP, then it will be bothering to set up to let Router be into IGB via Redistribution, and the into another eBGP router also using Redistribution.

# PBR (Redistribution)

to use PBR to change the addr ot the IP packets based on policy.


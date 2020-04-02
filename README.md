# BGP characters

1. Interdomain routing protocol

2. use TCP port 179 to establish connections with BGP neighbors.

3. iBGP for internal neibour, within the same AS.

4. eBGP for external neibour, usually the enterprise - service provider.

# BGP Decision Process

By default, BGP will select only one path to reach the des, unless admin specifies it to max paths.

When the path is selected, then BGP puts the selected one into the routing table and propagates to its neighbors.

# Best Path Selector

the algorithm looks like this:

1.

2.

3.

4.

5.

6.

7.

8.

9.

10.

11.


# BGP Neibors

 
           AS300 R ------- R  AS100  R ------- R AS400
           
                                R
                                |
                                |
                                |
                                R
           
                               AS200



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


               USA R          iBGP Core         R JP
               IGP                                IGP  
                   R                            R 
               
                              R      R
                               Africa
                                IGP

# BGP Optimization using Metrics

1. Use confederation (結盟) to reduce BGP Peering Overhead.

2. Use Route Reflectors to reduce BGP Peering Overhead.

3. Use MED to influence Inbound Traffic.

4. Use Weight to influnce Outbound Traffic's path from a router which is configed locally.


# PBR (Redistribution)

to use PBR to change the addr ot the IP packets based on policy.


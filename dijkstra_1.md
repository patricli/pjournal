# Edsger W. Dijkstra

Jan 29, 2021

_Progress is possible only if we train ourselves to think about programs without think‐
ing of them as pieces of executable code._
—Edsger W. Dijkstra, August 1979

A friend recently brought up Dijkstra who I best know for the Dijkstra Algorithm to calculate the shortest path in routing.  This goes back to my OSPF days when I was learning about networking.  It is a bit rusty but perfect time to revisit what I knew (or thought I knew).

According to Wikipedia (https://en.wikipedia.org/wiki/Edsger_W._Dijkstra#Algorithmic_work) Dijkstra was a pioneer in computing science but originally trained as a theoretical physicist. It seems his research covered many areas in computer science with a key contribution to driving the "structured programming" approach is writing better computer programs.  He also made tremedous contributions to distributed computing and concurrency programming.  This fascinates me recently because I have come to draw parallels between two areas: routing and blockchain.

Routing maintains a table of known routes in the network and stores it in each node.  It is inheritently distributed.  With the OSPF routing protocol, each node keeps the link state of all known routes.  With the EIGRP protocol, each know records to routes from "their point of view".  Routing information is propogated from node to node by multicast.  There are quite a few similarities with Blockchain but I must remember that they are related but not exactly the same.  They are both inheritently distributed systems and hence must tackle similar challenges (sharing data, learning existence of nodes, recovery, etc) so they are helpful to build a mental model of distributed systems and what are good questions to ask.

So back to the Dijkstra Algorithm.  It allows one to calculate the shortest path between two nodes and by extension, the shortest distance from  a fixed node (you are here) to all other given nodes in the graph.  (This probably relates to graphDB and DAG which I want to investigate in the future.  Also applied in AI to uniform search costs.)

The fundamental computer science definition is too challenging for me at the moment, but it helps me if I review the application to routing and OSPF.  To calculate the shortest path between two nodes, we first need to understand costs.  The cost of the link connecting two adjacent nodes = Reference bandwidth / interface bandwidth in bps.  In Cisco, the reference bandwidth is set to 100 Mbps.  And per the algo, cost is always a positive integer.  Now to get the shortest path from a given point to any node in the network, add up the costs of the links for all possible paths and keep the lowest cost path.  If this is calculated serially, we can drop any routes that cost more than our current shortest path.  Lowest cost should eliminate any paths with a loop.  If two paths cost the same, then OSPF will use ECMP.






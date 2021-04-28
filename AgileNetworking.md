**Can the networking team operate in the agile methology?**

With the Agile principles stated as: <br>
 Individuals and interactions over processes and tools <br>
 Working software over comprehensive documentation <br>
 Customer collaboration over contract negotiation <br>
 Responding to change over following a plan <br>
 
I do believe as network engineers we have always tried to follow these principles.  Strong network engineers and architects have always been essential to solve networking challenges.  We rely on them to create the standard network designs and templates to be used wherever possible but also to have the knowledge of when to deviate from them.  

A working network over comprehensive documentation - the engineers make adjustments to the plan as needed.  Only one floor instead of 5 floors?  Only a 512kps connection instead of 100Mps?  Sites tend to vary in different ways across offices.

Customer collaboration over contract negotiation - always try to do proper customer requirements gathering before designing the network.

Responding to change over following a plan - see number 2.  Well, it depends.... networking should not be organic because it is a distributed system.  Standard templates allow for better design practices and more reliable maintenance and troubleshooting.  We try to follow the plan as much as possible but the plan is also designed with flexibility to allow for some different situations.  
 

**Does that mean the network team acts as part of an agile cross functional team?**

It depends on the objective.  If the objective is to develop new software, I would say networking should not be part of the cross functional team but they should be consulted as SME's.  Most of the development work would not involve networking so it does not make sense as a use of their time.  (If the application is network centric, the situation may warrant a full time network engineer).  Instead, the network team should empower the software team by creating consumable offerings or service packages on top of their network platform.  This may be an offering for the high transaction, low data network policy or a real-time communication network policy.

If the objective is to design an enterprise architecture which would create the platform for others to move agiley upon, then yes the network team would be vital to the cross functional team.  However, they may have their own lane to work on but still in collaboration with the other disciplines.


**Does that mean the network team builds networks in an agile method?**

I feel there are definitely some aspects of the agile work process that are well incorporated with networking and other distributed platform services but other practices that apply well to an instance of an application that cannot be used on a broad platform service.

When building a network we do configure it iterately.  We check for L1/L2 connectivity first, then check for L3 connectivity.  We then incrementally add the configuration for particular services like multicast or QOS.  However, we would not just set up L2 connectivity, have users start working on the network, and then come back in two weeks to add IP routing.  Once we have the core set up properly, when we add the access layer, it goes very quickly to get the whole switch configured.  When we have a well designed template, we might even push out the entire configuration through zero touch deployment.  This is important because there are many sites that may not have any technical staff available.  

A key distinction may be that we are not doing development at this point but just focused on deployment.  Once you have something well defined, it does not make as much sense to slowly iterate.  Instead, you can take bigger steps with something that is known to work.  

Another difference is that developing a piece of software is more or less self contained (especially in a loosely coupled architecture).  The network however is a shared resource with a huge blast radius.  It is just easier to blow up and redeploy a microservice than to take down the network.  




Individuals and interactions over processes and tools <br>
Working software over comprehensive documentation <br>
Customer collaboration over contract negotiation <br>
Responding to change over following a plan <br>

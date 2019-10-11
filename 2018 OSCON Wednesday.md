# Introduction

I prefer to take a lot of notes when I attend confernces then summarize when I get back to work.   This helps me focus during the conference and iterates the knowledge.   Others might enjoy the information as well. 

Acronyms used:   



*   OS = Open Source
*   Innersource = Like OS but only within the company boundary
*   ML = Machine Learning
*   **Kubernetes**, also sometimes called **K8S** (K – eight characters – S)

[The O'Reilly OSCON site.](https://conferences.oreilly.com/oscon/oscon-or/schedule/2018-07-18)

**A collection of things to read:**


<table>
  <tr>
   <td><strong>Reading (who recommended)</strong>
   </td>
   <td><strong>Why</strong>
   </td>
  </tr>
  <tr>
   <td><a href="https://aws.amazon.com/opensource">opensource.amazon.com</a> (AWS)
   </td>
   <td>AWS team has a dedicated team for OS. That means cool tools and whatnot.
   </td>
  </tr>
  <tr>
   <td><a href="https://www.ethereum.org/">https://www.ethereum.org/</a> (Puppet)
   </td>
   <td>Blockchain knowledge. Everyone is excited about blockchain!
   </td>
  </tr>
  <tr>
   <td><a href="https://en.wikipedia.org/wiki/Byzantine_fault_tolerance">Byzantine fault tolerance</a>
   </td>
   <td>Blockchain logic on how to protect muti use of a block
   </td>
  </tr>
  <tr>
   <td><a href="https://www.weforum.org/whitepapers/blockchain-beyond-the-hype">Blockchain Beyond the Hype | World Economic Forum</a>
   </td>
   <td>Blockchain reading for those interested in the practical aspect of BlockChain
   </td>
  </tr>
  <tr>
   <td><a href="https://en.bitcoin.https//en.bitcoin.it/wiki/Nonceit/wiki/Nonce">Nonce</a>
   </td>
   <td>The idea of a bitcoin mining and how miners resolve blockchains
   </td>
  </tr>
  <tr>
   <td><a href="https://aws.amazon.com/sagemaker/">AWS SageMaker</a> (AWS)
   </td>
   <td>Machine learning project from AWS OS team.
   </td>
  </tr>
  <tr>
   <td><a href="https://aws.amazon.com/rds/aurora/">AWS Aurora</a> Relational DB
   </td>
   <td>A relational DB "built for the cloud" by your friends at AWS.
   </td>
  </tr>
  <tr>
   <td>AWS EKS: <a href="https://aws.amazon.com/eks/">Elastic Container Services for Kubernetes</a>
   </td>
   <td>Let AWS manage your Kubernetes solution
   </td>
  </tr>
  <tr>
   <td><a href="https://aws.amazon.com/blogs/opensource/kube-aws/">Kube-AWS OS project</a> (CoreOS)
   </td>
   <td>Incubator project on secure kubernetes solution.
   </td>
  </tr>
  <tr>
   <td><a href="https://nvlpubs.nist.gov/nistpubs/specialpublications/nist.sp.800-190.pdf">Application Container Security Guide</a>
   </td>
   <td>63 page reading NIST doc. a <span style="text-decoration:underline;">MUST</span> read for companies migrating to Containers.
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/99designs/aws-vault">AWS Vault</a>, <a href="https://aws.amazon.com/quickstart/architecture/vault/">HashiCorp Vault on AWS</a>
   </td>
   <td>Secrets management systems.
   </td>
  </tr>
  <tr>
   <td><a href="http://cri-o.io/">Cri IO</a>
   </td>
   <td>LIghtweight container runtime for kubernetes
   </td>
  </tr>
  <tr>
   <td><a href="https://www.tensorflow.org/">TensorFlow</a>
   </td>
   <td>ML, Deep Learning. Referenced multiple times in OSCON.
   </td>
  </tr>
  <tr>
   <td><a href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html">AWS Elastic Network Interface</a>(Pinterest)
   </td>
   <td>Pinterest used this for their container implementation (migration to the cloud)
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/Huawei-PaaS/CNI-Genie/blob/master/docs/multiple-cni-plugins/README.md">CNI Genie</a>
   </td>
   <td>Heavy theory around container networking.
   </td>
  </tr>
</table>



### **KeyNote (Wed Morning)**

The keynote sessions are high level and not worth detailing other than some high level ideas.   The major win on this keynote was Tim OReilly presenting at the end of the keynote session.

Some interesting notes



*   AWS is promoting Open Source and Cloud.   Check out: 
*   "Open Source won the battle between Open Source and Microsoft".     This is fairly heady idea for those of use that have been tech for a long time.
*   BlockChain is emerging.    A particularly interesting use will be political voting.  Lots of new companies in this space (presenting at OSCON!)
*   Tim Oreily keynote: \

    *   **<span style="text-decoration:underline;">Inclusive societies prosper,  Exclusive societies falter</span>**
        *   A product is taken over by a company once they prosper.  The microsoft story.    
    *   Continuously learning by doing \

        *   This relates to how devs need to get new skills or become stale.  This leads to happiness or misery depending on Devs ability to learn new skills.    The Cloud enables Devs to play with a wide variety of things... like docker for instance!
*   


### **Session - An introduction to blockchains (Lucy Wyman, Puppet)**

She covered the idea of blockchains being linked lists with trust relationship via Asymetric Encryption (Public, Private Keys).   A block has a cryptographic hash of the previous block as well as Data.  The hash of a block causes linkage uniqueness.    

What happens when 2 consumers utilize the same available block at the same time?  BlockChains utilize the idea of "Byzantine Fault Tolerant".   Higher level choice is used to discriminate (would need to dig into this).   

"Proof of Work" and "Proof of Stake".   The idea of validating a block within a blockchain

Nonce: An aspect of how bitcoin miners resolve blockchains


### **Session - Open source at AWS: Code, contributions, collaboration, and communication**

The idea of embracing the Open Source communities.   AWS has a belief that corporations and users should join communities.

The AWS OS team seems focused on evolving Machine Learning.

There are ML frameworks emerging from the AWS OS team - completely OS!

The idea:    Build your AWS ML system, train it, deploy it.

May want to read up on "Aurora" DB.  

AWS is selling a DB migration tool that may be useful for getting off legacy RDMS... like sql server.

AWS is selling a "Run Kubernetes For Me" solution.    EKS - Enterprise Kubernetes Services.

AWS said "Go read Secure AWS Kubernetes".   I believe that leads to Kube-AWS.


### **Session - NIST container security standards**

Containers still have the computational semantics of a VM and the security considerations are the same as VMs.  However, there are new considerations due to the architecture of container technology.

Its highly advisable to read the "Application Container Security Guide" for companies migrating to container technology

Containers are immutable - If you destroy a container and start a new one, it is a different container (with a new ID).   (JB: ala Java Strings)

Orchestrator idea:   Gets image from registry, push to environments, eventually prod



*   This seems like the core of **Continuous Delivery - Research more.  Is Kubernetes how one implements CD?**

Security Considerations:



*   Can a bad image be injected into your registry?
*   Remove items from your image that arent needed
*   do NOT embed secrets in your image
*   Is 3rd part image trustable?
*   Are there insecure connections to your registry?

Orchestrator Risks



*   Poorly separated inter container network traffic
*   a bad node gets into the cluster
*   Containers should be isolated at the OS kernal level (multi containers on 1 docker engine - will have separation unless you screw this up)
*   App vulnerabilities (same old same old)
*   Rogue Containers in prod - happens when dev debugs a container in prod
*   Improper User access rights - same old same old.   Lock system down to only those who need access
*   Host OS file system tampering

Recommendations



*   Use vulnerability management tools
*   Adopt tools and processes early on (governance!)
*   Only use base image from trusted source
    *   NodeJS example:    Use the super simple linux image that has linux stripped down and just runs nodejs.
*   Store secrets outside of your container
*   Only connect to registries over secure, encrypted channels
*   Its probably a good idea to research AWS Vault implementations
*   Regularly update your image version
*   Lock down who can authenticate to your Orchestrator
*   Lock down by networks, specific hosts, etc.
*   Design your Container layout with Isolation in mind.
*   Isolate your container environements (Dev, QA, Prod)
*   Containers should only be run with their root dir in Read Only mode.   
    *   This explains why linux admins must run chmod,chgrp, chown on new code setup. Linux is locked down out of the box.
*   Lock your Host down
*   Use Container Specific OS.   Example:   A linux version that only runs NodeJS
*   Watch Audit logs
*   Reduce permissions to the containers.


### **Session - Pinterest's journey from VMs to containers in the public cloud**

The presenter went over the Pinterest solution - Pins and Boards.  Huge amount of Pins related to Boards.    Board suggestions are derived with massive data computation.    They are currently at 175 Pb (Peta Bytes!).    The massive computation allows pinterest to recommend a pin to a user

The problem:    Product Engrs were spending time writing deployment code and infrastructure code.   They wanted devs to not have to worry about this (ie, dont have to deal with puppet scripts).   

Goals:



*   automate infrastructure
*   automate governance

They chose to move to containers.   They realized they needed the right tools and services.  "How to Docker" needed to be solved.   They also needed to choose an orchestrator.   They tested Kubernetes, ECS, and other orchestrators.   They chose Kubernetes.   He recommended tackling simple applications first (maybe tackle Harvester?).

K8s challenges



*   Security - who gets access to what?
*   Offer dedicated and shared solutions to their customers
*   How to get metrics and logging (for isolation)
*   Governance - how are people spending money on cloud resources.  Ie, what are the costs associated with cloud solution for each customer.

The guy recommends using IAM roles with K8 Yaml

They used a branch of ECS called ENI (??? Get back to)

Major use of Kubernetes:   Submission of huge ML jobs to the K8 managed cluster.


### **Session - Multiple networks and isolation in Kubernetes**

This was the worst session of both days.    The guy was very engrossed in Network theory.  enough said.

CNI - Common container network interface

Multiple Physical Network

Multiple Logical Network 

Network Tenancy - What is in what network?   Who is the tenant?


### **Session - Clean Code**

This was a guy who had been in the industry for a while.   

Code is for others to read that drives a computer

Clean code is testable

Martin Fowlers book (Late 90s?) on coding

"Copy and Paste is a design error"

SLAP:   Single Level of Abstraction (he demoed breaking method into 2 methods and why)

Unclean code ages quickly

"Code Smells"

Our mind can only process 1.6 things at a time.   When you are in the office coding, you get overloaded because Coding+PeopleTalkingToYou = 2

Open spaces leads to unclean code

Companies dont value the SW Dev "Craftmanship".  Good developers are Craftsman

Bad: 



*   Outsource Dev to lowest bidder
*   Complex code
*   a senior person always being a Hero (Heroism)

Make sure to educate your manager

Metrics:   Be very careful using these.  People will focus on the metric at a cost of doing the right thing.  

What do you need to produce code    What tools?

You must mandate peer reviews

Develop Innersourcing

Respect the reviewers

Dont accept unclean code

Mentor junior Devs

Use Apprenticeship model - thats your (old guys) lasting legacy.  Limit to 6 months


# Conclusion

Onto Day 2 (Thursday)


<!-- Docs to Markdown version 1.0β17 -->

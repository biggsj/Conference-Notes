# Introduction

Second day of OSCON

**A collection of things to read:**


<table>
  <tr>
   <td><strong>Reading (who recommended)</strong>
   </td>
   <td><strong>Why</strong>
   </td>
  </tr>
  <tr>
   <td><a href="https://developer.mozilla.org/en-US/">M</a>DN from Mozilla
   </td>
   <td>A useful developer network?
   </td>
  </tr>
  <tr>
   <td><a href="https://www.nginx.com/blog/what-is-a-service-mesh/">Service Mesh</a>
   </td>
   <td>This came up multiple times in OSCON
   </td>
  </tr>
  <tr>
   <td><a href="https://about.gitlab.com/">Gitlab</a>
   </td>
   <td>Automated Devops (CI and CD)?
   </td>
  </tr>
  <tr>
   <td><a href="https://en.wikipedia.org/wiki/Monad_(functional_programming)">Monads (wiki)</a>
   </td>
   <td>Referenced in a talk.
   </td>
  </tr>
  <tr>
   <td><a href="https://javascript.info/async-await">Async and Await</a>
   </td>
   <td>Awesome framework for multi thread lib. A must learn.
   </td>
  </tr>
  <tr>
   <td><a href="https://blog.stephencleary.com/2013/11/there-is-no-thread.html">There is no thread</a>
   </td>
   <td>Read for Async and Await foundation.
   </td>
  </tr>
  <tr>
   <td><a href="https://en.wikipedia.org/wiki/Border_Gateway_Protocol">BGP - Border Gateway Protocol wiki</a>
   </td>
   <td>This is the backbone details of the internet
   </td>
  </tr>
  <tr>
   <td><a href="https://www.nginx.com/products/nginx-unit/">Nginx Unit</a>
   </td>
   <td>Dynamic Web and App server. This is being developed by the nginx team.
   </td>
  </tr>
</table>



### **KeyNote (Thur Morning)**

This keynote was full of 10-15 minute presenters.    Health bio app, Vets who code, Social Engr

Kubernetes solutions are massively on the rise in terms of usage.   

Python and Go languages are also on the rise in terms of usage

Google Cloud:   "Open Source Project" and "Open Source Code" (look into?)

IBM:   Presentation on Quantum computing.    Can play around with QI kit.   Can explore real world details "Quantum Experience".


### **Session - Conquering serverless: Solutions for organizations**

There are a lot of "niggles" to make it work.   The idea is a chain functions are called, based on some kind of initiation (listener, etc).    

Access and permissions are painful for Serverless.   Have to specify IAM config a lot.

Options for locking down:



*   Write config
*   lets devs create roles/permissions
*   Automate
    *   Framework based approach (faster development, less errors)

<span style="text-decoration:underline;">Serverless - only pay for when functions are used.</span>

EC2 - lets say a web app costs $50/month.     Serverless would likely be free, but its hard to setup

Testing



*   Unit tests same as always
*   Integration Tests - Cloud testing great because you can change facets
    *   "Service Fakes" allow you to test offline
    *   Not many building blocks for Fakes (yet)
*   Best to test in the Cloud

Monitoring



*   how to instrument code?
*   He instrumented code by using an instrumented handler

Logging



*   Isnt very good.   Most use Splunk or Rollbar logging \


Tracing - use cloud provider.  "Epsigon is coming".


### **Session - Mozilla’s journey from the data center to the cloud**

Had to come up with "Rules of the Road".     



*   IT only supports AWS (no local hosting?)
*   Need Elastic
*   Need Multi Region
*   Must have a CI and CD mindset
*   Who will move Apps to the cloud?    ie, assign responsibilities
*   Need to use a Devops mentality

**People are Everything (ie, employees are highest value to the business).**

**People must collaborate**

**Every team is a learning and teaching team**

**Toxic Behavior is Contagious and Cancerous**

**<span style="text-decoration:underline;">Concluded that they needed to create a Devops team</span>**


### **Session - What worked for Netflix may not work for you: Expedia's story**

"Cloud Native" apps.    When converting to the cloud, you may want to evolve your apps first before the move (ie, Dockerize first, cloud second)

How to move to the cloud:



*   Invest to drive rate of change (training)
*   Know the landscape of your apps.   Which are easy to migrate, which arent

Considerations when moving to the cloud



*   New services implementation should be cloud ready (ie, docker)
*   Consider Replatform - untangle your complex app
*   Lift and Shift - tradeoff between replatform and acceptance of the current state
*   Deprecate
*   Move and Tune - go quickly to the cloud and deal with problems as they arise

How do you sequence micro services?

Cloud Native



*   embrace cloud service ecosystem
*   Is your cloud spending measureable?
*   Is your cloud spending manageable?

Run redundant domains for resilience.

Create "Guardrails"



*   automate as much as possible
*   Practice finance governance

Know how to get Unstuck



*   team evolution 
*   Ambiguity gets you stuck:   What can I do?   Learn to say Yes.  Challenge constraints

Summary



*   **Organic migrations dont work - Approach as a Big Boulder**
*   **Embrace multi tenant designs **
*   **Quickly Learn what to centralize and standardize and what not to.**
*   **accommodate security**
*   **Realize that Costs will hit you in the face - Build cost governance**
*   **articulate yoru GuardRails**
*   **Learn to disambiguate quickly**
*   **Expedia focuses on learning and training**
    *   **Encourage and Support**
*   **Important to get experimentation going**


### **Session - The async invasion**

AA = Async and Await

The async revolution

Javascript adopted in 2017

"Async and Await is Taking Over"!!!     The AA is a really cool paradigm for programming multi thread.

Async value - Mobile UIs, Cloud Servers

Async evolution:



*   None (semaphors?)
*   Event listeners (painful writing error handlers)
*   Callbacks (nodejs does this)
*   Futures (cool idea - can join futures to create "all futures must complete").
*   Async and Await
    *   It IS a futures implementation
    *   He did a demo around how Async and Await code looks very much like Sync code.   It was pretty neat


### **Session - Containers and anycast IPs at DigitalOcean**

This was another VERY heady presentation and hard to keep up with.    When you start talking large scale container networking, the conversation will quickly become complex.   The summary of this presentation was that docker networking has certain ovehead and causes network latency.   You can do a deep dive into kubernetes and BGP to increase network throughput but its a very heady topic.

Network Name Spaces

Docker networking code is glue code for common linux networking

Kubernetes Pods, Cluster (zzzz)

Kubernetes Services.

Look into linux IPTables

Spline - Leaf datacenter architecture

Core - Spine - Leaf becomes "Zones".    You have to scale out due to network switch limitations

BGP - Border Gateway Protocol



*   Figures out how to route packets
*   This is how the internet works

BGP autonomous systems

Kube- router

Can use Anycast IPs now

Summary



*   BGP + kubernetes works
*   Anycast + kubernetes services IPs are a powerful combo
*   Improved Perf for 100s of apps


### **Session - NGINX Unit - how to use the fully dynamic new server**

Application Landscape:   Olden times - IT built walls to assure quality but that caused massive delivery delays.  Now we can start containers fast and use Devops tools to perform actions (delivery, patching, etc).

Microserver Trends:   Tough for connectivity (lots of connections), Legacy apps are modernized, Its not always right to do microservices

Security is different:   Apps tend to be isolated (Firewalls), Apps should be restricted, Complicated request flows cause perf issues.  Perf issues become more complex

nginx unit - built from scratch (its NOT a fork of nginx).   It came out supporting PHP, Python, and Perl.   Its evolving into supporting other languages

Same Applayer across App stacks

Nginx Unit:



*   Implemented using Unix Sockets by default
*   Uses JSON for config

Future:   Increase community usage.  Hardening and Maturity.  Scalability, Support other languages.


# Conclusion

Create interest groups at Vesta

Should we have an Initiative "Create Devops Culture"?



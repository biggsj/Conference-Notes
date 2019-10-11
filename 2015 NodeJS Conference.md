# Node Interactive Conference 2015

### Summary:  
This conference focused on the current state of NodeJS which included both core nodeJS and related nodeJS activity.   The conference started with all attendees listening to keynote speakers in a common ballroom.   After the first few hours, attendees chosed 1 of 3 parallel presentations to attend meaning you couldnt attend 2 of the 3.    1 of 3 presentations focused on the "Internet of Things" or IOT.  I mostly stayed away from the IOT presentations.   The following is a summary of each presentation which I attended.   The conferences schedule will probably not be available over time but its available as of Dec 2105.
# Day 1
### Session:  convergence-evolving-nodejs-with-open-governance-and-an-open-community-james-snell-ibm
Node has significantly evolved since our first Vesta-Nagios implementation (0.10).   It is now up to v5.2 and there was a merge of two complimentary projects - nodejs and io.js.   Standalone Node, meaning no modules, scored an A+ on security via the SSL Labs cert process.   Node has evolved into a stabilized product which includes:

Changing ownership from a private company, Joyent, into an open source committee
Release frequency - every 6 months 
Note:   v0.12 support will expire in 2016.   This could impact vesta so we'll want to upgrade our node version.

### Session:   The World is being Reinvented in Code- Jason Gartner, IBM
APIs are the next "Killer App".   IBM Bought StrongLoop which is an Enterprise NodeJS solution.     IBM itself has 170+ NodeJS instances.  IBMs plans to build NodeJS APIs for people to use (JB:  not sure of the open source mode here!).    IBM has a concept of "API Harmony" which is the idea of finding the best API to do the job.  IBM think that API business will be $2.2Trilliion by 2018 which will include major industries like banking, healthcare, etc.

### Session:  Node.js at Uber - Tom Croucher, Uber
The theme here was how Uber used node.   "Everyone" should read The Platform Rant by Steve Yegge.  The ExpressJS framework was mentioned a second time at this point of conference.  There is an obvious concept of RAD web sites built with Express.   TChannel, a "network multiplexing and framing protocol for RPC" was mentioned.

### Session:   Node.js and npm by Numbers - Ashley Williams, npm
NPM is a company ran by the founder of npm.   "By the Numbers" meant Ashley presented a lot of charts showing how npm is expoding in terms of usage.   Im assuming the reader of these notes understands how npm fits into the node solution.  npm is to node as cpan is to perl.   There are 1.8 million events/day where each event is a pull of around 70 node_modules.    npm has exploded - about half of its all time downloads have occurred in the past 3 months:   =exponential growth.   330 packages are uploaded per day.  NPM has a definitions (fwiw):   Publishers:  These are somewhat flat lining.   Others defs that I didnt write down.    As of now, npm has ~200K packages.   NPM is the largest package management sytsem in the world.  Im not sure in what comparison that is.  Is it bigger than CPAN?   Measured in terms of downloads?   Quantity?    

### Session:  Serving the Node.js Enterprise, Thus Serving the Community - Joe McCann, NodeSource
This session was a CEO presenting his vision of the node future.    NodeSource is an early adopter (2009) of node and who wrote a variety of tools for node including perf tools.  This hope node dev will double each year and believes node is the biggest enterprise development shift in the past 10 years.   A flagship project of this company is called nsolid which is a tool for node performance analysis.    JB:   Its interesting what you get with node debugging VS what you get from nsolid.    nsolid wraps nodejs and gives you profiling, heap snapshots, etc.  This session introduced a buzz word that was brought up muliple times in the conference:  "Flame Graphs" which have enormous value for finding perf issues but are rather complex.   nsolid is FREE for development.     He mentioned EnterpriseJS.io which is "a community focused on elevating javascript development for the enterprise through collaboration, conversation, and education.".    He stated that "massive big companies are using node".    

### Session:   Streams and You: A Love Story - Calvin Metcalf, App Geo
This session was primarily a focus on the node streams library and was a bit... slow.   THe take away here was to consider how Streams v1,v2,v3 have evolved.

### Session:  Scripto JavaScript and the Internet of Things - Andrew Chalkley, Treehouse
Oops.  I went to an IOT session for the first and last time.   The big issue here is IOT is emerging and is very, very new.   Here are the new, Cheap embedded devices:

* Tessel2
* Rasperry PI
* C.H.I.P.
The newest RasperryPi is $5 (called Rasperry Pi ZERO).    It does require an SD card.  http://www.slideshare.net/yunongx/debugging-node-in-prod

### Session:  Debugging Node.js in Production - Yunong Xiao - Netfilx
This presenter is very bright and went through his technique of root causing a challenging prod issue very quickly.  Netflix extensively uses the Restify node module.   How do we get Statisticts for functions in node?   
This page may be a good summary of his work.

Need to research mdb debugger which is joyents "MDB is the illumos modular debugger".

**Stack Trace Debugging**

* Statistically sample stack traces 
  * Compare different stack traces
* How to sample stack traces?
  * Use linux perf events.   Bummer - Google JS V8 engine uses symbols instead of method names (JIT)
  * Node:    pass param to node on startup:    node --perf_basic_prof_only_funcitons
    Searching on "perf_basic_prof_only_funcitons" led to this writeup on node debugging.  
* This session had another reference to Flame Graphs.  Probably worth researching if one gets into production fire fighting.
* Can look at run time crashes using Core Dumps
node  abort_on_uncaught_exceptions
* Use linux debugging of node processes
* use mdb commands
  * ::JS STack
    * Always name your js functions so you get useful data when debugging.   hah - try to not write anonymous funcs.
  * ::JSPrint
  * ::JSConstructor

**Memory Leak Debugging**
* Generate core dumps ad hoc
  * gcore [-o filename] pid
*  mdb ::JSObjects
* @asdf::jsprint    this is a technique for dumping object details.
* ::JSObjects.    Can pass -r to this to find parents which is useful in finding calls that are causing problems.

### Session:  Getting a Handle On Your Dependencies - Dan Silivestru, bitHound
Its now common to have 80% of your code from external sources.   He reiterated (see npm ashley above) that there are 200K+ packages on npm.   How do you decide which packages are the best?

* use npm website to search modules
  * look at code quality, downloads, collaborators.
  * look for the project being flagged as insecure.   See github site
  * watch for dependency that has vulnerability

Look into the node security project.  I believe its this site.   Consider contributing back to the community.

### Session:  Building and Engaging High Performance Teams in the Node.js Ecosystem - Chanda Dharap

This person was a manager at StrongLoop.   The Devs were super devs.
She went over a term - Fungible.    Be fungible across stacks and know how to debug

* hire Top Notch people.
* evolve your team processes continuously
* Technology:  beg, borrow, write it.   
* Write small node_modules.  
* Scrum teams - max of 7 people.   Tooling is important
* Used Waffle for PM.  Unfortunately waffle doesnt have burn down
* Dev comm tools:    Slack, hangouts, zoom, talky.io
* Extensive use of GitHub.    

### Session:  Making Your Node.js Applications Debuggable - Patrick Mueller, NodeSource

This is probably available on youtube
**Perf:   use v8 CPU profiles**

* Take stack traces.  You can trigger on/off.
* consider "self time" vs. "total time"
* You may want to use the NSolid Flame Graph
* node_modules
  * v8-profiler
  * node-inspector
  * Strongloop arc 

**Memory:    use V8 HeapSnapshots**

* dump to JSON.   This creates very large files
* Triggered by TakeHeapSnapshot()
* See Google Developers - viewing heap snapshots
* Output by constructors
* idea:  take 2 snapshots then diff
* look into node/v8 option:   --no_use_inlining
* Can use chrome debugger to do the diff of the snapshots

### Session:   Reaching Ludicrous Speed - Matteo Collina, nearForm

Matteo is one high energy guy.   
Look into the flags you can pass to node (no_use_inlining, abort_on_uncaught_exceptions, etc)

* trace_opt, trace_deopt
* trace_inlining
* trace_deopt_map  

Realize that there is a difference between flags you can pass to V8 JS and nodeJS.   
Allocating functions is expensive.   Try to reuse functions when possible.
He mentioned a node_module called Steed which is an alternative to the async module.    Look into cork(), uncork(), to avoid crossing the js/c++ boundary
Garbabe Collection time counts, allocate as few objects as possible

###  Session: Lessons Learned: Extending Node.js with Another JavaScript Engine - Arunesh Chandra
Look into the FUSE npm. It lives between linux kernal and hardware (see link)
User Space - FUSE client 
Can use this package to mount various systems, including bit torrents

### Session:  Lessons Learned: Extending Node.js with Another JavaScript Engine - Arunesh Chandra, Microsoft
MS is participating in NodeJS but seemingly in an unfortunate way.   The nodejs is now forked to accommodate "Chakra" which is a node extension that runs on Win10 that allows node to talk to a type of processor
This seems infuriating, disgusting, and every 4 letter word I can come up with.  Read about this garbage here.

### Session:  Stellar Module Management - David Dias, Protocol Labs

Pull Modules from Smart Lookup as opposed to npm only.    Details here.  
The InterPlanetary File System (IPFS) is a new hypermedia distribution protocol, addressed by content and identities. IPFS enables the creation of completely distributed applications. It aims to make the web faster, safer, and more open.
IPFS - Intergallactic P File System - Avoid net outages

 

# Day 2
### Session:  Rebuilding the Ship as it Sails: Making Large Legacy Sites Responsive - Philip James, Eventbrite
Review Dorsal - a style guide utility.
Review Selenium Sauce.    

### Session:   Node.js API Pitfalls: Can You Spot Them? - Sam Roberts, Strongloop
This session presented a number of challenge code for the audience.   
Know the differerence between nextTick and setImmediate.  Its counterintuitive

* SetImmediate will be called on next Tick
* NextTick will be called immediately
Review the Cluster npm module, and extensible multi-core server module

### Session:  Peer-to-Peer Numeric Computing with JavaScript - Athan Reines, Verbify, Inc.
This session was around large data computing projects.   The idea is you can write your code in various modules then share the data on the web.   You could have module1 crunch data over many hours then put the output in to a page that module2 consumes and others can review/modify.
This is a great example of the blurring between client and server
Peer to Peer wasnt the real focus on this but the presenter thought it would be fun to discuss.
Review:  rpc-multistream npm package
The presenter thought this was "killer" for data analysis sharing
Review: webrtc-connect

* This allows data channels between browser-node and node-node.   
I think the idea is to build out browser and node channels which ultimately gives you browser to browser 

### Session:   Offline-First Apps with PouchDB - Bradley Holt, IBM
We have been focusing on "Mobile First" development.   The person thinks we will change to "Offline First"
PouchDB is a webDB that communicates to a server PouchDB and replicates with the browser
PouchDB is based on Apache's  CouchDB.  It utilizes optimistic concurrency

Session:  Building Interactive npm Command Line Modules -- All The Things. - Irina Shestak
This person built a variety of command line modules, mostly for fun.   Make them useful, make them fun, zzz.

Session:   Node.js Performance Optimization Case Study - Bryce Baril, NodeSource
When looking at Performance, you need to consider throughput (task completion).  
Task Completion = Task Start - Task End
Throughput = requests/sec
Consider:   How slow is it?   Can use /usr/bin/time to easily record time. Ie, can use kernal tools to evaluate perf.
Review:   v8 Profiler

* Put instrumentation in your code
* get perf file
* view file by loading in chrome tools
Review:    Node/V8 arugments

* --prof
* --trace_depot 
Review:    IRHydra2   Code Optimization/Deoptimization

### Session:   NodeJS Testimonies:   Paypal
In 2012 they built the nodeJS prototyping platform.   Replace Java/Spring
Paypal has 700 active nodeJS Devs
To switch to nodeJS you need:   influences, experts/mentors, community
They prototype with ExpressJS
They like Gulp instead of Grunt
Consider OpenSource and InnerSource:  InnerSource is only inside Paypal
Review:   Kraken (bootstrap express).   A javascript benchmark
Review:  KrakenJS:   Kraken is a secure and scalable layer that extends express by providing structure and convention. Though kraken is the main pillar of our framework, the following modules can also be used independently:

* Lusca
* Kappa
* Makara
* Adaro

Review:  Kappa - private npm
Wins:  Open source aligns with modern developers
Angular then react
Innersource:   InnerSource takes the lessons learned from developing open source software and applies them to the way companies develop software internally

### Session:   NodeJS Testimonies:   Netflix
Netflix had struggles between JS Client devs and Java Server devs
Gained performance on startup times using a module ecosystem
Use:

* Restify 
* React (kind of tricky on the server side)
* Falcon (internal to Netflix)

Node:   Need to unlearn Java instincts
They had to debug memory leaks around shared global space.
Its important to understand the Server JS and Client JS are somewhat different
The importance of insights - they moved to to using Restify.
Review:  Spinnaker and Jenkins
Wins:  Platforrm as a Service - Easy Deployments

* Titus
* Container Service
* Docker
* Reactive Sockets
* Logging

### Session:   NodeJS Testimonies:   GoDaddy
Built a variety of micro service
Technologies used:

* Express
* Reddis/Casandra
* Proxyquire for mocking
* Mocha
* Apollo (comming soon)

### Session:   NodeJS Testimonies:   Modulus  
install it as a global module (-g)
Have to sign up for an account
Modulus project create - Pick your runtime (nodeJS).  Bummer:  Projects are hosted externally (on Modulus servers)

* Pick your server size
* Run modulus deploy.  You get back a URL where your project lives

### Session:  Node.js and Joyent - Bryan Cantrill, Joyent
Node is no longer being maintained by Joyent, its now part of an open source community project
Joyent is selling cloud hosting solutions - direct competitor to AWS
Their hosting uses a "Containers" where you can build your app locally then deploy to a Joyent container
Review:  Docker containers

### Session:   Real-time diabetes management with Node.js and Microsoft Azure - Scott Hanselman, Microsoft
Presented an Azure app where data from his IOT diabetis device uploads to azure then he can see charts and whatnot.  Cool stuff for a diabetic (like Scott)

### Session:   End of Conference
The hope is 100% year over year growth
Node community wants people getting involved.   Current and future::

* Node School 
* Training Programs
* Cert programs


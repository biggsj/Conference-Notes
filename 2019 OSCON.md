# Summary

The highest level of abstraction taken away:


### **We won (Open Source beat M$)**

Note the past tense of this statement.    Understanding this should give one purpose.


### **Automation**

This was more confirmation.   The new age purpose is to think in terms of automation to eliminate mundane work and enable innovative work.   This leads to happiness.  Some basics to consider



*   learn the bash language
*   learn the powershell language (Yes!).    The most obvious here is around LDAP/ActiveDir but there other MS centric software.     
*   all _good _new age software has api interfaces to allow automation.   Train your mind to think in automation.  How will i automate setup and maintenance of this software?    How can I use a 3rd party "Orchestrator" to eliminate a human having to perform maintenance and/or support?  Shift left!


# Conference notes



*   "A goal without a plan is a wish"
*   "Open Source is not free"
*   "Organizing is what you do before you do something"
*   "The Journey is never ending.   There's always going to be growth, improvement, adversity".
*   JB lunch with UofOregon teacher.   University's are likely way behind on understanding the new age of Infrastructure automation.
*   Process overhead stifles your Dev Culture.    Process overhead creates bottlenecks and silos.
*   OKR is a tool, NOT a solution.    Goals come from a purpose.
*   People dont resist change, they resist being changed.

Further research links:


<table>
  <tr>
   <td><strong>Software to Look Into</strong>
   </td>
   <td><strong>What it does</strong>
   </td>
  </tr>
  <tr>
   <td><a href="https://conferences.oreilly.com/oscon/oscon-or">Oscon Conference</a>
   </td>
   <td>Videos should be exposed eventually.
   </td>
  </tr>
  <tr>
   <td><a href="https://airflow.apache.org/">Apache Airflow</a>
   </td>
   <td>Airflow is a platform to programmatically author, schedule and monitor workflows.
   </td>
  </tr>
  <tr>
   <td><a href="https://www.openservicebrokerapi.org/">Broker API (open source)</a>
   </td>
   <td>A vendor supplies this solution to sell cloud native solutions.
   </td>
  </tr>
  <tr>
   <td><a href="https://stedolan.github.io/jq/">jq json query</a>
   </td>
   <td>Its like SED for JSON
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/28mm/blast-radius">Blast Radius for Terraform</a>
   </td>
   <td>Nice tool for rendering your Terraform provided infrastructure using Terraform graphs
   </td>
  </tr>
  <tr>
   <td><a href="http://shop.oreilly.com/product/0636920039761.do">Database Reliability Engr</a>
   </td>
   <td>If SRE is great, why not have DRE?
   </td>
  </tr>
</table>



## Wednesday 2019.07.17


##### **Solving enterprise DevOps and frontend challenges with open source (HPE)**

Expose your products (fraud, vsafe?) via a broker solution.   It simplifies being able to integrate a 3rd party product via discovery.   The idea is to have a "Service Consumer" discover a "Service Provider".   The stack of software:



*   Broker - offers capabilities
*   catalog - provides the catalog of services
*   Service - a capability managed by a service broker
*   Service Instance - Create a specific instance
*   Binding - bind the service to the backend

**<span style="text-decoration:underline;">The automation</span>** - you dont have to worry about the _how_ of the back end.   You just want to call into the service to use the functionality.   Using brokers enable you to use the functionality quickly in that you have no setup costs around the backend.   Just use the service and pay the bill!   The backend is likely going to be provided in the cloud.    You dont have to worry about the provider.

Look into Open Source Broker service API in links above.


##### **Great wide open source in big business (sponsored by Capital One)**

You need to define your companies philosophy. 

Capital Ones philosophy:



*   We work in a highly regulated industry
    *   Vesta:    pci, MAB, 
*   We are risk focused
*   We work in a long standing industry with established ways
*   We are accountable for our decisions and must understand tradeoffs
    *   Vesta:   Developers need a workflow to enable adopting new technologies.    Maybe COP review?
*   Open Source has a cost.   Don't just use a new open source widget for the sake of using it.   It has to be an accountable decision.
*   Open Source is a business strategy.   
    *   You should align to an open source purpose for you business.
    *   What kind of business do we want to be?
    *   What we are versus what we are not
*   Make Open Source a core tenet:
    *   Build on OS
    *   Contribute to OS
    *   What are Vestas core tenets?:
        *   How do we get engagement?
        *   What are the executive's tenets beyond the ridiculous simplicity of: make more money and save more money.
*   Engagement
    *   Education throughout the organization
        *   Education of all developers, including data scientists.
    *   Conferences
    *   Alignments on goals \
Vesta:    Security - what are the goals of Infosec?  How do devs align with Infosec?  Can infosec align with Devs?
    *   Align on processes
    *   Align on capacity
    *   Feedback to get better

Capital One had to align across the org to get common OS managed.   Meetings of higher level cross team members.   From a Centralized committee to a decentralized.    They debated governance.   It was a Shared Responsibility across the teams.

Define your company goals - Corporate goals, program goals

OS transition:



*   They intentionally started slow to flush out mistakes.
*   design controls that are lightweight.   Reduces cleanup costs.   Cleanup will be necessary as you evolve \


Consider pipeline blocks - sw cant go through the pipeline unless it passes each control along the pipeline.

Capital One KPI - How many New College devs did they hire?

Vesta - whats is our core values?    JB Opinion:  Its payments and innovation .  For instance, We don't have to be a great docker company.   We can buy 3rd party tools to reduce the need to build unneeded software.   Do we want to be a Splunk company?


##### **Conquering both containers and virtual machines with Kubernetes**

This was an excellent overview of how containers evolved out of linux - cgroups and namespaces.    The idea is processes are managed by the linux kernal.   She presented an overview of how linux process are configured within linux on disk and how you can create processes which create the backing cgroup and namespace.    This is an easy to understand demo and worth watching a second time once Oreilly exposes the OSCON 2019 videos.

Docker can be run in 2 ways - a linux kernal or a hypervisor.    

"VMs solved syntethetic machines with Hardware"

Demo:   She wrote C code, gcc.ed the code, then ran the demo to expose various ideas around cgroups and namespaces.



*   Clone - a new process can share the original process PID
*   Clone with new - changed the C code to create a new PID for new child process.  Now there were 2 pids but more importantly, a new pid with cgroup and namespace data.
*   Clone with new and new mount - Exposed how the mount was within the **namespace **of the new child pid
*   Mkdir nova - This caused linux actions that impacted the **cgroup** config.
*   You can configure cgroup information which impacts the process related to that cgroup info (memory, cpu limit, etc).   She limited the memory on the cgroup for the pid and showed how linux killed the PID because there wasnt enough memory to run the process

Container technology utilizes linux cgroups and namespaces to both create and manage linux processes


##### **ML on code: Machine learning will change programming**

This presentation was interesting but not compelling to me anyways.    The person presented how code is a sequence of words that may get compiled into bytes.    The ML stuff can perform neural net based on sequences of bytes or words.   Calls like printf can turn into graphs of calls.   The word "graph" was also applied to building our neural nets based on a graph of the bytes or words.   


##### **I'm a developer; should I care about a service mesh?**

Developers are the new "King Makers"

A Service Mesh has



*   Traffic Management
*   Security
*   Observability

Service Level Metrics:



*   Response code
*   Response time 
*   Dashboards \
These 3 items related to "Stats Adapters" like Data Dog and Prometheus

AppA comms to AppB.    Service Mesh injects proxies in front of the Apps so that the above mentions can be collected.   A Service Mesh will take care of Certificate Management

AppA →ProxyA → ProxyB → AppB

If we introduced AppC and A called B called C, the service mesh has to manage A to B to C stats using **Tracing Headers**.

Do I need to change my application?   Ans.   It depends



*   Are you using distributed tracing?
*   are you talking to external services.   You only get TCP metrics for external services


## Day 2


##### **Day 2 Keynotes**

"Document Heroes" at google!


##### **Deploying containerized and serverless apps with Terraform**

Terraform is very cool due to the enormous amount of providers it has already.

jq is really cool.    The evolution from xml to json!

Terraform variables - 1 is for describing the variables, 1 is for setting

When do you run terraform init?   She used terraform init of an already initialized environment which didnt make sense to me.


##### **Level up your dev culture (sponsored by SAP)**

Your development culture differentiates you from your competitors

Your development culture builds on top of your corporate culture

They value a grass roots development environment.

Key concepts:



*   Coding
*   Agility
*   Exchange
*   Learning
*   Empowerment
*   Proudness

A hackathon should be setup by teams wanting to do it - NOT by management asking for it.  Ie, grass roots

Process overhead stifles your Dev Culture.    Process overhead creates bottlenecks and silos

Open Source - its not just about tools, its about process:  "Why are we doing this?"

OKR is a tool, NOT a solution.    Goals come from a purpose

People dont resist change, they resist being changed

Dev Culture:



*   Measure
*   Act
*   Repeat

Dev Culture change is a change in your DNA!  



*   Exec acknowledge that sw dev is the future.  They understand automation and the value of coding.
*   Developers realize development is not a playground.   Devs need to understand business values
*   Everyone changes around a dev culture!


##### **Writing npm (JavaScript) libraries using TypeScript**

Very interesting overview of creating npm modules:



*   npm install typescript
*   npm run typescript blah      (This creates a ts.config.json file)
*   edit ts.config.   she set outdir, rootdir, and include (include tells typescript what to compile)
*   He then wrote a node module
    *   export blah { \
    console.out("sdfsd'); \
}
*   npm run typescript    (he gitignored his lib/ dir)
*   update package.json    He defined entry point (main:  lib/module.js), he defined what files to include   Files: [lib/**/*]
*   npm publish dryrun (allows you to see what would happen)
*   npm publish    He had to set the namespace for publish to work
    *   He demo'ed how typescript requires you to define types used in your code's apis
    *   He demoed how you cant publish over an existing version
        *   npm version patch

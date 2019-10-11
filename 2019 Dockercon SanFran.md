
**Tuesday**

"Learning how to lose makes you a loser" - Chris Paul, Houston Rockets

(said after a basketball game that occurred in one of the evenings while at Dockercon)


<table>
  <tr>
   <td><strong>Software to Look Into</strong>
   </td>
   <td><strong>What it does</strong>
   </td>
  </tr>
  <tr>
   <td><a href="https://hub.docker.com/_/kibana">Kibana</a>
   </td>
   <td>Related to Monitoring/Alerting/Charting (part of Prometheus/Elk presentation)
   </td>
  </tr>
  <tr>
   <td><a href="https://helm.sh/">Helm</a>
   </td>
   <td>Used for K8 orchestration. They use "charts" in context of shipping, not reporting
   </td>
  </tr>
  <tr>
   <td> <a href="https://anchore.com/">Anchore </a>
   </td>
   <td>Security and Compliance
   </td>
  </tr>
</table>



### **Keynote.  Announcement:  Docker Desktop **

You will now be able to automate your docker setup with templates

     Ex.  You can setup a k8 + redis + MySql instantly

Works on your desktop

Creates a pipeline for you

Code generators for baseline tools like  Jenkins for the pipeline

Aside. I should open source the nagios solution via github

"Docker Enterprise as a Service" - End to end automation 


### **Workshop - ELK, Prometheus.  Paid $100 for this**

What do users care about?   



*   Availability
*   Latency
*   Reliability

Build monitors for the 3 items above.

"Brain Based" Tools - humans can only deal with 8 objects at a time.   Design your dashboards accordingly.

SRE - They should treat operations as if it were a SW problem

**Monitoring concepts:**



*   Black Box - outside of the container
*   White Box - inside the container

**Monitoring goals.  You should:**



*   Monitor all along the pipeline, all the way up to code checkins
*   Monitor all along the stack
*   You should Monitor all the way up stream to code checkins

**Need to define Vesta monitoring standards**



*   Whats useful
*   how long to keep 
*   Container logs, Swarm Logs, Compose logs

**Elk**

[Kibana](https://hub.docker.com/_/kibana) - Look into 

He created logging tests that also pinged google.   He then used kibana to view the logs

Kibana - you define log parsing (or use a known format).  Create indexes for the logs.    There was a lot of good demo info here.

Can utilize tags for searching

Kibana - create a dashboard.   you create a "visualization".

Kibana uses elasticsearch under the hood

**Docker Monitoring**



*   **Docker Stats** - A real time dump
*   **Docker Top** - What containers are running \

    *   Docker System Info - client info, log drivers, etc
*   **[Docker df](https://docs.docker.com/engine/reference/commandline/system_df/)** - helps you see whats being consumed
*   **[cAdvisor](https://prometheus.io/docs/guides/cadvisor/), [github location](https://hub.docker.com/r/google/cadvisor/)**
    *   Real time data
    *   Its just another container.  
    *   Shows memory, cpu, etc
*   **[Prometheu](https://prometheus.io/)s \
**
    *   Used for a query language
*   **[Grafana](https://hub.docker.com/r/grafana/grafana/)**
    *   Used for Reporting
    *   Can create Green/Red dashboards

Prometheus Stack



*   Grafana wraps:
    *   cAdvisor for Container info
    *   Docker stats, docker top, docker df
    *   node-explorer for nodes

What metrics are we interested in?

What alerts are we interested in

We could have a Vesta "Dashboard certification" program!


### **From Swarm to Kubernetes (and back again)**

Simplify ↔ Experiment ↔ Standardize (↔ simplify ...the three form a triangle)     In the middle of those 3 is the word:  Visibility

Everyone codes!

Some bad issues with K8s:



*   They found that there wasnt much K8s training
*   K8s gets to be complex fast

K8s [Taints and Tollerations](https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/) - get complex fast

They failed to recognize the human element



*   Nobody was trained on K8s
*   K8s is more robust, therefore more complex, than Swarm


### **Docker Desktop**

Helps you learn Kubernetes, Swarm, Docker, etc

"Less time in Ops, more time in Dev"

K8 works on your desktop now.    JB: Do you still need minikub?

The tool is trying to achieve parity between Dev and Prod.   Consistency

This tool automates new app setup

There are now "application templates".  You can make a template for your company

You can codegen your pipeline


### **Aqua Image Scanning**

You cant scan in production, its too late, so scan early in the pipeline

You need to answer:



*   what is the risk of running an image?
*   What can a running container do?

This is part of the "Shift Left" movement

Note/beware:  Some people are getting hacked because they checkin their SSH keys into github

Can have Aqua as a Plugin into Jenkins. 

Example pipelines:   



*   compile, scan, push to DTR
*   download from Dockerhub, scan, pass scan, push to your DTR

protects against hacker:   getting into container, adding hacker tools, using tool

**95% of container hacks start with the hacker getting inside the container**

You can introduce network control:



*   can have per container network policy.  
*   Can have Build Policy for network modifications in your stack file
*   Can have a tool that learns your network flow, you review, then lock the flow in as policy
    *   Good for enforcing network traffic blocking going forward

Image scanning is an emerging industry standard

Run time protection:  You can enforce immutability.  Should we enforce?

**Free Tools:**



*   Aqua Microscanner
*   CIS Benchmarks for K8s
*   [Kub-hunter](https://blog.aquasec.com/kube-hunter-kubernetes-penetration-testing) for Pen Testing


### **What I wish I knew Java**

Need to look into Namespaces

Consider:  Java is already in a container

Won't our Java app containers be small?

Use dockerignore to help save size

Look into docker squash

Alpine based on musl libc and BusyBox

Can use the various java Vm config to limit compute (memory, cpu...).  -Xmx, etc


### **Building your Dev pipeline**

Optimize your build agents.  Use containerized build agents.   Use OnDemand build agents

Docker inside Docker.   Parent can control processing using docker ps.   



*   Bummer have to give privilege to the containers.  docker.sock
*   Using docker.sock means you lose the benefit of containers being contained.
    *   Using docker.sock is bad in that you give host access to the container.

Demo'ed:   Provision build agent, build your app, push to DTR

try to use the compose file composition logic - docker-compose-test, docker-compose-dev

Idiot proof deployment pipeline failures?

Can benefit from containers starting in parallel.   Better compute usage with faster startups

Can use Jenkins parallel stages - example:  Building Linux and Win version in parallel

**Securing container images**

He demo.ed a security flaw where a baseline dockerhub image used Oracle JDK but that JDK didnt have a version number.



*   pipeline:    download image, scan, push to DTR 

Can have policy on images - cant start a container that isnt signed and pulled from your private DTR

Look into [Anchore ](https://anchore.com/)- "Automated container security and compliance"

Look into running "Cannary Apps" in production

Pipeline only has to monitor the pipeline because the orchestrator does the other work

Rolling update considerations:



*   As you are rolling, you could be temporarily running 2 versions of your app.
*   We need to consider this and test scenarios

He Demo'ed:   Catching a developer breaking policy by using the Anchore tool.   

Policy considerations:



*   Cant run commands as root in your dockerfile
*   Cant build and image that doesnt have a Healthcheck

We should have a story around Dockerfile policy

A failure of policy compliance fails that stage of the pipeline (assertive).

Enable "Security Team" signoff via code and tools.


### **Secrets Plugin Development**

JB:   This is an advanced topic that likely doesnt apply to Vesta at our early stage

JB:   This person was a pretty dull presenter

The industry standard seems to be using Hashicorp Vault which has DockerEE integration out of the box

Docker:



*   Extensible plugin architecture
*   Being refactored to refine/enhance its component architecture.   This should enable even more plugin development

To enable a plugin in docker:  "Docker load plugin"

Hashicorp Vault:



*   This was presented after the heavily technical Go Language plugin development presentation
*   tokens are used for logging into Vault
*   tokens can have time based rotation policy
*   can use a temp token to wrap a secret.   Security around secrets transfer (vault to docker)
*   This removes "man in the middle" attacks
*   Uses the golang client library
*   You can build a plugin to call out to vault

Vault/Docker plugin development:


    create a client instance


    client.auth()


    get temp token from Vault


    do your secret work

He demoed how 2 instances of the same app go secret from Vault but each secret was wrapped in different tokens



*   Token identity different
*   Secret info the same

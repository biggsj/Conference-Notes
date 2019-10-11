## Summary (by me)

I have been lucky enough to go to a lot of [conferences ](https://confluence.trustvesta.com/confluence/display/~john.biggs/Conferences)which has given me valuable insight around the future of high tech.  Please reach out to me any time if you want to discuss (nerd out) on this future.  I think SRECon is THE most valuable conference of all of the conferences I've attended.  

There are a lot of thematic ideas centered around today's current state of high tech.    IMO, building an SRE team solves these major problems:



*   Ops to Dev (OpsDev):   **<span style="text-decoration:underline;">Operational Awareness</span>**.   
    *   Most devs have little operational awareness because thats how we modeled the business.   One of the first SRE small projects is to start building operational awareness using concrete measurable metrics.  The metrics must have very little to no subjectivity.   Ive brainstormed over 50 metrics and hope to work with Linda (QA) and Caroline (Operational awareness) to create a robust metric model.   The Metrics will span both Ops and Dev and rollup into higher level values.   I (meaning me) think that the highest level metric is "Reliability".  We'll know more once our model emerges.
*   Dev to Ops (DevOps):   **<span style="text-decoration:underline;">Everyone Codes</span>**.   
    *   We'll need our operations staff to know how to code and manage code (giflow, trunk based dev, pull requests, etc).   We have to automate mundane tasks.   Its important to know that this bullet point is not where you start.  Coding will predictably take time to learn so _<span style="text-decoration:underline;">nobody</span>_ should feel threatened by this transition.   We get to teach core principals of coding for this brand new team.  This is nothing short of awesome because a good developer designs and documents prior to writing code.   We can teach our SRE team how to properly design software solutions and avoid building code to react to the current problem - ie, we dont want incidental architecture.  

Vesta needs to send a large amount of Ops and Dev team members to the next [SRECon - Santa Clara, March 2020](https://www.usenix.org/srecon).



*   **SREs require:  Innovation, Agile, Continuous Learning (each of these pillars ties to the other 2) \
**

The most prolific session was the very last session I attended.  Scroll to the end of this page and read the notes for "The 3rd Age of SRE".  [The slide deck is here](https://confluence.trustvesta.com/confluence/download/attachments/53616740/srecon19_3rd_age_slides_rabenstein.pdf?version=1&modificationDate=1570802314637&api=v2).



---




    *   [Summary (by me)](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Summary(byme))
1. [SRECon 2019 Notes](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-SRECon2019Notes)
    *   [Day 1](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Day1)
        *   [Session:  T](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:T)
        *   [Session:  What makes a SRE team?](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:WhatmakesaSREteam?)
        *   [Session:  A systems approach to safety and cybersecurity](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:Asystemsapproachtosafetyandcybersecurity)
        *   [Session:   Building a Humane and effective on Call](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:BuildingaHumaneandeffectiveonCall)
        *   [Session:   Support Operations Engineering](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:SupportOperationsEngineering)
        *   [Session: The Unmonitored Failure Domain – Mental Health](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:TheUnmonitoredFailureDomain%E2%80%93MentalHealth)
        *   [Session:  Being reasonable about SRE](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:BeingreasonableaboutSRE)
        *   [Session:   From nothing to SRE](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:FromnothingtoSRE)
        *   [Session:   My life as a solo SRE](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:MylifeasasoloSRE)
        *   [Session:  Zero Touch Prod](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:ZeroTouchProd)
    *   [Day 2](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Day2)
        *   [Session: SRE Training](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:SRETraining)
        *   [Session: How to SRE by influence](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:HowtoSREbyinfluence)
        *   [Session:  Are we all on the same page?](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:Areweallonthesamepage?)
        *   [Session: Weathering the storm](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:Weatheringthestorm)
        *   [Session:  What to do when you have no SREs?](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:WhattodowhenyouhavenoSREs?)
        *   [Session: One on One SRE (with Miss Amy)](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:OneonOneSRE(withMissAmy))
        *   [Session:  Does Customer Service mater to SRE?](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:DoesCustomerServicematertoSRE?)
        *   [Session:  SRE and Prod Mgmt](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:SREandProdMgmt)
    *   [Day 3 – JB - Bummer on being late due to Uber Automation Exploit.  This is a good conversation of how Automation has some negative sides (but not much)](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Day3%E2%80%93JB-BummeronbeinglateduetoUberAutomationExploit.ThisisagoodconversationofhowAutomationhassomenegativesides(butnotmuch))
        *   [Session: How to learn more from incident](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:Howtolearnmorefromincident)
        *   [Session:   What I wish I knew before going on call](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:WhatIwishIknewbeforegoingoncall)
        *   [Session:   Why automating everything adds to toil](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:Whyautomatingeverythingaddstotoil)
        *   [Session:  Expect the unexpected](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:Expecttheunexpected)
        *   [Session:   Hiring Great SREs](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session:HiringGreatSREs)
        *   [Session – The 3rd age of SRE](https://confluence.trustvesta.com/confluence/display/~john.biggs/2019+SRECon#id-2019SRECon-Session%E2%80%93The3rdageofSRE)


# SRECon 2019 Notes


## **Day 1**


### **Session:  T**



*   SRE is pretty unknown today and diverse meaning within the tech industry
*   Vision an XY chart with Operational Efficiencies on the Y, and Reliability on the X.   Most companies have an operational model that exists to meet the current but its actually not that efficient.   The reliability is also not that great relative to what it could be.   SREs improve both X and Y
*   There are 2 opposing forces:   An innovation force and a reliability force, each pushes against the other.   Reliability supports a “reactive model”.   Every business needs a mix of both (ying-yang)
*   If the automaters (developers) aren’t operationally away, they can introduced unreliability automations.
*   Where the 2 points meet is considered the “Error Budget”.

**Opening Remarks 1**



*   Imagine XY chart.  X:   MisAligned to Aligned,   Y:  99.9% to 99.99999%
*   Upper left:   Unhappy customers
*   Lower Left:   Unhappy customers with low reliability
*   Why is SRE hard?
    *   Scope
    *   Difficult to measure “hard”
    *   What does it cost?   How can you define relative cost?
    *   Misconception of what an SRE does
    *   Ex.   Do you want a better pilot or a more reliable plane?


### **Session:  What makes a SRE team?**



*   SRE team builds monitors/alerts
*   SRE team skills – Phase 1 – “Fundamentals”
    *   Monitoring/Alerting
    *   Capacity Planning
    *   CI/CD rollout
    *   Load Balancing skills of managing chaos
*   SRE team skills – Phase 2 – “Advanced”
    *   Systems architecting (building out systems)
    *   Designing Distributed Algorithms
    *   Designing networks
*   SRE team skills – Phase 3 – “Pioneering”
    *   Product Management
    *   Data Scientist
    *   UX Research \

*   SREs: Measures cost VS. Reliability.  Build trust in the system
*   **The SRE I want to be: \
**
    *   Have a measure of reliability
    *   The measurement is tied to project priorities
    *   Your Ops work is tied to the measure


### **Session:  A systems approach to safety and cybersecurity**



*   Our current failure measurements are based on 50-60 year old patterns
*   Failures – The reqts were met but the reqts were unsafe
*   Safety and Reliability are not the same
*   Complexity is the problem – the unknown unknowns
*   Automation itself can make more problems
*   **“Human error is a symptom of a system that needs to be redesigned”**
*   We need new tools for the new problems
*   The new solution:  Use systems theory \

    *   **JB:  <span style="text-decoration:underline;">The whole is greater than the sum of the parts</span>**
    *   **JB:  Feedback loops**
*   Consider safety as a control problem (vs a failure problem)
*   Controller -> Controlled Process
*   RCA drives control but not as a dictatorship
*   **Make it in SREs self interest to do the right thing**
*   Data is not informational – its only when we utilize data that it becomes useful.


### **Session:   Building a Humane and effective on Call**



*   Constantly refine your alerting
*   Train people for being on call. 
*   They tried using run books for this training but it didn’t work
*   **Quantify On Call.  **
    *   Cost per minute of triage
    *   # of incidents
    *   Impact to on call person (People will quit if overly hammered)
*   Today – we have mitigation run books
    *   Need to get away from this
*   On call solutions – automate failover to give you some time to root cause the failed system.   Nobody wants to work on a live production incident.
*   Bad  On call people weren’t trained on the tools so they didn’t <span style="text-decoration:underline;">trust</span> the tools
*   JB: Are we stumbling into this with docker/Terrraform?
    *   We should log all mitigation actions
*   Enables you to build tooling- 
*   **Make your tools “safe” so on call people trust the tools**
*   Work toward undoing the mitigation actions
*   **Work toward mitigation work being M-F, 9-5**
*   “Fixing on call with mitigation tools”


### **Session:   Support Operations Engineering**



*   **Custom tooling is better than agent tooling.   This leads to automation**
*   Service Ops (SOPS) Principles (JB: Devs need to learns Ops):
*   **Favor automation over tooling**
*   Question the fundamentals
*   Context sensitive safety
*   Be diligently data driven
*   Build Automated Services as an asset


### **Session: The Unmonitored Failure Domain – Mental Health**



*   Some people feel threatened to expose mental health
*   We need to improve working conditions as SREs
*   Consider a snapshot of your current state (not just SREs):
*   Are you stressed?  Do you feel tense?
*   Physical Health – do you feel shortness of breath?
*   Mental health – Do you have depression?  Anxiety?  Or other mental health issues?
*    Stress is caused by:
    *   Novelty – Something new you haven’t experienced before
    *   Unpredictability
    *   Threat to Ego (your competence)
    *   Sense of control (you feel you have no conrol)
*   Stress leads to:
    *   burnout  Work overload, lack of control, insufficient rewards (+3 more I wasn’t able to write down!)
    *   Exhaustion; cynicism, ineffectiveness
*   How to destress?
    *   Vacation, mindfulness, meditation, exercise, controlled breathing, sleep better, therapy
*   Imagine 3 circles:   Occupational Uncertainty, imbalanced Job Design, lack of value and respect
    *   If these 3 circles were drawn with overlap, the middle of overlap would be “Procedural justice”
*   There is a concept of “Emotional Contagion”.   Can make for extra extra happy (good) or extra extra sad (Bad)
*   Influenecers:   Mgr to you, you to reports, you to peers.  We influence each other at group levels
*   Interpersonal+Individual_Factors+Contextual_Factors Leads to:
    *   Level of engagement which leads to
        *   Team effectiveness
*   SRE Techniques for improving the above
*   Monitor our people.  How often are you asked for feedback on your job?
*   Are there 4 golden signals? \

    *   Standard SRE signals:
        *   Latency
        *   Saturation
        *   Traffic
        *   Errors
*   New HR signals to think about:
    *   Cynacism
    *   Emotional exhaustion
    *   Chronic Negative Response
    *   Inneffeceness
*   What would be our SLOs, SLIs for our SRE job? (based on the hR signals)
*   What specifically affects SREs?  Create a form to collect data \

    *   On call?  Job Sat?   Stress?  Sleep?  Ability to focus?  Flight risk?
*   Hero syndrome:  People who are less likely to talk about their emotions are more likely to be emotionally contagious
*   **GO FROM A VICIOUS CYCLE TO A VIRTUOUS CYCLE**


### **Session:  Being reasonable about SRE**



*   Funny - he showed a photoshopped road sign:   “OPS renamed to SREs, expect delays” 
*   Beware: Checkbox and buzzword driven adoption of SRe
*   Shifting Ops to SREs takes time
*   Need soft skills
*   “Theres nothing wrong with Ops”
*   Team skills culture.  Cooler name.  Watch out for higher expectations
*   SREs need to level up on soft skills, communication skills
*   SREs need to understand App level development.  Understand demand on Devs and how Devs manage projects.
*   SRE thrives in a special culture. 
*   If you don’t address these reqts, SRE HELL!
    *   No connection with Devs
    *   Thell create science projects
    *   Wont feel useful
*   How to solve?  How to fix?
    *   Join the Devs!
    *   Master a programming language
    *   Learn and get educated
    *   Build inclusive attitude
    *   Treat tooling as a product
    *   Look for a value in provide, not a box to fit it in.
*   Reliability is about motivation.
    *   JB:  Where is our motivation?
*   Infrastructure Ops tend to work in Passive Mode due to the nature of the job
    *   SREs are proactive.  They work with Devs to be more proactive
    *   Ticketing systems are Passive
*   SREs work with Devs to prioritize stories
*   **<span style="text-decoration:underline;">*** SRES BECOME FRIENDS WITH DEVS!  ***</span>**


### **Session:   From nothing to SRE**



*   On Call is a topic that’s ho as you move from Ops to SREs
*   Complexity catch us by surprise
*   How does your team navigate risk?
*   SRE – where do you start
*   Cant just put a SRE on a team because initially, nothing makes sense
*   It will fail for something like On Call
*   **SREs require:  Innovation, Agile, Continuous Learning (each of these pillars ties to the other 2)**
*   SRE Failures: \

    *   If you try building out a separate SRE team, You start becoming a tooling team.  You’ve also gone back to a handoff model
    *   Both of the above lose things like Error Budgets
*   Embrace autonomous team.  The entire team becomes SREs
*   Devs are best to “Gain Signal” to gain ownership
*   You build it, you own it
*   **<span style="text-decoration:underline;">Eventually… EVERYONE is an SRE \
</span>**Dickersons Hierarchy of Reliability.  (JB:  Lookup in the SRE book)
*   Incidents, Monitoring, Post Mortems are old school
*   Putting gates in place – people find ways around them
*   SRE is NOT a cost center.   Not a source of beauracracy.
*   SRE is “Force Multiplier”
*   Avoid negative Measures.
*   How do you want your users to feel? 
*   Blameless Post Mortems
*   Dial up Autonomy.   Dial down control
*   Incestuous – shared context, shared approach
*   Measure positive value signals (ex. “this was great because…”)
*   JB Aside:  There are a lot of tools on the market these days.   Avoid building tools internally when you can.


### **Session:   My life as a solo SRE**



*   Brand new SRE – Don’t jump in and fix everything.
    *   Work on cataloging problems
*   “How come Ops doesn’t just fix everything?”  We need more documentaiotn and education
*   SLIs (SL Indicators) – maybe your customers want faster releases and can sacrafie a little quality for instance
*   His business wanted to improve – so they brought accountability to the Devs
*   They started learning and created an SRE culture
*   “Dashboads are terrible alerts”!
*   His Lessons learned:
*   Measure things that matter
*   Transparent communication
*   Educate the Team (Observabiity, Empathy, etc)
*   Ops is used to getting tickets and solving problems.   Evolve into empathisizing
*   His results:   Some learned Terraform, Ansible, etc.   The others left.


### **Session:  Zero Touch Prod**



*   Safe proxies:  When you automate everything, malicious actors can do big bad things.   Access to prod should be by ACLs
*   Every change in prod must be either:
    *   Made by automation or
    *   Pre Validated by SW or
    *   Made by auditable “Break Glass” mechanism
*   Education is a major part of an SRE culture


## Day 2


### **Session: SRE Training**



*   Consider Pyramids:
    *   1) Service reliability hierarchy (product is at the top of the pyramid)
    *   2) SRE Training Reliability hierarchy (program is at the top)
*   They measured feedback after 6 months
*   Found people want more hands on
*   Need to instill confidence
*   Teach just enough tech an tools to be ablel to navigage issues
*   Move away from passive listening
*   They wanted SREs to troubleshoot a real system
*   Facilitator back off more and more
*   Use groups of 3 students.  The “least” of the 3 should be in the middle
*   Need to have a prod like, pre prod system
*   Need to train in steps it seems.   Test training occurs along the way
*   They discussed 80 different breakpoints and realized there wre really only 4.  Value stream mapping?
    *   Docker fixes 76 of the old problems
    *   They realized they had new error types so trained around the system
*   They used a volunteer system.  Incentives with focal reiews.  Volunteer edcators, volunteer students
*   “SRE EDU”.   They had pools of instructors
*   Built instruction lab which was setup pre student arrival.  Students got a “pager” in a lab.
*   Instructor gets paged if it doesn’t break enuf
*   SRE EDU:   Instrumented for observability
    *   EDU Design – build around your culture
*   Training SREs is about building confidence.  Hands on. Means more confidence
*   ASSBAT – a student should be able to…


### **Session: How to SRE by influence**



*   NY Times developer their CI/CD pipeline in 2015 (not that long ago)
*   “Delivery Team”
*   Tools and automation, Engagement, <JB: missed the next points>
*   Focused on how they were perceived
*   Took a product management mindset
    *   Internal teams are customers
    *   Incentivize vs standardize tooling and processes
    *   Interviewed other teams for feedback
*   Not every team is at the same SRE level
*   Let engineers revise lurking issues
*   Raise and prioritize things we find, create improvement stories across teams
*   Plan degradation strategy
*   Incident Training – Develop training so engrs know how ot become an incident commander
*   Failure when you don’t have Devs intelligence
*   Your part of a team.  Get help from the team
*   SRE Training – use**<span style="text-decoration:underline;"> load testing </span>**(typical load) and **<span style="text-decoration:underline;">Stress testing</span>** (breakage)
*   Work with your team to create these 2 tests
*   Test execution – get team in a common room.   Post results to slack
*   Plan a party on a busy day (ex nytimes – election night)
*   Are we ready?  Were we ready?  Scorecard?
*   You get feedback on system, People, and process
*   Create learning reviews
*   Create improvement plans
*   This is “Continuous Systems Learning”
*   Can create Incident Management class


### **Session:  Are we all on the same page?**



*   How do we monitor a complex system?
    *   Devops, SREs, its all the same
*   Who gets paged?  Everyone
*   Who to alert/page?
*   Solution: “Adaptive paging” (instead of symptom based)
*   They used Tracing data.  **<span style="text-decoration:underline;">JB:  Need to learn open tracing. Can we use it?</span>**
    *   Used to determine context of alert
    *   They used tags to add semantic meaning
    *   Aside:  Open telemetry will replace Open tracing
    *   Tracing gives:  latency, thruput, errors -> Causality
    *   Build a parent/child relationship with tags to enable drill down
        *   Ex.  Acct system is broke (child) but no, payment system(parent) is down
        *   Ex.  Span tag – peer to peer tags to build peer relationships
        *   You can map to a team owner but its very challenging
        *   They were able to reduce false positive rates to 0%
        *   Traces Led to quicker RCA


### **Session: Weathering the storm**



*   Micro services:
    *   better code but more difficult context analysis. 
    *   Harder to monitor
*   An alerting machine:
    *   (Alert Pipeline + alert relationships(contexts) + deployments(code changes))
    *   These 3 are combined to create “correlation results” (ie, alerts)
*   These guys added monitoring for everything
*   Culture shift – shift in culture towards incidents monitoring
*   Pre calculation is valuable (**JB: Prediction Models!!**)
*   Hierarchy helps.   Validation rules helps, Accuracy Shines.  Evidence helps.  Adoption helps (ie, why aren’t they using it)
*   History repeats.   Save history!
*   Additional user based monitoring helps (3<sup>rd</sup> party external monitors)
*   Learning and defining remediation actions help in the future


### **Session:  What to do when you have no SREs?**



*   How do you get started?  
    *   Start small
    *   Review what you have
    *   Record the junk you have
    *   Create small tasks and report on what you have
    *   This adds a proactive element
    *   You slowly infuse the SRE culture \

*   Be transparent about the evolution
    *   Inform the business about the reality
    *   Don’t burnout.   Learn, report (stories?)
*   Define manual process via documentation, then automate
*   Always test backups!
*   SREs talk about redundancy.  Use risk/cost analysis.  Document.
*   SREs:  Keep going, Record your work, share your work
*   Find your rules and share/Publish
*   Example rules:  Don’t release from branches.  Test Pre Prod
*   Introduce Blameless incidents – NO blame
*   Documentation is RW, not RO
*   There is no such thing as a human error
*   Missing documentation
*   Missing Automation
*   Main causes of problems \

    *   Code changes
    *   Infrastructure change
    *   Tech Debt
    *   Capacity Issues
*   It doesn’t have to be pretty, it has to better
*   Good is the enemy of perfect


### **Session: One on One SRE (with Miss Amy)**



*   Trauma: extreme stree that overwhelms your ability to cope
*   “Poly Vagal theory” – a third level of stress management – social engagement! \

    *   JB:   This seems like what we have in the SO and RE teams
*   Resliance Engr \

    *   The ability to weather the storm
    *   Its not about CI/CD pipeline, it about bringing teams together (dev and ops) to work together
*   Emergent behavior – whats the impact on the person who had to handle the incident?
    *   We are trying to build a trust model, people to people

SRE 1on 1 questions for post incident evaluation



*   what was your role in the incident
*   What surprised you
*   How long di you work on the incident.  Looking for trends.   No heroes
*   Were you able to get the support you needed
*   Do uo ufeel the incdent was preventable
*   What actions do you feel good about
*   What do you think could have been better
*   What did you personally learn from this incident
*   What do you think we can do to preent reoccurrence
*   Did our tools and docs serve you well
*   Did you practice self care during the process
*   Can you thnk of anyone else we can talk to \

*   Vulnerability – how do we actually get stuff done (not just talk about it.  This creates human connection
*   Redunancy – message tranlatoin failure (info hand down)
*   Flying under the radar – slice some time to talk.
*   Teams don’t talk to each other so you reach out and 1:1 with anyone
*   **“The secret to leading org change is empathy” – Harvard bus review \
 \
EVERYONE IS HIRING SRES!**


### **Session:  Does Customer Service mater to SRE?**



*   Retention is cheaper than acquiring.
*   Giving good service makes us happy
*   Vulnerable people have long lasting memories
*   People really value service.  People talk about bad svc \

    *   JB: My Airbnb debacle in Dublin!!
*   Customer service people are an asset
*   Good service wins forgiveness
*   Company service metrics
*   Team Metrics:
    *   Happiness and Alignment
    *   Customer Service Impact
    *   Customer Service Capacity
    *   No Escalations
*   Operations Roles are basically Customer Service
*   Who Cares about your SRE Service? \

    *   Service Users (Customers)
    *   Service Owners
    *   Service Dependencies (Your stuff hoses others)
    *   Engineering Leads
    *   Engineering Mgmt
*   How to tell when you are winning? \

    *   Part 1 – Service Level Indicators (SLIs)
    *   Part 2 – Service Level Objectives (Set objectives so nobody is surprised later)
    *   Part 3 – SLAs
    *   Tool 1:   The Weekly Production Mtg
        *   Discuss High level metrics
        *   Review customer tasks
        *   Log follow ups
        *   Team decides importance
        *   Roadmap progress
    *   Tool 2: The Service review \

        *   SLA/SLO summary
    *   Tool 3: The dreaded maturity matrix \

        *   Bucket aspects of your service
        *   Use it to compare to others
    *   Tool 4: Data Catalog – what data do we own (JB ???)
    *   Tool 5: Customer Surveys


### **Session:  SRE and Prod Mgmt**



*   production Mgmt (Ideation) versus Program Mgmt (Implementation)
*   Common SRE product work – Ideas and Implement
*   Product mgmt. is about meetin needs and empathy
*   It doesn’t matter who does the product work, as long as it gets done
*   Done assume usage of your SRE tools, talk to your users
*   Interview Users, but not more than 2. \

    *   Ask non leading questions
*   Prototyping sprints \

    *   One week, one focus for all involved
    *   Limited time forces limited scope
    *   Team bonding
    *   Add user centric goals to roadmap
*   Prioritize Metrics. \

    *   Ex. Making dinner together as a family – high priority \

        *   Making desert – low priority
        *   Side dish – stretch goal
*   Scope is critical to roadmap
*   Examples of good and bad: \

    *   BAD:  Implement CI solution
    *   Good – Pilot a new CI solution
    *   Bad – Get rid of old CI
    *   Good – transition major partners to new CI
    *   BAD: Decomm old CI
*   How to use a roadmap?
    *   Strict start and stop dates
    *   Add updates to the roadmap weekly or biweekly
    *   Update line by line items
*   Roadmap is an internal tool – don’t send it out to a broad audience.  \

    *   Get feedback from users


## Day 3 – JB - Bummer on being late due to Uber Automation Exploit.  This is a good conversation of how Automation has some negative sides (but not much)


### **Session: How to learn more from incident**



*   **<span style="text-decoration:underline;">Use positive words</span>**
*   Don’t blame the system as being designed poortly
*   Ex. How did things go right?
*   What skills/tools/people were involved
*   Keep review and planning meetings separate
*   Keep future mitigation out of the post incident review


### **Session:   What I wish I knew before going on call**



*   Wargames – playground for incidents
    *   Use continuous learning
    *   Knowledge sharing
    *   On call handoff meeting
    *   Post Mortem
        *   Analysis of incident
        *   How to improve (backlog)
        *   Add to learning to the wargame pre prod lab?
*   Wargame:  Create an imaginary incident
*   Create a wargame template
*   Ex. Use pre prod.   Create bad code.   Release to pre prod
*   Actors
    *   Investigators
    *   Communicators
    *   Game master helps out
*   Run the game
    *   Invite audience
    *   Game Master Asks questions
    *   Take notes
*   Keep good run books.  (JB:  Better – automate)
*   Having humans run batch scripts for trouble analysis is usually bad (bad “what was the output when you ran xxx.sh”)
*   Can you have alert take human to run book?  Best solution!
*   Run books are hard to maintain, but needs maintenance


### **Session:   Why automating everything adds to toil**



*   IBM started automating a lot.  Thru research they discovered automation toil
*   Toil – gets in the way of making progress
*   Repetitive manual tasks
*   They key is to reduce the amount of toil
*   Automation: \

    *   Good for repetitive tasks
    *   Faster than humans
    *   Humans make mistakes
    *   Examples: \

        *   Chatbots
        *   Self healing
        *   Auto provisioning/deploying
        *   Self Service
*   In the beginning, Automation reduces toil
*   Identify Toil then automate.   This leads to happy SREs
*   Automation fails when the code isn’t maintained \

    *   New APIs break automation
    *   Dependencies change
    *   Requirements change
    *   SREs change
    *   Production Systems Change
    *   Languages change (Python 2 to Python 3)
*   “Automation Rot” \

    *   Unused automation – we maintain code that isn’t actually used
    *   The code is team specific, it doesn’t span teams
    *   Too many tools – there is a danger that when you goto use the tool, it doesn’t work. \

*   **<span style="text-decoration:underline;">Speaker opinion:  Automation is good, but toil is bad \
</span>**
    *   Solution: reduce toli caused by automaton (minimize rot toil)

**<span style="text-decoration:underline;">AUTOMATION IS DEVELOPMENT, SO TREAT IT AS SUCH</span>**



*   Code mgmt., git gitflow, trunk based, unit tests etc
*   **JB:  Architect your automation Tools**
*   **Design first, implement second**
*   Create self service tools that anyone can use
*   We want our tools to be used a lot
*   Build hammers – but how big of hammer do we need? \

    *   Restart container? (docker)
    *   Reboot VM hosting docker
    *   Reinstall the OS
    *   Reprovision the machine
    *   Go crazy and rebuild the cluster
*   Maximize usage to minimize rot \

    *   JB:   This seems like a metric
*   Imagine if you had to look at 10 jenkins instances for figure out which Jenkins job did what you needed to fix the current issue
*   Run books should point to the automation
*   Dealing with Rot – you cant avoid it forever \

    *   Have a strict MVP to see if it gets used
    *   Don’t deal with corner conditions.  Again MVP it
*   Survival of the fittest \

    *   Don’t assume the current is the best
    *   Encourage innovation
*   Build maintenance APIs into your product


### **Session:  Expect the unexpected**



*   Devs build structure into their life but aren’t good at resilience
*   Ops are better suited at resiliency and handling the unpredictable
*   Transparent Response \

    *   Share techniques
    *   Feedback to Devs
    *   Build trust with Devs
    *   Make Ops work transparent
*   Game Day - Incident simulation \

    *   Learn, Adapt, Evolve
*   Turn rusty knobs.  Use the od tools. \

    *   Ex.   Failover testing
    *   Ex.  What if a datacenter has a hurricane coming?
*   Automated failure tests – focus on most routine failures first
*   Can do with Open source tools
*   Incident Training – Do training exercises as fun team building exercise


### **Session:   Hiring Great SREs**



*   Avoid toxic people
*   The fundamentals \

    *   Will the candidate be able to do the job eventually?
    *   How long will it take them to reach that goal
    *   Is this someone we want to work with for years?
*   What is a great SRE?  BAD:   You only think about your current states
*   Focus on a set of traits when hiring a SRE
*   SRE Traits \

    *   Breadth of knowledge of services
    *   A need to understand how things work
    *   Wants to help
    *   Loves automation
    *   Wants to take action
*   What do we really need them to do?.  You may be forced because person just left
*   What % DEV, What % OPS
*   What skill level do we really need?
*   The Interview:
    *   Have a strategy.  Train on that strategy
    *   Create rubriks to measure
    *   Feedback to evolve.   Get rid of useless stuff
*   Avoid different groups asking the same questions
*   Why 2 people in an interview? \

    *   It helps the 1 person with the other person when asking questions
    *   It helps the candidate when clarity is needed
    *   Its “right sized”
*   The Interview is a conversation
*   They score: 0 (unfamililar), 1, or 2 (great details on the topic)
*   They weight the rubrik so it can be applied to both seniors and juniors
*   Realize nobody knows everything
*   Juniors – how to identify great candidates
    *   Should know approximate shape of answer
    *   How long before they can contribute


### **Session – The 3<sup>rd</sup> age of SRE**



*   First Age:
    *   Nobody did SRe except Google.
    *   Nobody knew what the role was
    *   SREino – SRE in name only
*   Second Age – 2014 – First SRECon (JB: So this is SRECon 6) \

    *   SRE in spirit
    *   Conferneces, books, etc.
    *   However, you still have in name only
    *   Note there are now 3 oreilly books.  Newest:  Seeking SRE
*   Third Age – Happiest and Highest paid in the industry \

    *   He cant name any company that is at the 3<sup>rd</sup> age
    *   Cloud only for the 3<sup>rd</sup> age
    *   You wont have SREs, but everyone will BE an SRE (will have a SRE mindset) \

        *   JB:  Imagine all this is taught at universities
        *   JB:  Imagine you have SRE consultants to get youre infra/docker/etc going quickly
        *   You wont hire SREs, everyone will be SREs
        *   You will only have dedicated SREs if: \

            *   You are huge
            *   You ARE the cloud (aws, azure, etc)
*   Most problems today are second age problems
*   Would you ever not be an SRE?   No!  It’s a mindset that cant be forgotten
*   Third age – EVERYONE IS A PROGRAMER


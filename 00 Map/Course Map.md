# Improving Your Testing Through Better Operability

## Course Title

Improving Your Testing Through Better Operability

Hopefully the title resonates for the primary audience (testers) and through the course I can show that although the focus might be on better testing, operability enhancements are cool for everyone.

## Target Learners

* Who is this course for?
  * My primary thought is that it is for testers, specifically those who are in teams transitioning to looking after their own platforms or maybe creating a new platform.
  * I get asked often by testers what their roles might be in 'DevOps' and operability creates a useful focus.
* What problems are they facing?
  * I think they are faced by a request/need for them to get involved in testing new platforms, disposable environments, cloud based systems but without the fundamentals of operability.
  * Also, I think often without the operational know how to get involved, plus there can be a lingering resistance from operations teams to let testers in, alas you still have to prove yourself often.
  * As testers are often (in my experience) not involved in operability changes, they miss opportunities to enhance their testing skills and over testability of the system.
* What skills are they developing?
  * There are two threads to this:

    | Mindset | Technology |
    |---|---|
    |Wider operational teams over development teams only| Networking concepts such as DNS, proxies,protocols|
    |Focus on system usage over testing functionality| Monitoring, logging, events and metrics|
    |System wide failure over feature failure| Testing hooks for failover, disaster recovery, data loss, deployment strategies|
    |Focus on production over test environments|Resource modelling, storage, compute, databases, support models|

* What is their knowledge gap?
  * I think the gap comes from testing what you can see (as in a feature) to the metadata of a system, around capacity, deployment, operational team roles, monitoring, modelling usage.
  * The course will look to enumerate what characteristics an operable system has, approaches to testing for them, finally how they improve testing in general.
  
## Prerequisite course, knowledge, skills or tools

* What knowledge or skill set do learners need to have before starting your course?
  * Three aspects to this I think
    * Expose to solution architecture - able to describe some of the patterns of an architecture (layered, client server, model-view-controller)
    * Knowledge of deployment patterns and source control - such as canary/feature toggles, plus tooling like Jenkins as a common starting point.  
* Are there any existing courses on the Dojo that they should complete first?
  * The 'Building Blocks of the Internet' would be a good start, as a lot of the concepts are testing the overall system and its interactions. Anything of an architectural nature.
* Are there any tools or programmes they are required to use?
  * Docker/Docker compose for general setup, mostly just for ease/speed of use
  * Jenkins for deployment based sessions
  * Git as a source control tool, mostly pull, rather than push, so no accounts as such require.
  * Probably use something like Localstack for the cloud parts, rather than having people set up accounts.

## Course Goals

Lets enumerate the characteristics of an operable system for this:

* When failures occur, they are obvious and recoverable.
* Logging is coherent, both in structure and location.
* Those who need to know how to operate the system, know how.
* Dependencies are known and their risks to your system are mitigated.
* Traffic to the system is known and can be throttled when needed.
* The system has hooks to report on system health and configuration status.
* The system can be partially available by component, rather than a state of complete failure.

### What skills and/or knowledge will learners walk away with or develop/problems they can solve.

* Recognition of importance of logging to improving testing
* Introduce testing of deployment pipelines to enhance their operability
* Create a operability test approach for system failover scenarios.
* Add meaningful operability hooks for systems via a HTTP API
* Know how to test system protection measures for dependencies, such as circuit breakers
* Model system traffic and access points to add to a team knowledge base

## Course Description

Reliability, handling failure gracefully and recovering quickly are becoming increasingly important as the software development world adopts DevOps culture and practices. Outages and security failures are big news and many companies are investing heavily to avoid these challenges. Operable systems are easy to deploy and test, provide actionable information about their state and behave more predictably in adverse conditions.

Testers on development teams are often used to testing changes to the functionality of an application but less so testing how operable a system is. My recent experience has seen testers on teams charged with improving operability for systems through better logging, monitoring and system control measures (such as feature flags) to emit better information. This information on system stability and state is critical to testing and we can influence its creation profoundly.

### Why it is important for testers

* As the operability of systems becomes a greater focus, testers need to be equipped with models to think about how to add value in this context.
* As testers, we strive to add value and testing for reliability enables us to use our risk analysis skills to explore for failures and how to recover.
* If we get involved with helping our system to emit better information from an operability standpoint, testability through observability and control will likely be enhanced.
* Rather than having shallow status checks, testers can contribute to meaningful monitoring of customer journeys and how reliability and recovery are measured.

## Lesson Plan

* Write a clear title telling learning what each lesson will cover
* What key knowledge or skills will your learners walk away with from each lesson?
* Are you learners ready for each lesson? Note down the prior knowledge required to complete each lesson, was this covered in the lesson before?

|#|Lesson Title|Lesson Goals|Prior Knowledge|
|---|---|---|---|
|1||||
|2||||
|3||||
|4||||
|5||||
|6||||
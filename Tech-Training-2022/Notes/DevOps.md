# Training Contents for next 4 days
1. Introduction to DevOps
2. Git and git operations
3. Git continue.... and intro to Jenkins
4. Jenkins

# DevOps Concepts
This page covers the core of DevOps Concepts and defines the terminology and principles defined for this module.
## References
* [DevOps Culture](https://martinfowler.com/bliki/DevOpsCulture.html)
* [Continuous Delivery - Atlassian](https://www.atlassian.com/continuous-delivery/pipeline)
* [CI CD CD - Atlassian](https://www.atlassian.com/continuous-delivery/principles/continuous-integration-vs-delivery-vs-deployment)
* [Continuous Deployment vs Continuous Delivery - Atlassian](https://www.atlassian.com/continuous-delivery/continuous-deployment/how-to-get-to-continuous-deployment)
* [DevOps Image Source](https://www.logigear.com/blog/continuous-delivery-devops/continuous-delivery-everything-you-need-to-know/)

# What is DevOps?
- DevOps is the union of people, process, and products to enable continuous delivery of value to our end users." - According to Donovan Brown in [What is DevOps](https://www.donovanbrown.com/post/what-is-devops)?
## Steps in Dev Ops and Production of Code
The steps or phases for Dev Ops refers to the creation, testing, and deployment of an application.

These steps include:
1. Source code Control: Producing (writing) code and pushing to a repository 
2. Building and Testing Automation: Test basic functionality of code (Generally unit testing) and create a new, working build
3. Deploying to Staging: Deployment of working build to a temporary environment 
4. Acceptance Testing: Undergo other more complex tests (systems, integration) within temporary environment
5. Deployment of Build: Migrate working build to Production environment accessible by end users

## DevOps and Agile
Agile is a mentality or philosophy utilized when approaching the creation of information systems, and is a flexible approach of addressing the steps of the Software Development Life Cycle. Development teams who practice an Agile methodology place a focus on producing code through iteration and collabortion rather than following a rigid plan.

Though DevOps, which involves the creation of a systematic approach to producing code, and Agile, which is a mentality that focuses on creating products by adapting to change quickly, seem contradictory, the goal of both methodologies is to produce working and valuable product more efficiently. DevOps pertains to the entire system working together to produce, test, deploy and maintain the code base, while Agile practices allow for each step of that process to change wherever and whenever needed.
* Agile Practices with DevOps:
  * Continuous Integration
  * Continuous Delivery
  * Continuous Deployment

Adoption of the Agile philosophies can provide a stepping stone for the establishment of a working DevOps pipeline, as Agile practices intrinsically produce more continuous feedback loops. Continuous Integration, Continuous Delivery and Continuous Deployment seek to automate the phases of DevOps as much as possible.


## SDLC 
- Phases 
  - Planning & Analysis
  - Design
  - Development
  - Testing 
  - Deployment 
  - Maintainence

- Models of SDLC
  - Waterfall model
  - Iterative model
  - Spiral model
  - Agile
    - SCRUM

- DevOps is contraction of Dev and Ops teams refers to replacing the siloed Development and Operations.
- DevOps Practises includes:
  - Agile Planning 
  - **continuous integration** 
    - ongoing merging and testing of code (to find defects easily)
    - Tools
      - Source Version Control (Git, SVN, Bitbucket, Gitlab, TFS etc.....)
      - CI Pipeline - Jenkins/Travis CI/Circle CI/Azure Pipelines/Github Actions
      - Environment - Cloud/on-prem/hybrid - Azure, AWS, GCP
      - Containerization - docker
  - **continous delivery**
  - monitoring of apps

# DevOps - Continuous Integration
- Continuous Integration is the process of regularly and consistently merging code into a central repository and reviewing new code to ensure that it integrates well within the previously established code base.

### References
* [Continuous Integration - Martin Fowler](https://martinfowler.com/articles/continuousIntegration.html)
* [CI Circle Image](https://www.qfs.de/en/blog/article/2019/07/11/using-qf-test-in-continuous-integration-systems-1.html)

Below are examples version control software:
* [Github](https://github.com/features)
* [Gitlab](https://about.gitlab.com/features/)
* [Perforce](https://www.perforce.com/support/self-service-resources/documentation)
* [Bazaar](http://doc.bazaar.canonical.com/en/)
* [DevOps Tools](/revature_training/devops-team/-/blob/master/./devops-tools.md)

## Continuous Integration
Continuous Integration (CI) is the first, and most fundamental step in creating an autonomous development pipeline.

Continuous Integration is a development team mentality, and is achieved when all members of the development team practice consistent merging of code into a central repository. For CI to take place, these Central repositories should be in the form of version control software.

Version control software is a tool which utilizes some directory structure to store files. These tools can track changes to code, and allow for changes to be merged (allowing you to select which changes to keep or reject if/when conflicts arise) or files to be rolled back to a previous version. The integration of code into these repositories should happen as often as possible with at least one commit each day. Generally, the more frequently code is merged, the less conflicts and/or integration issues will arise.

## Continuous Integration
Continuous Integration (CI) is the first, and most fundamental step in creating an autonomous development pipeline.

Continuous Integration is a development team mentality, and is achieved when all members of the development team practice consistent merging of code into a central repository. For CI to take place, these Central repositories should be in the form of version control software.

Version control software is a tool which utilizes some directory structure to store files. These tools can track changes to code, and allow for changes to be merged (allowing you to select which changes to keep or reject if/when conflicts arise) or files to be rolled back to a previous version. The integration of code into these repositories should happen as often as possible with at least one commit each day. Generally, the more frequently code is merged, the less conflicts and/or integration issues will arise.


Continuous Integration establishes the foundation for an automated DevOps pipeline, because it provides the following benefits:
* Ensures the entire team works on the most up to date code
  * Frequently pushing code allows developers to account for changes performed by other team members quickly.
* Detects broken builds quickly
  * If problems arise, version control software can help detect the root cause or rollback changes when necessary.
* Code can be tested easily by creating separate, test or development branches based on the mainline code.
* Reduces risk in development when a large codebase has already been established.
* Reduces the overall amount of bugs in a project

The best way to ensure your code integrates well is to marry the integration of your code with testing the code. Running test suites on the code base after new commits helps to minimise potential disruptions if conflicts do arise, particularly when utilizing certain DevOps tools to automatically run unit and integration tests. Despite this, it is also best to practice Test Driven Development.

# DevOps - Continuous Delivery

This page details the use and importance of Continuous Delivery for a DevOps pipeline.

### References
* [Continuous Delivery - Martin Fowler](https://martinfowler.com/bliki/ContinuousDelivery.html)
* [Continuous Delivery - Atlassian](https://www.atlassian.com/continuous-delivery/pipeline)
* [CI CD CD - Atlassian](https://www.atlassian.com/continuous-delivery/principles/continuous-integration-vs-delivery-vs-deployment)

## Continuous Delivery
Continuous Delivery is a paradigm in which the building, management and testing of produced software is automated such that deployments can be performed at the push of a button.

Continuous delivery is often confused with Continuous Deployment, which automates the entire production pipeline, including deployment. Continuous Delivery; however is the process of automating all steps of a Development pipeline except for the final deployment step. Inherently, Continuous Delivery is dependent on the implementation of Continuous Integration, and also serves as a stepping stone to creating a fully automated Development Pipeline (Continuous Deployment). Though Continuous Integration can technically be achieved without automation, Continuous Delivery is only achieved when code integration, testing and product building has been automated. In this way, you are able to perform frequent deployments "at the press of a button", but may choose not to do so, usually for business purposes or possibly due to a preference for a regular scheduled deployment process.

The deployment to production may also be kept manual so that final user acceptance tests can be performed manually as a final safety check on the code to ensure that it meets business needs. This is due to the difficulty and cost of creating tests to evaluate the user experience and not simply the functionality.

Benefits of Continuous Delivery:
* Reduced Risk in Deployment
  * Since new builds are not deployed automatically, faulty code is less likely to by deployed to production environments.
  * Less pressure is placed on the development team by allowing for small, more frequent changes to be made. This expedites the iteration of code.
* Predictable Progress
  * Since pipelines are a programmable infrastructure by the development team, desired behavior during the production of code is easier to configure.
  * With a pipeline the deployment process is more predictable, allowing development team to focus on the production of code rather than operational steps required to deploy the new codebase.
* Frequent Feedback
  * With the increased efficiency of producing code, smaller, more incremental changes can be applied to a system more frequently. If human error does cause problems, it is easy to roll back changes to a working build.
  * More releases accelerates the communication and feedback loop with client/product owners as well.

### Costs/Considerations of Continuous Delivery
* Requires a strong foundtation with Continuous Integration culture, and test suite coverage
* The Final deployment must still be automated which is an additional cost, Though the trigger to begin the process is manual this can still cause slowdown for the development.
* Communication of incomplete features and backlog must be maintained rigorously to communicate expectations to client and development team


## Topics for Research activity 
- Research and create reports on following topics 
  - What is [SRE](https://www.ibm.com/cloud/learn/site-reliability-engineering?utm_medium=OSocial&utm_source=Youtube&utm_content=000020LH&utm_term=10013860&utm_id=YTDescription-101-What-is-SRE-LH-SRE-Guide) - Site Reliatbility Engineer ?
  - Are SRE and [DevOps](https://www.ibm.com/cloud/learn/devops-a-complete-guide?utm_medium=OSocial&utm_source=Youtube&utm_content=000020LH&utm_term=10013860&utm_id=YTDescription-101-What-is-SRE-LH-DevOps-Guide#toc-how-we-got-IsFf3zMv) same or different, if different then how?
  - Various tools for setting DevOps?
- Make sure each group have a [git](https://github.com/) account, if none in the group have Github accounts please make one
- Reports should be in markdown form. If you want to know more about markdown use this [link](https://www.markdownguide.org/cheat-sheet/)
- Pairs for this activity as follows:

    |James - Steven|
    |--------------|
    |Hector - Ugo|
    |Michael - Harrison|
    |Timothy - Temi|
    |Jesus - Yulee|
    |Matt - Momo|
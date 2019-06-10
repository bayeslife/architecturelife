# Critical Success Factors and High Level Implementation Plan To Consume RESTFUL APIs into Azure Cloud

## Context


## Assumption

The following factors are assumed to combine to determine project success
- timeliness of delivery is an important component
- resource cost
- functional quality

## Hypothesis

There are critical factors (a winning hard) if the integration project/programme is to have a good chance of success.

## Critical Success Factors

### Source Code Management 
Store source code for the integration into a ***Git*** based repository.  Continuous Integration tools will retrieve code from this repository rather than from developers environments to ensure repeateability and transparency of changes over time to all integration team members.
`The Azure stack is easily integrated to GitHub (a Microsoft owned subsidiary)` 

### Environments
Like any on premise or cloud deployment the probability of successful deployment into Azure can be
facilitated by ensuring environment repeatability between test and production environments.
`Deploying an integration to Azure Kubernetes Service using helm allows the environment architecture and components to be described as source code such that it is very easy to maintain synchronization between development/test and production environments`

### Scalability
If the expectation is that volume of data needs to scale to 10-100 thousand assets it is important that the processing can be split or charded such that testing can occur at a smaller but still completely representable scale environment.
The solution will required a simple mechanism to scale processing as additional assets are brought online.
`The Azure Kubernetes coupled with the Azure Event Hub is ideal to acheive this deployment flexibility.  The Event Hub process supports for Consumer Groups (which share processing load) and Kubernetes provides the mechanism to easily scale those consumer groups when they are written with this intention`

### Replicate Production Data Streams 
Having real time replicated data streams in the test environment(s) will greatly improve
the quality of any validation activity in any test environment.
`Using Azure Event Hub a development/test environment can ready a copy of production data and forward it to development/test environment in parallel with consumption of the stream from production components`

### Decoupling
Decouple the throughput to ERP with the throughput of any data stream by using a pull model into the ERP.
This could be achieved by streaming API data into the EventHub where it can be processed and consumed into the ERP
at rates/timeframes suitable to the ERP (batch mode, after business hours).
`The Azure Event Hub is based on Apache Kafka which provides a short term, multi-client store and forward paradigm that provides a purpose built decoupling mechanism between producers and consumers`

### Continuous Integration
Build services using a Continuous Integration capablity that provides a capability to produce versioned runtime artifacts when unit and integration tests pass.
`Azure Container Registry provides the build, storage and registration services required for the software development life cycle`

### Config
An app’s config is everything that is likely to vary between deployments (development/test vs production).  There needs to be strict separation between config and code (which should not vary between environments)
`In the Azure Kubernetes service configuration is explicity managed, visible and lifecycled`

### Release
A deployment into an environment needs to combine specific versions of artefacts with environment specific configuration. The deployment process should deploy and validate the health of each microservice.  The deployment process should support rolling forward and backward deployments which ensure health of new component while older components are utilized to prevent interruption of service.  The deployment paradigm needs to easily support running multiple verions of services concurrently.
`The Azure Kubernetes Services provide great deployment capabilties to achieve all these capabilities`

### Security
Authentication, confidentiality and authorization (role based access control) are all necessary aspects of the integration so that systems can trust the related parties they are sending and receiving information to/from. As much as possible the security mechanism should be an orthogonal concern provided ideally through shared service capability which will take care of mundane aspects of security concerns such as life cycling of security credentials and life cycling user/system authorization to services through permissions.  
`
Azure provides the Key Vault to manage the life cycle of API credentials and restrict their visibility to authorized administrators.
All traffic from the integration solution will be HTTPS ensuring confidentiality.
The API request will include a security token (JWT tokens) to provide appropriate claims/permissions necessary to gain authorized access to individual REST endpoints. 
Azure provides an IAM (Identity and Authorization Mechanism) which can be used to life cycle credentials, manage user/group relationships, and audit usage amongst other capabilities.
The Azure Kubernetes provides for controlled access to its runtime through a certificate based mechanism. Certificates are issued to users authorized via Azure IAM mechanisms.
`

### Statelessness
Keep all the processing services stateless to allow for ease of deployment and concurrency.  Rely upon backing services outside the deployment to store state.
`Azure provides a number of managed services which can store process state and solution meta data. The services include Azure SQL,  Azure Cosmos, Azure Event Hub`  

### Agile
Focus the integration establishment as a set of independent activities which are incrementally identifying the next smallest unit of functionality which can be developed, tested and delivered.  The approach here is to minimize planning activities to those changes which are short term commitments.  The approach is also to use small teams which are empowered to incrementally deliver independent units of the solution.

### Hands On
As much as possible the team implementing the integration should have visiblity and hands on manipulation of the end to end solution functionality.
For example the team should have access to a test data capture device or simulated data capture device which they can manipulate and correlate with changes in the data stream.  They should also have access to dashboards where the data stream is surfaced to end users.
These views can allow the team to understand what is significant to the user story they are working effectively allows them to establish priorities for competing functions of a solution.

### Cost transparency
Ensure that cloud resources are grouped to allow for effective cost management.  If there are multiple independent outcomes of the integration establishment that should be independently managed the it is likely appropriate to create resources in groups associated with these outcomes.
`All Azure resources are associated with a resource group which serves as a primary way to get cost visibility`

### Test Driven Development
To ensure appropriate levels of quality are attained it is critical that planned effort is allocated to develop tests which will directly related to requirements of the solution.  To ensure this tests and a throwaway implementation should be developed first as a way to explore the problem domain.  Once the basic capability is known to satisfy required tests, it is subsequently possible to plan the refactoring of the implementation to achieve the appropriate levels of simplicity, readability, reusability and delivery timeliness. 


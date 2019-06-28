# Data Management System

## Identify principles, protocols and characteristics a program’s data management approach, including protocols for managing sensitive information and formats for data storage and handling. 

## Executive Summary

When considering a programs data management approach , it is important to consider the many options at multiple levels that are available within the program.
The following content presents options that are available to the program team. 

### Statement of Concern

The context for the Data Management System options identified for further consideration below are 
- there are managers attempting to address issues and risks to meet outcomes identified in a long term plan
- and they have difficulty getting access to potentially available data
- in a timely manner
- there are data providers who
    - distributed geographically
    - have different technical capabilites
    - have different license requirements on their data 



## Considerations

### Programme Problem Definition and Goals

There are considerations which relate to the problem definition and goals to be delivered by the programme. 

##### Validating the Problem Domain
The programme should address one or more identifed problem domains and should provide evidence to validate the problem domain.

Some work has been done in this area including
- Survey monitoring programs how data is requested

Other ways to accumulate meta data about data sources which could have been taken include:
- Establish a [FAIR](#fair-data-principles) data request facilitation service
    - A team who mediates requests for information and joins providers with requestors 
        - This could be realized through an email channel initially
        - That team would become the data aggregation service and would become a focal point to identify inefficient and address with automation.

- This might further be extended into provide a system which captures requests for data 
    - This could be implemented on top of available communication channels (twitter , stack overflow).

##### Approaches to Promote Reduction in Impediments to Data Access

The programme should consider all available development approaches to resolve the problem.
- Expand - Current proof of concept looks to be proceeding with data aggregation portal expecting that if it is built, they will come.  This is taking a concept and working through the technical delays to surface the capability in a scaled accessible form.

- Exploration - An alternative would be to foster further exploration of possibly innovative solutions to the problem.  It would have to be expected that many ideas would fail and there is no certainty with this approach but there is the possibility of success.
    
- Agile/Kanban - Another alternative would be an incremental approach characterized by agile/kanban methodologies.  Proceed to identify opportunities which appear most useful for the least amount of work  and work on delivering this opportunity.

- As a service - The idea here is to establish the service without any existing technology, get it to function in what ever way is possible and then as it provides service figure out how to take cost out of the service and add further value in.

##### Requirement Identification

There are multiple approaches to gathering the requirements for the data management service. 

- Assume that requirements which can be expressed currently will form the basis of the best alternative for a system design
    - Reflected in engagements which various parties have been engaged in to date.

- Assume that requirements are difficult to describe and communicate, and that an exploration model is better suited to achieve a valueable outcome
    - Promote activities which provider services manually or try novel approaches to connect different ideas/technologies to hopefully surface breakthroughs 
    - Operate in the business before evaluating what is valueable or not

##### Variations in Information Flow Model
In the system there are programs which generate data and managers which consume data.
There are 2 ways to connect the providers with the consumers and both should be considered.

- Enable providers who can use the platform to make their data FAIR
- The alternative is to enable requestors who want data to publish their interest in data sets

The latter approach might better facilitate achievement of long term goals as the data requests would be expected to align fairly directly to the long terms goals.


##### Sub Domains

When building any system there are invariable sub systems which should be identified and developed in as decoupled parts of a problem in order to be addressed comprehensively.  This is known as [Conways Law](https://en.wikipedia.org/wiki/Conway%27s_law)

It is suggested that it is appropriate to break the programmed down into sub services and consider DMS requirements to each individually.

Proposed sub service would be expected to include items like

- Log In (Identithy Provider Integration) Service
- Sign Up Service
- Submit Data Set
- Search for Data Set 
- Explore Data Set
- Request access to data set Service
- Retrieve Data Set Service
- Retrieve Media Service
- Free Text Query Service
- Ad Hoc Query Data Service

Possibly this differentiation is too fine grained and it might be appropriate to deliver the solution as
- One capability for one project for discovery aggregation
- A second capability for shared data repostory (data lake)
It is likely the problem domains are sufficiently differentiate to require specialized teams.

##### Central Capability Concept

The programme could deliver capabilities which are quite different in the approach they take. 
Some of these approaches have already been mentioned in the [data audit report](#data-audit)

The following are all possiblites:

- Centralized Meta Data Repository, Distribute Data Store
    - the Federation Style model
    - this approach would support register and find data set but not data access
    - onus on the providers to have the capability to serve the data

- Centralized Data Archive 
    - this approach would support put and retrieve data set but not index and search
    - onus is on providers to statically describe the type/form of their data and publish it centrally

- Decentralized Data Sharing
    - A peer to peer solution (think BitTorrent) might be viable.  Provider would need to given some tools to seed data into the network and requests some tools filter and search for data into the network.
    
- Decentralized Data Query
    - Given the need for provider data sovereignty along with the requirement for requestor access, a federation style decentralized data search might be an appropriate solution.  Providers would not need to give up their data but rather be provided tools to be able to respond to aggregate queries without having to actually share data.    

#### Data Management Concerns

The concerns of [data management](#data-management) are described here.

##### Processes
###### Copyright

If copyright is a signficant concern with some of the data sets, it may be appropriate to develop a process to life cycle the Copyright to Data Assoication.

###### Confidentiality

In addition to provide confidentialty mechanism in the solution, it may be necessary to life cycle confidentiality levels

###### Records Management

The data set may be appropriately considered a 'Record' in the sense of a records management with a implied life cycle (time to live). Processes to life cycle a data set may be required.


##### Meta Data Standards

To support discovery of data set it will be necessary to life cycle meta data for a data set.  Some standard going to be required.  There are options to

- Adopt a standard
    - If there are standards which the majority of providers are likely to know of they should probably be adopted.

- Develop new standard 
    - more likely to be fit for purpose if the environmental managers have specific known what to express what they are interested int.
    - a canonical model with translators to other formats (xlsx, cvs, stream,...)
    - the standard could evolve based on end user use cases as they arise

- Rather than having a standard consider a babel like translation service give people what they need and decouple producers of data from consumers of data.
    - Support multiple standards - Receive data in one format but make available in multiple.
    - This is central to modern organizational systems and is expressed as the [CQRS](https://martinfowler.com/bliki/CQRS.html) pattern.


##### Data Formats

The solution domain will necessarily involve transfer of data from providers through to requestors and a ability for the requestors to syntactially and semantically parse the information.

For the solution to be effective a consideration of the appropriate approach to facilitate the communication is required.

The [data audit](#data-audit) has identified data formats that providers currently use for data sets.

The solution design should consider the appropriateness of the following API contract technologies:
- Consider an API capability possible based on
    - REST API as a technical publication format such as swagger or Async API based on JSON Schema
    - Consider Apache Avro as technical data serialization format publication format
    - Consider capabilities which let users choose a format that works for them and converts the data into that format for them.


##### Data Access

From the [data licensing report](#dms-license) it is understood there are a variety of agreements governing access to the data.

The solution needs to consider how to provide capabilities to support access where there is some possibility.
This could include:
- Capability to describe reasons for non access
- Capability to life cycle data sharing agreements so they can be served to requestors for review
- Processes to request access
- Processes to approve access


As there are concerns data licensing the solution might need to consider techniques from Digital Rights Management to protect data re-distribution.

##### To support confidentiality

If data archival in the platform is required it will be necesary to have techniques to protect data at rest.
- This applies to File Storage, Relational, Messaging
    - and this will require capabilities to manage Encryption Keys
        - Some cloud providers provide key management capabilities 

##### Storage

To store meta data or provider data relational storage is  likely required.
There are options about which technology approach to proceed with
- Consider Postgress
- Consider SQL Server

##### Service Scaling

The solution should be implemented such as to support horizontal scaling of services as this is fairly standard capability today. As such the solution should consider deployment via
- Cloud specfic load Balancing, scaling, paas offerings
- Docker based deployment scaling
- Kubernetes

##### Online Transaction Processing

The solution will have some requirement for online transaction process to implement the any of the sub systems providing self service transactions.  Services which provide OLTP need storage which acheives
- Fast Simple Reads and Writes
- Indexing of specific columns
- High Availability Required

As the solution is decomposed into service it can be expected the storage solution will apply repetitively across the microservices.

CQRS (Command Query Responsibility Pattern) should be consider to make meta data writable but also support multiple approaches to data query

##### Search

It may be appropriate for the solution to free text index data and make this avaiable through a search function. 

The solution may need to ELT meta data and data into search storage solutions such as [Elastic Search](https://www.elastic.co/start?ultron=[B]-Elastic-ANZ-Exact&blade=adwords-s&Device=c&thor=elastic%20search&gclid=EAIaIQobChMI4-DYg7OG4wIVBZGPCh1RxwX3EAAYASAAEgLtUvD_BwE).

##### Media

The [data audit](#data-audit) has already provided evidence that the data sets include non relational content data (image and video).
The solution will need to address how to store and serve this data to provide storage media and retrieve media.
Option include:
- use of S3
- use of Azure Storage
- use of HDFS

##### Data Movement

- Reliable and Secure 
    - Consider [Apache Ni-Fi](https://nifi.apache.org/)

##### Pipeline



##### Offline Analystics Processing

To support all use cases, a solution may provide a capability for offline analytics processing.
The requirements here are quite differnet from OLTP.
There is a need for 
-Ad Hoc Queries , 
-Fast reads, no writes, 
-Indexes on every column
- High availability should not required

The solution may need to implement capabities based on
- HDFS (Data Lake)
- SQL on Hadoop solution
    - Consider cloudera
    - Consider Presto
    - Consider Hive

And the solution will need to consider ETL solution to populate Data Lake from OLTP 


##### Identity and Authorization

A solution which provides access to protected resources need identity management capability(or integration) and authorization capabity.

The solution needs a sign up registration process to provision users into the space.
   
The solution needs an approach for how to authorize users to access resources (data in this case).
The solution may acheive this through
- one time vs time based access
- Request/approval authorization process
- Invitation based authorization

### Vendor Selection

The programmed needs to consider the suitability of provider the solution through use of
- vendor provided
versus
- open source provided
technologies.


## DMS5: Conduct an audit of available data (measured and modelled) against program design and synthesis & reporting requirements (DMS2), including: quality, availability, location/custodian, and caveats for use.  Identify data products that need updating, modifications or need for new data sets. 

An audit activity could certainly provide value in surfacing the available data.  It does have the drawback that it is a snapshot in time update.

It may be appropriate to augment this with a process/proedure by which data providers or data requestors can describe data they have available or can easily make available or have a need for.  A capability that provides this may acheive a similar outcome to an audit in a more continuous and end user engaging manner.

## DMS6: Ensure access, licensing and IP arrangements are fit for purpose. 
Review licensing, data provenance and transparency, and IP of relevant data sets.  Identify requirements to secure access to and use of data, including data-sharing mechanisms to align with the needs of identified audience range and reporting products. 


## Terminology

<a id="data-management"></a>
Data Management - [Here is a good description for what 'Data Management' entails](https://www.fsd.uta.fi/aineistonhallinta/en/)


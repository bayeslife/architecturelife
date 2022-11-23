# Architecture Topics

## Access and Authorization

[OpenId and OAuth](https://www.youtube.com/watch?v=996OiexHze0)

## Messaging Approaches

- RabbitMQ - Traditional message broker
- Kafka - focus on speed and reliability. Streaming only.  Complexity high
    - Event Hub - Azure Kafka as a service
- NATS - focus on simplicity. Has streaming but not highly available streaming as yet

### MicroService Architecture
[This talk is useful to run through microservice architecture challengs](https://www.youtube.com/watch?v=fhZwzm-d9ys)
- Sagas - as the way to acheive distributed transactions
- CQRS - as the way to acheive distributed queries
- Event Sourcing or Transactional Outbox - as the way to achieve atomicity between update state and create events

## Event Sourcing

[Lessons Learned Implementing CQRS and Event Sourcing](https://itnext.io/1-year-of-event-sourcing-and-cqrs-fb9033ccd1c6)

## Complex Event Processing
- [EEP](https://github.com/darach/eep-js)
- [RxJS](https://www.learnrxjs.io/)

## Rules Engine
Nice summary [here](https://blog.waylay.io/tag/rules-engine/)
- [Waylay.io](https://www.waylay.io)

## Statistics Libraries

- [Simple Statistics](https://simplestatistics.org)
- [Math.js](http://mathjs.org/)

## Front End Framework

- React
- Vue

[Comparison](https://medium.com/javascript-scene/top-javascript-frameworks-and-topics-to-learn-in-2019-b4142f38df20)

## Front End Components

[Vuetify](https://vuetify.com)

## Site Hosting Options
- netlify.com
- gitlab.com
- [Atomist](https://atomist.com/) - full javascript CI/CD
- [ZeitNow](https://zeit.co/now)

## Email Related Services

- mailinator.com - Public Email
- mailtrap.io - SMTP Server useful for dev/staging environments so email isnt sent to customers.


- [A framework for rendering web emails](https://mjml.io/)


## Architecture Frameworks

- TMForum
- Archimate
- [Clean Architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
- [Disciplined Agile](http://disciplinedagiledelivery.com/the-dad-role-of-architecture-owner/) - How architect fits into agile
- [Explicit Archtecture](https://herbertograca.com/2017/11/16/explicit-architecture-01-ddd-hexagonal-onion-clean-cqrs-how-i-put-it-all-together/)
- [Ports and Adapters](https://softwarecampament.wordpress.com/portsadapters/)

## SDLC Concerns

- [12factor.net](https://12factor.net/) - Describes the characteristics of contemporary solutions.

### Javascript Test Frameworks
- [Riteway](https://github.com/ericelliott/riteway)
- Mocha
- Jest
- Ava

### Full Stack Application Templates Approachs
- Yeoman : a bit dated now
- React: react has its own templating  though its CLI
- Vue : Vuew has its own templates through its CLI
- [Mern](https://mern.io) : Havent yet tried these

### Log Analytics
- Splunk
- Graylog
- ElasticSearch/Kinana
- FluentD

## Notebook Paradigms
- ObservableHQ
- Jupyter

## Browser Based Sandbox

- [Code Sandbox](http://codesandbox.io)
- [Plkr](https://plnkr.co/) : Angular specific
- [Code Pen](https://codepen.io/)

## Data Pipeline

- segment.io
- funnel.io


## Data Streaming

- [MicroBatching](https://engineering.salesforce.com/applying-the-micro-batching-pattern-to-data-transfer-5b5f72509da2/)
- [Spark Streaming](https://www.databricks.com/blog/2015/07/30/diving-into-apache-spark-streamings-execution-model.html)
- [Spark Stream API](https://spark.apache.org/docs/latest/streaming-programming-guide.html)

## Data Integration
- [XMPro](https://xmpro.com/) : 
- [Reekoh](https://reekoh.com/) : Brisbane based, Merrick Spain introduced

## Warehousing Platforms
- [Snowflake](https://www.snowflake.com/)


## Synchronize Data Sets
- [Zapier Cloud Based Integration Platform](https://zapier.com/)

## Surface private services to the internet

- ngrok.io 
- xip.io
- [localtunnel](https://localtunnel.github.io)

## Browser Error Aggregation

- Rollbar
- Loggly
- Sentry
- AirBrake
- ErrorCeption

## Services To Testing Request Content
- Request Bin - this was shut down
- [Post Bin](https://postb.in)

## Testing 

### TDD
[Red-Green-Refactor](https://www.youtube.com/watch?v=EZ05e7EMOLM) - This has been a breath of fresh air as it address how to minimize writing tests but get the benefits of TDD.

### Unit Testing
Riteway
Mocha
Ava
Jest

###  Integration Testing
- [TestCafe](https://www.npmjs.com/package/testcafe)
- [Cypress](https://www.cypress.io/)


## Dependency Management
- npm link
- [yalc](https://github.com/whitecolor/yalc) - Facilitates development with multiple packages without publishing
- yarn public-local

## Dashboard Analytics Platforms

- [Cube JS](https://github.com/statsbotco/cube.js) [Cube.dev](https://cube.dev/) Definitely looks like it would address problems with had in original MineQ project where we were attempting to send large results sets to the front end to support the analytics views.  I think it effectively creates materialized viewes in the DB layer for every query the front end needs.  The query just simple does a fetch from the back end.


### Query Storage 
- MongoDB
- Click House
- Big Query
- AWS Athena


### Methodology

- Scrum
- Kanban
- [Disciplined Agile](http://disciplinedagiledelivery.com/)
- [Spiral](https://csse.usc.edu/TECHRPTS/1988/usccse88-500/usccse88-500.pdf)
- [Red-Green-Refactor](https://www.youtube.com/watch?v=EZ05e7EMOLM) - Can we say this is a methodology

### API Definition
- [Swagger](https://swagger.io/) - Focus on REST API
- [AsyncAPI](https://www.asyncapi.com/) - Focused on Event Driven Architecture


### Schemas

#### Measurements
- [ISO 19156 Observations & Measurements (O&M) data model](https://en.wikipedia.org/wiki/Observations_and_Measurements)


### IOT Architecture

- 2022-03-10 [Industrial Internet Reference Architecture](https://www.iiconsortium.org/IIRA.htm)
- [Microsoft Reference Architecture for IOT](https://aka.ms/iotrefarchitecture)

## Architect in Agile

[Architect-Agile-Manifesto](https://www.infoq.com/articles/architect-agile-manifesto/)


### ORMs (Object Relational Mapping)

- I have used [Sequelize](https://sequelize.org/) extensively

### Icons

[Undraw](https://undraw.co/illustrations) - freely available icons which can be styled to match a brand


### Threat Assessment

- STRIDE  (Spoofing,Tampering, Repudiation,Information Disclouser, Denial of Service, )
- DREAD
- [LINDUNN Privacy](https://www.linddun.org/) (Linkability, Identifyability, Non Repudiation, Detectability, Disclosure of Information,  Unawareness, Non-compliance)


### Cyber Security Assessment Frameworks

[AESCSF](https://aemo.com.au/initiatives/major-programs/cyber-security/aescsf-framework-and-resources) - is a cyber security framework for the energy space.  Provides a method which could be followed.

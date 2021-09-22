# Architecture Topics

## Current View for How to Break Down Technology
Analytics – Science – Problem Formation
Story/Constraints – Elicitation – Problem Breakdown
Planning - Collaboaration - Progressing team solution

Access - Authentication and Authorization – Making a solution available

Integration – Standardization – Getting data from external systems
Infrastructure – Realization – Resource provisioning
DevOps – Automation – Reducing SDLC cycle time

Dashboard – Presentation – Effective information display and control
Push – Notification – Pushing information to users

Forecasting  - Modelling – IO Functions
- Programmatic – System Development
- Training  - Machine Learninghttps://nivo.rocks/components
API – Interfacing – Surfacing model behaviour
Pipelines – Composition – Joining information sources/streams

Warehousing - Data Life Cycling – What and how data is stored

Testing – Verification – Change with confidence
Operating - Monitoring
Supporting - Assisting

## Access and Authorization

[OpenId and OAuth](https://www.youtube.com/watch?v=996OiexHze0)

## Infrastructure - Messaging Approaches

- [Apache Camel](https://camel.apache.org/)
- [RabbitMQ](https://www.rabbitmq.com/) - Traditional message broker
- [Kafka](https://kafka.apache.org/) - focus on speed and reliability. Streaming only.  Complexity high
    - Event Hub - Azure Kafka as a service
- [NATS](https://nats.io/) - focus on simplicity. Has streaming but not highly available streaming as yet


### APIs - MicroService Architecture
[This talk is useful to run through microservice architecture challengs](https://www.youtube.com/watch?v=fhZwzm-d9ys)
- Sagas - as the way to acheive distributed transactions
- CQRS - as the way to acheive distributed queries
- Event Sourcing or Transactional Outbox - as the way to achieve atomicity between update state and create events

## Pipelines - Complex Event Processing
- [EEP](https://github.com/darach/eep-js)
- [RxJS](https://www.learnrxjs.io/)

## Inferencing - Rules Engine
Nice summary [here](https://blog.waylay.io/tag/rules-engine/)
- [Waylay.io](https://www.waylay.io)

## Statistics Libraries

- [Simple Statistics](https://simplestatistics.org)
- [Math.js](http://mathjs.org/)

## Presentation - Front End Framework

- React
- Vue

[Comparison](https://medium.com/javascript-scene/top-javascript-frameworks-and-topics-to-learn-in-2019-b4142f38df20)

## Presentation - Front End Components

[Vuetify](https://vuetify.com)

## DevOps - Site Hosting Options
- netlify.com
- gitlab.com
- [Atomist](https://atomist.com/) - full javascript CI/CD
- [ZeitNow](https://zeit.co/now)

## Notification - Email Related Services

- mailinator.com - Public Email
- mailtrap.io - SMTP Server useful for dev/staging environments so email isnt sent to customers.

- [A framework for rendering web emails](https://mjml.io/)

## Architecture Frameworks

- TMForum
- [UML](https://en.wikipedia.org/wiki/Unified_Modeling_Language)
- [Togaf](https://www.opengroup.org/certifications/togaf)
- [Archimate](https://pubs.opengroup.org/architecture/archimate3-doc/)
- [Clean Architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
- [Disciplined Agile](http://disciplinedagiledelivery.com/the-dad-role-of-architecture-owner/) - How architect fits into agile
- [Explicit Archtecture](https://herbertograca.com/2017/11/16/explicit-architecture-01-ddd-hexagonal-onion-clean-cqrs-how-i-put-it-all-together/)
- [Ports and Adapters](https://softwarecampament.wordpress.com/portsadapters/)
- [Cell based framework](https://github.com/wso2/reference-architecture/blob/master/reference-architecture-cell-based.md)
- [3 Factor Framework](https://3factor.app/)
- [Real Value Architecture]()
- [Purdue Enterprise Architecture Mode](https://en.wikipedia.org/wiki/Purdue_Enterprise_Reference_Architecture)
- [Department of Defence](https://dodcio.defense.gov/Library/DoD-Architecture-Framework/dodaf20_sv1/)
- [Open Group Agile Architecture](https://www.opengroup.org/AgileArchitecture)
- [C4 Model](https://c4model.com/)
- [Polylight](https://polylith.gitbook.io/polylith/introduction/polylith-in-a-nutshell)
- [Cloud Security Alliance](https://cloudsecurityalliance.org/) - Has security focused cloud architecture content

## Decision Frameworks
- [Waterfall]()
- [Scrum]()
- [Cynefin](https://medium.com/@warren2lynch/scrum-what-is-cynefin-framework-8c33c01bcc19) <img src="https://miro.medium.com/proxy/1*CrhLcEx6NUqXNC8k3hUSXQ.png" width="200"/>

### Development Methodology

- Scrum
- [Disciplined Agile Kanban](https://www.disciplinedagileconsortium.org/resources/Documents/Posters/PosterLifecycleLean.pdf)
- [Disciplined Agile](http://disciplinedagiledelivery.com/)
- [Spiral](https://csse.usc.edu/TECHRPTS/1988/usccse88-500/usccse88-500.pdf)
- [Red-Green-Refactor](https://www.youtube.com/watch?v=EZ05e7EMOLM) - Can we say this is a methodology

## Presentation - Reactivity UI Architecture Frameworks
- MVC
- [Flux Architecture - Creating UIs](https://facebook.github.io/flux/)
- [Mobx](https://mobx.js.org)
- [Recoil](https://recoiljs.org/)
- [Valtio](https://github.com/pmndrs/valtio)

## DevOps - SDLC Concerns

- [12factor.net](https://12factor.net/) - Describes the characteristics of contemporary solutions.

### Development - Javascript Test Frameworks
- [Riteway](https://github.com/ericelliott/riteway)
- Mocha
- Jest
- Ava

### DevOps - Full Stack Application Templates Approaches
- Yeoman : a bit dated now
- React: react has its own templating  though its CLI
- Vue : Vuew has its own templates through its CLI
- [Mern](https://mern.io) : Havent yet tried these


### Presentation - Visualization Framework
- [D3]https://d3js.org/
- [Deck GL](https://deck.gl/#/examples/core-layers/trips-layer)
- [Nivo](https://nivo.rocks/components)

### 3d Visualization 
- [Resium (React Cesium)](https://resium.darwineducation.com/) - A 3d viewer

### Chart Libraries
- [User React Visualization](https://uber.github.io/react-vis/)
- [Recharts](https://recharts.org)


### Presentation - Dashboard Templates Approaches

- https://flatlogic.com/
- https://coreui.io/

### Operating - Monitoring - Log Analytics
- Splunk
- Graylog
- ElasticSearch/Kinana
- FluentD

## Presentation - Notebook Paradigms
- ObservableHQ
- Jupyter

## Browser Based Sandbox

- [Code Sandbox](http://codesandbox.io)
- [Plkr](https://plnkr.co/) : Angular specific
- [Code Pen](https://codepen.io/)
- [JS Fiddle](https://jsfiddle.net/)
- [JS Bin](https://jsbin.com/)
- [Gitpod](https://www.gitpod.io/)

## Pipeline - Cloud Data Pipeline

- segment.io
- [Funnel.io](https://funnel.io/),
- https://www.datagekko.com


# Pipeline - Data Pipeline Approaches

| Cloud | Product    | Base Technology | Description | 
| ----- | ---------- | --------------- | ----------- | 
| GCP   | Composer   | Apache AirFlow         | About definining a data pipeline and its run schedule in code |
| GCP   | Data Flow  | Apache Beam                |  An sdk which produces a programming paradigm to execute parallel execution. |
| GCP   | Data Proc  | Apache Spark and Hadoop | A distributed query engine which is really on part of the data pipeline requirement | 
| GCP   | Data Prep  | Trifacta                |  Cloud based, visual design tool |
| Azure  | DataBricks  | Apache Spark   | A distributed query engine which is only part of the data pipeline requirement |
| Azure | Data Factory | MQuery, Hadoop | Provides prep,  
| AWS  | QuickSight  |                 |  Cloud based, visual design pipeline tool |
| AWS  | Glue  |                 |  Serverless data pipeline and data catalog |
| AWS  | Athena |  | Serverless SQL query for content save in S3 buckets |
| AWS | EMR | Apache Spark and Hadoop | Distributed query engined |
| AWS | Data Pipeline |  | Orchestration of Pipeline using other AWS services |
| Kubeflow | Kubeflow | Kubernetes | a way to express and managed pipeline jobs |

# Data Warehouse 

| Cloud | Product    | Base Technology | Description | 
| ----- | ---------- | --------------- | ----------- | 
| GCP   | BigQuery   |          | About definining a data pipeline and its run schedule in code |


## Integration - Synchronize Data Sets
- [Zapier Cloud Based Integration Platform](https://zapier.com/)

## Dev Ops - Surface private services to the internet

- ngrok.io 
- xip.io
- [localtunnel](https://localtunnel.github.io)

## Infrastructure - Domain Name Services

nip.io - Provides DNS lookup for 1.2.3.4.nip.io to the corresponding IP address

## Monitoring - Browser Error Aggregation

- Rollbar
- Loggly
- Sentry
- AirBrake
- ErrorCeption

## Verification - Services To Test Request Content
- Request Bin - this was shut down
- [Post Bin](https://postb.in)

## Verification - Testing 

### Verification - TDD
[Red-Green-Refactor](https://www.youtube.com/watch?v=EZ05e7EMOLM) - This has been a breath of fresh air as it address how to minimize writing tests but get the benefits of TDD.

### Verification - Unit Testing
Riteway
Mocha
Ava
Jest

###  Integration Testing
- [TestCafe](https://www.npmjs.com/package/testcafe)
- [Cypress](https://www.cypress.io/)

### Quality Checklists
[Power of 10 Rules](https://en.wikipedia.org/wiki/The_Power_of_10:_Rules_for_Developing_Safety-Critical_Code?source=post_page---------------------------)

## Dev Ops - Dependency Management
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
- Azure Storage

### Data Mininig Methodology

- [CRISP DM](https://www.sv-europe.com/crisp-dm-methodology)


### API Definition
- [Swagger](https://swagger.io/) - Focus on REST API
- [Open API](https://www.openapis.org/)
- [AsyncAPI](https://www.asyncapi.com/) - Focused on Event Driven Architecture
- [RAML](https://raml.org/)


### Schemas
- [Cloud Events](https://github.com/cloudevents/spec) - Standard for what events should contain

#### Measurements
- [ISO 19156 Observations & Measurements (O&M) data model](https://en.wikipedia.org/wiki/Observations_and_Measurements)


### IOT Architecture

[Microsoft Reference Architecture for IOT](https://aka.ms/iotrefarchitecture)


## Architect in Agile

[Architect-Agile-Manifesto](https://www.infoq.com/articles/architect-agile-manifesto/)

### Catalog of Conferences Related to Software Development

[it call for papers list](https://github.com/softwaremill/it-cfp-list/blob/master/README.md)


## How to break projects down

- [Breaking Apart Monolith](https://techbeacon.com/app-dev-testing/how-break-apart-monolith-without-destroying-your-team) - Domain Driven Design, Reverse Conways Law, 
- [Event Storming](https://en.wikipedia.org/wiki/Event_storming) - A facilitation technique technique to identify a domain model. [eventingstorming.com](https://www.eventstorming.com/)


## Why projects fail

[Standish report on project succcess/failure](https://www.projectsmart.co.uk/white-papers/chaos-report.pdf)

## What technologies are popular on the web

[BuiltWith](https://trends.builtwith.com/) - This site exposes technology usage on the web. Similar to idea I had a few years back.
 
 ## Deployment Strategies
 [Nice overview](https://thenewstack.io/deployment-strategies/)
 - Recreate
 - Rolling
 - Canary
 - Blue/Green


 ## Mapping Library

 [Article providing commentary on the set of mapping apis](https://flatlogic.com/blog/top-javascript-maps-api-and-libraries/)
 - Google Maps
 - Leaflet.js
 - MapBox


## UI Styling Approaches

- Bootstrap
- Material Design
- [Microsoft UI Fabric React](https://developer.microsoft.com/en-us/fabric#/)-With a theme designer [here](https://fabricweb.z5.web.core.windows.net/pr-deploy-site/refs/heads/master/theming-designer/index.html)


## SSL / Certificates

[Lets Encrypt](https://letsencrypt.org/) - provides get mechanism to add SSL to a web site


## Monitoring Public Sites

[DataDog](https://app.datadoghq.com/)
[New Relic](https://newrelic.com/)

## Cloud Logging Aproaches
[winston](https://www.npmjs.com/package/winston)

## Usage Analytics

- Google Analytics
- Azure ??
- [MixPanel](https://mixpanel.com/)

## Wire Frames

    https://whimsical.com/mind-maps
    

## ORM Frameworks

Sequelize - Node JS
Entity Framework - .Net
Hibernate - Java
??? - Python

## Process Manager

Capability to keep processes running if they fall over.

- forever - used at Spark
- [Non Sucking Service Manager](https://nssm.cc/) - Used for EOS Premier, Windows
- [PM2](https://pm2.io/) - Considering for use at Quartile One, Windows
- [Node Windows](https://www.npmjs.com/package/node-windows) - used at Muswellbrook Coal , Windows

## Branching Approaches

- [Gitflow](https://nvie.com/posts/a-successful-git-branching-model/)
- [Gitflow extension to git](https://github.com/petervanderdoes/gitflow-avh/wiki)
- [Trunk Based](https://trunkbaseddevelopment.com/)

## Secret Sharing

- Last Pass
- [One Time Secret](https://onetimesecret.com/)

## Vulnerability Scanning

- [Tenable.io](https://www.tenable.com/products)

### Scheduling

- [Google OR](https://developers.google.com/optimization)

### Parsing and Transformation from language to language

- [Unifieid](https://unifiedjs.com/)


### CMS  (Content Management System)

- [Cosmic](https://www.cosmicjs.com/)
- [Prismic]()
- [Contentful]()
- [Wordpress]()
- [Sharepoint]()
    - [PnP api is the recommended way to call sharepoint from javascript](https://pnp.github.io/pnpjs/getting-started/)

## Inefficiency

- [Last Reponsible Moment](https://blog.codinghorror.com/the-last-responsible-moment/)
- [7 Wastes](https://hackernoon.com/7-wastes-in-lean-software-development-and-how-to-prevent-them-7bi3tqp?source=rss)


## Applied Search

This tools index a site and enable context sensitive search

- [algolia](https://www.algolia.com/) - Online search
- [lunrjs](ttps://lunrjs.com/) - Offline search


## Approaches to real time client server integration

- Web Sockets
- Web RTC

## Micro Front Ends
Approach to breaking up application

- Module Federation


## Functional Programming Libraries

- [Ramba](https://ramdajs.com)
- [RxJs](https://www.learnrxjs.io/)


## Persistent Logs
- [Hyperdrive](https://github.com/hypercore-protocol/hyperdrive)

## Peer to Peer
- [Hypercore](https://hypercore-protocol.org/)

## Enterprise Service Bus
- [IBM Message Broker](https://www-01.ibm.com/common/ssi/cgi-bin/ssialias?infotype=an&subtype=ca&appname=gpateam&supplier=649&letternum=ENUSA05-1237), 
- [Mulesoft](https://www.mulesoft.com/), 
- [Red Hat Fuse](https://www.redhat.com/en/technologies/jboss-middleware/fuse)


## Ontology

[Relates ontology to simulation](https://www.sne-journal.org/fileadmin/user_upload_sne/SNE_Issues_OA/SNE_24_2/articles/sne.24.2.10243.tn.OA.pdf)


## Manage multiple environments

- [nvm]()
- [volta]()
# Architecture Topics

## Access and Authorization

[OpenId and OAuth](https://www.youtube.com/watch?v=996OiexHze0)

## Messaging Approaches

- RabbitMQ - Traditional message broker
- Kafka - focus on speed and reliability. Streaming only.  Complexity high
- NATS - focus on simplicity. Has streaming but not highly available streaming as yet

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

## Email Related Services

- mailinator.com - Public Email
- mailtrap.io - SMTP Server useful for dev/staging environments so email isnt sent to customers.

## Architecture Frameworks

- TMForum
- Archimate
- [Clean Architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
- [Disciplined Agile](http://disciplinedagiledelivery.com/the-dad-role-of-architecture-owner/) - How architect fits into agile
- [Explicit Archtecture](https://herbertograca.com/2017/11/16/explicit-architecture-01-ddd-hexagonal-onion-clean-cqrs-how-i-put-it-all-together/)

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

## Synchronize Data Setse
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
Red-Green-Refactor

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

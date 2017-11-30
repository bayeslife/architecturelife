# What went wrong

A request has been made to provide feedback on where things went wrong in delivering the Storm Trooper API integration.  The suggestions provided below are proposed changes that could be considered as part of future development.

Suggestions:

### Separate Service/Capability delivery from Product Delivery

Service capability should be delivered independently of specific product project deliverables. Robustness as a capability outcome unconstrained by project specific constraints.  

This approach is also known as 2 speed IT

This addresses:

https://jira.vodafone.co.nz/jira/browse/ESA-22
If the prequal had been developed independently of StormTrooper specific Siebel configuration there is a reasonable chance it would have worked for CSS.

https://jira.vodafone.co.nz/jira/browse/MOB-3463
If the modifyOrder API was developed without specific end to end knowledge of Storm Trooper specific requirements , the concerns of informational transparency would have been considered.

### More focus on testability

StormTrooper integration with Bandit was not tested until production. The project team took the approach to move the code through to upper environments in the absence of test results (either positive of negative) in lower environments with the consuming application.

- The project took the view that it would not be the bottleneck in the SDLC and therefore pushed forward with the delivery at the expense of a robust solution.
- The test environment was not easily accessible to the consuming application
- The SIT test environment was a resource under contention and the project had limited access to the environment
- The SIT test environment




### As built needs to be continuously reported rather than documented.

As components are released they should appear onto component inventory dashboards such that there is transparency for subsequent reuse.






Minimize one-time side effects in integrations
More focus on testability in the SDLC




All test cases/scenario created before build, all product projects to be able to provide test cases retrospectively

Test cases for each of the known issues with existing API
Regression suite fully automated including functional and non-functional aspects (reporting, monitoring)
Consumer implemented and tested in parallel against mock responses
Documented on confluence linked from implementation and test collateral.

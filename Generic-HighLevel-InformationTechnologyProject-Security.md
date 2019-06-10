# Security Related Success Factors

What is the winning hand to achieve successful development, delivery, and operation where success is measured by minimizing cyber security risks.

## Relevant Standards

- [NIST](https://www.nist.gov/cyberframework) - A comprehensive United States Department of Commerce CyberSecurity Framework.

- [ISM](https://www.cyber.gov.au/ism) - This is a government standard provides a comprehensive framework which comprehensively covers information security risks and controls.
- [](https://www.cyber.gov.au/publications)

- [OWASP](https://owasp.org/) and [OWASP Top Ten](https://www.owasp.org/images/7/72/OWASP_Top_10-2017_%28en%29.pdf.pdf) - Standards related to web application security concerns.  In particular these would be considered during development of an information portal.  

## Framework Practice

The standards mentioned above provide guidelines to align the SDLC with contemporary security baseline practices. 
The following summarizes activity expected as part of project/programme delivery life cycle. 

- Consideration
    - To ensure that security concerns are considered in the SDLC, it is important that there is a security role appointed in the project team. 

- Access
    - Access (local or remote) to protected resources require supply of multifactor credentials which identify the end user
    - Access is provided on the basis of least privilege
    - Networks are segregated
    - Where possible white listing is used to allow access
    - Software tokens with timeouts are used to access systems
    - Shared access it not allowed
    - Password limitations are enforced to reduce brute force attack vector
    - Firewalls are configured to limit allow traffic to that which is to be supported
    - Resource access occurs over SSL layer to provide confidentiality

- Data
    - Data identified as confidential is stored at rest in encrypted form
    - Data in transit is by default encrypted to prevent eavesdropping
    - Where appropriate Data Integrity checks are implemented to reduce the risk of tampering
    - Data export and transport is controlled
    - Database access is limited to those people with a need to know
    
- Processes
    - Change control processes are used
    - Backups of important information are maintained

- Development
    - Software environments are restricted to those who need to use them.  Dev/Test environments are limited to project teams.
    - Code reviews - code reviews are undertaken in part to consider security implications of developed code

- Maintenance
    - Maintenance and Repair of systems are performed and logged

- Protect
    - Where appropriate audit logs are implemented and review
    - Where appropriate mechanisms are implemented to achieve resilience (load balancing)


- Detect
    - Detected events are analyzed to understand attack targets and methods
    - Impact of events is determined

- Monitoring
    - The network is monitored
    - Vulnerability scans are undertaken periodically
    - Solutions are assessed by independent security consultants who can probe and report on vulnerabilities

- Respond
    - Incidents are reported
    - Coordination with stakeholders occurs

- Suppliers
    - All suppliers (including cloud providers) are expected to operate their services using security baseline practices. 
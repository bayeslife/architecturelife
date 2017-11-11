# Reflections of a solution archiect
Here are some thoughts on working as a solution architect.

There are some aspects of the role that are reasonably well understood.  Architects have responsibility for preparing solution guidance and high level designs and taking these to the architecture review forums.

In addition to this at various times as an architect there has been unrealistic expectations
- that I should have technical hands on knowledge of the solution implementation.
- that I should have knowledge of release and the status of release through the life cycle
- that I should have knowledge about the state of testing the status of defects
- that I should be able to help out when developers face issues
- that I should review all project collateral including requirements
- that I should have in depth experience around non functionals including capacity, scaleability, licensing and monitoring
- that I should describe cost effective solutions
- that I have expertise in any solution domain
- that I should be able to pick up any detailed design and understand it
- that I maintain a heads up display on organizational maturity to sell, order, provisioning, bill and support particular capabilities
- that I link all decisions to requirements  and manage the traceability of the solution back to business
- that I know the state of all projects and their inflight scope statements to be able to decide which project is the best project to address specific issues.

Covering all these is going to be an task which any architect can only perform poorly

## What is more reasonable?

There are opportunities for different types of architects but I will offer suggestions from a general point of view.

1. Solution Architects should operate vertically (end to end solution) as well as horizontally (a specific capability across multiple projects). Both short term(delivery) and long term (capability) thinking should be considered in architectural decisions. Where the solution architect has end to end responsibility they should assist in developing requirements and test scenarios and describing the contracts between the different components that come together to form the functional solution.
2. Where the solution architect has capability responsibility, they should be maintaining as built representations of the capability (ideally as real time interactive dashboards) and have knowledge of source code repositories, regression test suites, test environments and the contracts which the capability requires of consumers.
3. The capability architect should be able to publish as built IP to be consumed by end to end architects to allow them to get some understanding of the paradigms supported by the capability.
4. The capability architect should be able to publish as built IP to be consumed by end to end architects to allow them to get some understanding of the paradigms supported by the capability.

How can an architect capture the capability IP as well as capture the end to end solution interactions and communicate this to stakeholders.

The stakeholders are going to be
- programme and project managers
- other capability architects
- development teams
- test teams

## Terminology/Lingo

The first tool of communication will be having easily shared and reused terms.

- Understanding the nuances and relationships between terms will be important.
- The ability to link from content to term definitions will be important
- The ability to see how term relates to other terms will be important.
- The for the content to be univerisally available at least in a read only format will be important.

Suggestion: To define the terms as an information model in a tool such as Enterprise Architect as UML class diagrams and publish the terms along with significant information viewpoints to Confluence or a GitHub Pages site  where the terms can be individually referenced.


# Inventory

Secondly the next tool of communication will be to have an ongoing inventory that is reflective of current state and can be utilized into various types of diagrams (sequence, collaboration, use case, mapping).

- Items in inventory should be classified/stereotyped to agreed terms.
- Keeping the repository current here will be important
- The repository will need to reflect multiple levels of abstraction
- The repository should place items that are in the same category together so that its relatively easy to identify when a set member exists and can be reused.
- Ideally the inventory could be updated automatically as capabilities/components come online.
- The inventory will need some organization/categorization but also an ability to search across the inventory to allow architects to find items previously identified.
- The inventory should be automatically exportable and importable so that the information can be validate/cross refererenced/published for use outside of the architectural practice.

Suggestion: The suggestion is to maintain inventory in Enterprise Architect modelling tool but also in a code repository.  
Enterprise architect is used to reference inventory, express relationships between inventory and produce many types of diagrams.
The code repository serves to provide rigour and traceability to the state of the information and facilitates application of automated processing (validation, quality, publishing, analysis) of the information.

# Solution Models

Thirdly the next tool is to facilitate presentation of solutions.

- Solutions viewpoints including use case diagrams, sequence diagrams, class diagrams and other to be able to consider a solution from multiple views
- Solutions viewpoints should not copy inventory or terms but instead should refer to the instances and ideally allow click through to see further details.
- Solution viewpoints ideally would be styled independently of content
- Solution viewpoints ideally could be formed dynamically as queries
- Solution viewpoints would ideally be stylistically consistent across projects/architects in order to allow rapid understanding of solutions viewpoints across a wide group.

Suggestion: There is no one tool which satisfies the needed.  Enterprise Architect is a reasonable tool to allow presentation of diagrams from a repository of terms and inventory items.  This could be augmented by living documents generated off the content separately committed into the source code repository by a build pipeline. It would be the living documents which would be standard and be styled independently.

# Design Patterns and Standards

Architects should strive to minimize the informational delta with each solution.  A way to achieve this is to separate out pattern content and reference the design pattern applicable any one solution.

- Design Patterns should use defined terms
- Design patterns should available for ongoing collaborative development and refinement.
- Design patterns should be identified as inventory.

Suggestion:  Design patterns are a good fit to confluence.

# Specification/Instruction/Prescription

Ultimately when working with teams that will deliver components it is necessary to development descriptions that are not descriptive but instead are prescriptive.  In this area architecture should support test driven development and behaviour driven development.

- Developing specification should be a collaborative exercise with analysis, development and test teams.
- Specifications should defined using Terms.
- Specification should be easily converted into unit and integration tests
- Specification should separate data (variance) from logic (invariance)
- Specifications should be able to cross reference other artefacts and be cross referenced from inventory items.

Suggestion: Architect, BA, Developmer and  Tester collaboratively use Jira to create tasks that describe functionality in terms of Cucumber specifications.    Cucumber specifications do a good job of separating logic from data, can be understood by end users using the appropriate language and can be executed automagically (if required). Tags can be used to markup tests so they can be linked back to inventory and terms.

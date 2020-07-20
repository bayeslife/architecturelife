# What to strive for with CD-CD

***Note assumption is that we dont have dedicate on shore Dev Ops people but rather we need to be self sufficient without dev ops***
- this probably needs to be questioned
- I dont count the Ukraine because they are to far removed from day to day activity


## Capability which is used by many teams

This is becomming a commodity capability and it doesnt make sense to roll our own.

Options at scale
- Gitlab (Auto Dev Ops)
- Azure DevOps
- GitHub Actions
- Circle CI

- Jenkins, Octupus
    - These are not be software defined.

## Capability to build

- Projects

- It is useful to put projects into groups. [Project Example](https://gitlab.com/eos-premier) - [Team Example](https://gitlab.com/q1-team) - [Example Packages](https://gitlab.com/q1-packages)


- Libraries - These are quite different...more testing...always give a new version...publish an artefact

## Capability to build on premise or on cloud

- Gitlab - Easy to run gitlab runner locally which we had to do (to get past build limits before) [Example](https://gitlab.com/integratedsolutionsprojects/groundgauge2/contamination/-/settings/ci_cd)
- Azure Dev Ops - Easy to run the runner locally, had to do this to make use of specific .Net framework for GeoDocs.
- Havent inquired on doing this with Jenkins builds

***Ability to build on a customers environment*** may provide some benefits.

## Capability to Test
- This must come from the project rather than from CI/CD because developers need to be able to run tests themselves

## Capabiltiy to Lint
- This must come from the project rather than from CI/CD because developers need to be able to run tests themselves


## Capability to security analyze
- This is where we gain benefit from cloud CI/CD provider.

- Gitlab [SAST](https://docs.gitlab.com/ee/user/application_security/sast/) [DAST](https://docs.gitlab.com/ee/user/application_security/dast/)

##  Capability to store/retrieve artefacts

- Nexus (Ukraine)
- GitHub (private artefact repository) [features](https://github.com/features/packages)
- GitLab (private artefact repository) [npm repo](https://docs.gitlab.com/ee/user/packages/npm_registry/)

- Default to publishing libraries to public domain as that tends to be easy to retrieve. Negative example [Aurecon Nexus Repo](https://aurecon-package-manager.australiasoutheast.cloudapp.azure.com/)

## Environments

- Environments
    - CI/CD pipeline needs to support environments
        - Gitlab does but we havent really use it 

    - Review Apps: Gitlab Auto Dev Ops dynamically create environment per branch [For Example](https://gitlab.com/eos-premier/powerview-agent/pipelines/74324659)


## Maintain Secrets
Maintaining environment specific secrets

- I like the K8S approach to keep these inside the K8S cluster

- Gitlab lets variables be set at group or project level as well on per environment


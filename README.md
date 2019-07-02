# Jenkins
This is a helper markdown for creating a jenkins CI/CD build system.

# Requirements
- Must have blue ocean UI.
- Must have email notification support.
- Master and Agents:
    - Master handles UI, user approval steps.
    - Agents handle build pipeline stages.
    - Agents are scalable.
- Must have Bitbucket and Github support.
- Must have testing support:
    - OpenCover for .Net Core code coverage. [tutorial] (https://automationrhapsody.com/code-coverage-net-core-unit-tests-opencover)
- Maybe support for Selenium Grid
- Pipeline for .Net Core Api, Queue, Jobs projects
- Pipeline for React Redux project

# Setup

## Docker Jenkins
Create either a standard jenkins docker container:
```
docker run -p 8080:8080 -p 50000:50000 --name j1 -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts
```
or blueocean variant
```
docker run -p 8080:8080 -p 50000:50000 --name j1 -v jenkins_home:/var/jenkins_home jenkinsci/blueocean
```
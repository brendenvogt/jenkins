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

# Grab jenkins initial password

# Login with initial password

# Choose select plugins to install

- check bitbucket
- check github
- uncheck subversion
- check xUnit
# Click install and wait
# Create your first admin user
- Username
- Password
- Confirm Password
- Full Name 
- E-mail address
# save and continue
# Instance Configuration Set Jenkins Url. Set this to the final url if hosted or leave localhost for local
# Click save and finish
# Click Start using Jenkins
# Click create a new job 
# Select Freestyle project and give it a name
# Configure Pipeline
- Description
- Branch Source
    - Add repo url
    - Add credentials, Secret Text, Add secret, configure scope if needed, add id, save
    - Github personal access token
- (if Dockerfile not in root) Build Configuration 
- Orphaned Item Strategy
    - Max # of items to keep: 5
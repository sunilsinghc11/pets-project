# Spring PetClinic Application CICD [![Build Status](https://github.com/spring-projects/spring-petclinic/actions/workflows/maven-build.yml/badge.svg)](https://github.com/spring-projects/spring-petclinic/actions/workflows/maven-build.yml)

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/sunilsinghc11/pets-project.git) [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=7517918)

## CICD for the Spring Petclinic application

[See the presentation here](https://speakerdeck.com/michaelisvy/spring-petclinic-sample-application)

## Pre-requisites to Run Petclinic CICD

Spring Petclinic is a [Spring Boot](https://spring.io/guides/gs/spring-boot) application built using [Maven](https://spring.io/guides/gs/maven/) .

``` 
CICD Pipeline can be executed by logging into the Jenkins Server.
Jenkins URL http://35.90.13.23:8080/
Login with user admin and password provided seperately.
Once Logged in Click on Dashboard to view the pipeline
```
## Jenkins Pipeline
<img width=“1042” alt=“petclinic-pipeline” src="https://github.com/sunilsinghc11/pets-project/blob/main/pipeline.png">
This Pipeline Execuetion, would compile the code, test, upload the artifact to Artifactory Repository and then Build a Docker Image.

## To Clone the Repo Locally
```
git clone https://github.com/sunilsinghc11/pets-project.git
cd pets-project
```
## Files used for Setting up the CICD Process.

[Jenkinsfile](https://github.com/sunilsinghc11/pets-project/blob/main/Jenkinsfile).

[Dockerfile](https://github.com/sunilsinghc11/pets-project/blob/main/Dockerfile).

## Maven Settings to Configure Artifactory Repository Server 

[settings.xml](https://github.com/sunilsinghc11/pets-project/blob/main/settings.xml)

[pom.xml](https://github.com/sunilsinghc11/pets-project/blob/main/pom.xml) . Updates to add jFrog Artifactory to upload Build artifact



The Docker Image to Pull:

```
docker pull sunilsc/petclinic
docker run -d -p 8080:8080 docker pull sunilsc/petclinic
```

1. Navigate to the Petclinic

    Visit [http://localhost:8080](http://localhost:8080) in your browser.

## Looking for something in particular?

|Spring Boot Configuration | Class or Java property files  |
|--------------------------|---|
|The Main Class | [PetClinicApplication](https://github.com/spring-projects/spring-petclinic/blob/main/src/main/java/org/springframework/samples/petclinic/PetClinicApplication.java) |
|Properties Files | [application.properties](https://github.com/spring-projects/spring-petclinic/blob/main/src/main/resources) |
|Caching | [CacheConfiguration](https://github.com/spring-projects/spring-petclinic/blob/main/src/main/java/org/springframework/samples/petclinic/system/CacheConfiguration.java) |


## Interaction with other open-source projects

One of the best parts about working on the Spring Petclinic application is that we have the opportunity to work in direct contact with many Open Source projects. We found bugs/suggested improvements on various topics such as Spring, Spring Data, Bean Validation and even Eclipse! In many cases, they've been fixed/implemented in just a few days.
Here is a list of them:

| Name | Issue |
|------|-------|
| Spring JDBC: simplify usage of NamedParameterJdbcTemplate | [SPR-10256](https://jira.springsource.org/browse/SPR-10256) and [SPR-10257](https://jira.springsource.org/browse/SPR-10257) |
| Bean Validation / Hibernate Validator: simplify Maven dependencies and backward compatibility |[HV-790](https://hibernate.atlassian.net/browse/HV-790) and [HV-792](https://hibernate.atlassian.net/browse/HV-792) |
| Spring Data: provide more flexibility when working with JPQL queries | [DATAJPA-292](https://jira.springsource.org/browse/DATAJPA-292) |

## Contributing

The [issue tracker](https://github.com/spring-projects/spring-petclinic/issues) is the preferred channel for bug reports, feature requests and submitting pull requests.

For pull requests, editor preferences are available in the [editor config](.editorconfig) for easy use in common text editors. Read more and download plugins at <https://editorconfig.org>. If you have not previously done so, please fill out and submit the [Contributor License Agreement](https://cla.pivotal.io/sign/spring).

## License

The Spring PetClinic sample application is released under version 2.0 of the [Apache License](https://www.apache.org/licenses/LICENSE-2.0).

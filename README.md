This is quick overview for Budget Project.<br/>
Latest project version is hosted in bitbucket private repositories and I update from time to time repositories mentioned below. They are stripped off sensitive data and maintenance of  so many repos for pet project as a single developer/qa/devops/whatever maintenance is time consuming task. Some things may not be up to date on github but I sync repos from time to time.<br/><br/> Project is hosted under https://konradboniecki.com.pl but it's not expected to work all the time, especially during development/refactorings.

Budget consists of multiple springboot based microservices. All of them are build on top of my own chassis which holds common configuration for plugins, dependency management and defines common topics, for example logging. This way, its not visible (except configuration) that services are using config-client for fetching configuration

Below repositories does not contain any sensitive data and chassis. Therefore they are not runnable.

Repository | link |
--- | --- |
Config repository | https://github.com/MilczekT1/config-git |
Account Management | https://github.com/MilczekT1/account-mgt-svc
Password Management | https://github.com/MilczekT1/password-mgt-svc
Mail | https://github.com/MilczekT1/mail-svc
Family Management | https://github.com/MilczekT1/family-mgt-svc
Budget Management | https://github.com/MilczekT1/budget-mgt-svc
MVC | https://github.com/MilczekT1/mvc-svc

Project contains also config server and gateway, but they are single class applications.

Testing:<br/>
Code coverage >= 80% <br/>
Contract testing: In order to verify if communication between services is not broken at build time I use consumer driven contracts (Spring Cloud Contract). API producer has to pass generated tests for given contracts and once they are verified API client can mock response for that contract in integration tests. It saved my "platform" several times :)

BDD: Acceptance tests which are executed against local environment (maven build) and production environment depending on given profile.

 Details | Tool |
--- | --- |
Tracking | Spring Cloud Sleuth + Zipkin (https://konradboniecki.com.pl/zipkin/)
Monitoring | Prometheus, Grafana
Databases | MongoDB && MySQL
CI/CD | CircleCi, Kubernetes, Nexus |

[Screenshot](./img/circleci-chassis.png)

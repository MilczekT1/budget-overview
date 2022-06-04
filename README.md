# Budget project overview <br/>
Project is hosted under https://konradboniecki.com.pl and is designed to work 24/7 but it's not expected to work during development/refactorings. I'll be rich someday and have 2 environments :)

Budget consists of multiple SpringBoot-based microservices. All of them are build on top of my own chassis which holds common configuration for plugins, dependency management and defines common topics, for example logging. This way, it's not visible that services are using config-client for fetching configuration etc.

## Repositories
Below repositories don't contain chassis therefore they are not runnable.

Repository | CI | Coverage | Sonar |
---|---|---|---|
[Config repository](https://github.com/MilczekT1/config-git) | N/A | N/A | N/A |
[Config Server](https://github.com/MilczekT1/config-server) | [![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/config-server/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_config-server&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_config-server) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_config-server&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_config-server) |
[Gateway](https://github.com/MilczekT1/gateway) | [![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/gateway/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_gateway&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_gateway) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_gateway&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_gateway) |
[Account Management](https://github.com/MilczekT1/account-management) | [![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/account-management/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_account-management&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_account-management) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_account-management&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_account-management) |
[Password Management](https://github.com/MilczekT1/password-management) | [![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/password-management/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_password-management&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_password-management) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_password-management&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_password-management) |
[Mail](https://github.com/MilczekT1/mail-sender) | [![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/mail-sender/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_mail-sender&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_mail-sender) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_mail-sender&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_mail-sender) |
[Family Management](https://github.com/MilczekT1/family-management) | [![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/family-management/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_family-management&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_family-management) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_family-management&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_family-management) |
[Budget Management](https://github.com/MilczekT1/budget-management) | [![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/budget-management/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_budget-management&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_budget-management) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_budget-management&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_budget-management) |
[MVC](https://github.com/MilczekT1/mvc) | [![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/mvc/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_mvc&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_mvc) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_mvc&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_mvc) |

# Testing:<br/>
Code coverage >= 80% <br/>
Contract testing: In order to verify if communication between services is not broken at build time I use consumer driven contracts (Spring Cloud Contract). API producer has to pass generated tests for given contracts and once they are verified API client can mock response for that contract in integration tests. </br>All contracts are stored in contract-repository. Artifact is hosted in nexus. Api producer downloads contracts during build  in order to generate tests. Api Consumer download stubs during build in order to provide up to date mocks. This saved my "platform" several times from giving up:)

BDD: Acceptance tests which are executed against local environment (maven build) and production environment depending on given profile.

# Tech stack:<br/>
 Details | Tool |
---|---|
Backend | ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=java&logoColor=white) ![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white) |
FrontEnd | ![Bootstrap](https://img.shields.io/badge/bootstrap-%23563D7C.svg?style=for-the-badge&logo=bootstrap&logoColor=white) |
Monitoring | ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=white) ![Grafana](https://img.shields.io/badge/grafana-%23F46800.svg?style=for-the-badge&logo=grafana&logoColor=white) |
Databases | ![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white) ![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)  |
CI/CD | ![CircleCI](https://img.shields.io/badge/circle%20ci-%23161616.svg?style=for-the-badge&logo=circleci&logoColor=white) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)  ![Apache Maven](https://img.shields.io/badge/Apache%20Maven-C71A36?style=for-the-badge&logo=Apache%20Maven&logoColor=white), Nexus |                                  |
Tracing | Spring Cloud Sleuth + Zipkin (https://konradboniecki.com.pl/zipkin/) |

# Screenshot of chassis pipeline
![plot](./img/circleci-chassis.png)
# Release procedure
![plot](./img/release-procedure.png)


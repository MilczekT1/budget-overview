# Budget project overview <br/>
Project is hosted under https://konradboniecki.com.pl and is designed to work 24/7 but it's not expected to work during development/refactorings. I'll be rich someday and have 2 environments :)

Budget consists of multiple SpringBoot-based microservices. All of them are build on top of my own chassis which holds common configuration for plugins, dependency management and defines common topics, for example logging. This way, it's not visible that services are using config-client for fetching configuration etc.

# Tech stack:<br/>
Details | Tool |
---|---|
Backend | ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=java&logoColor=white) ![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white) ![Swagger](https://img.shields.io/badge/-Swagger-%23Clojure?style=for-the-badge&logo=swagger&logoColor=white) |
FrontEnd | ![Bootstrap](https://img.shields.io/badge/bootstrap-%23563D7C.svg?style=for-the-badge&logo=bootstrap&logoColor=white) ![Thymeleaf](https://img.shields.io/badge/Thymeleaf-%23005C0F.svg?style=for-the-badge&logo=Thymeleaf&logoColor=white) |
Monitoring | ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=white) ![Grafana](https://img.shields.io/badge/grafana-%23F46800.svg?style=for-the-badge&logo=grafana&logoColor=white) |
Databases | ![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white) ![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)  |
CI/CD | ![CircleCI](https://img.shields.io/badge/circle%20ci-%23161616.svg?style=for-the-badge&logo=circleci&logoColor=white) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)  ![Apache Maven](https://img.shields.io/badge/Apache%20Maven-C71A36?style=for-the-badge&logo=Apache%20Maven&logoColor=white) Nexus |                                  |
Tracing | Spring Cloud Sleuth + Zipkin (https://konradboniecki.com.pl/zipkin/) |

## Repositories

Repository | version | CI | Quality Gate & coverage | Other metrics |
---|---|---|---|---|
[Chassis](https://github.com/MilczekT1/chassis) | ![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/MilczekT1/chassis?color=blue&label=release&sort=semver) | [![CircleCI](https://dl.circleci.com/status-badge/img/gh/MilczekT1/Chassis/tree/master.svg?style=shield)](https://dl.circleci.com/status-badge/redirect/gh/MilczekT1/Chassis/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_Chassis&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_Chassis) </br> [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_Chassis&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_Chassis) | [![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_Chassis&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_Chassis) </br> [![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_Chassis&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_Chassis) |
[Config repository](https://github.com/MilczekT1/config-git) | N/A | N/A | N/A | N/A |
[Config Server](https://github.com/MilczekT1/config-server) | ![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/MilczekT1/config-server-service?color=blue&label=release&sort=semver) | [![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/config-server/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_config-server&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_config-server) </br> [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_config-server&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_config-server) | [![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_config-server&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_config-server) </br> [![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_config-server&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_config-server) |
[Gateway](https://github.com/MilczekT1/gateway) | ![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/MilczekT1/gateway?color=blue&label=release&sort=semver) |[![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/gateway/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_gateway&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_gateway) </br> [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_gateway&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_gateway) | [![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_gateway&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_gateway) </br> [![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_gateway&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_gateway) |
[Account Management](https://github.com/MilczekT1/account-management) | ![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/MilczekT1/account-management?color=blue&label=release&sort=semver) | [![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/account-management/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_account-management&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_account-management) </br> [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_account-management&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_account-management) | [![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_account-management&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_account-management) </br> [![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_account-management&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_account-management) |
[Password Management](https://github.com/MilczekT1/password-management) | ![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/MilczekT1/password-management?color=blue&label=release&sort=semver) | [![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/password-management/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_password-management&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_password-management) </br> [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_password-management&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_password-management) | [![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_password-management&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_password-management) </br> [![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_password-management&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_password-management) |
[Mail](https://github.com/MilczekT1/mail-sender) | ![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/MilczekT1/config-server-service?color=blue&label=release&sort=semver) | [![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/mail/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_mail&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_mail) </br> [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_mail&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_mail) | [![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_mail&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_mail) </br> [![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_mail&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_mail) |
[Family Management](https://github.com/MilczekT1/family-management) | ![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/MilczekT1/family-management?color=blue&label=release&sort=semver) | [![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/family-management/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_family-management&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_family-management) </br> [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_family-management&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_family-management) | [![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_family-management&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_family-management) </br> [![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_family-management&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_family-management) |
[Budget Management](https://github.com/MilczekT1/budget-management) | ![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/MilczekT1/budget-management?color=blue&label=release&sort=semver) | [![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/budget-management/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_budget-management&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_budget-management) </br> [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_budget-management&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_budget-management) | [![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_budget-management&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_budget-management) </br> [![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_budget-management&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_budget-management) |
[MVC](https://github.com/MilczekT1/mvc) | ![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/MilczekT1/mvc?color=blue&label=release&sort=semver) | [![CircleCI](https://circleci.com/gh/MilczekT1/mail/tree/master.svg?style=shield)](https://circleci.com/gh/MilczekT1/mvc/tree/master) | [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_mvc&metric=coverage)](https://sonarcloud.io/summary/new_code?id=MilczekT1_mvc) </br> [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_mvc&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MilczekT1_mvc) | [![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_mvc&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_mvc) </br> [![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=MilczekT1_mvc&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=MilczekT1_mvc) |

# Testing:<br/>
Code coverage >= 80% <br/>
Contract testing: In order to verify if communication between services is not broken at build time I use consumer driven contracts (Spring Cloud Contract). API producer has to pass generated tests for given contracts and once they are verified API client can mock response for that contract in integration tests. </br>All contracts are stored in contract-repository. Artifact is hosted in nexus. Api producer downloads contracts during build  in order to generate tests. Api Consumer download stubs during build in order to provide up to date mocks. This saved my "platform" several times from giving up:)

BDD: Acceptance tests which are executed against local environment (maven build) and production environment depending on given profile.


# Chassis pipeline
![plot](./img/circleci-chassis.png)
# Release procedure
![plot](./img/release-procedure.png)


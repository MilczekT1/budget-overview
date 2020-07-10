This is quick overview for Budget Project.
Budget consists of multiple springboot based microservices. All of them are build on top of my own chassis which holds common configuration for plugins, dependency management and defines common topics, for example logging. This way, its not visible (except configuration) that services are using config-client for fetching configuration

* config repository: https://github.com/MilczekT1/config-git
* Account Management https://github.com/MilczekT1/account-mgt-svc
* Password Managementhttps://github.com/MilczekT1/password-mgt-svc
* Mail https://github.com/MilczekT1/mail-svc
* Family Management https://github.com/MilczekT1/family-mgt-svc
* Budget Managementhttps://github.com/MilczekT1/budget-mgt-svc
* MVC https://github.com/MilczekT1/mvc-svc

Project contains also config server and gateway, but they are single class applications.

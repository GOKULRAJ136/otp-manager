[![Maven Package upon a push](https://github.com/mosip/commons/actions/workflows/push_trigger.yml/badge.svg?branch=release-1.2.0.1)](https://github.com/mosip/commons/actions/workflows/push_trigger.yml)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=mosip_commons&metric=alert_status)](https://sonarcloud.io/dashboard?branch=release-1.2.0.1&id=mosip_commons)


# Commons

## Overview
As the name suggests, Commons refers to all the common services (also called "kernel") that are used by other modules of MOSIP.

## Databases
Refer to [SQL scripts](db_scripts).

## Build & run (for developers)
The project requires JDK 21.0.3
and mvn version - 3.9.6.
1. Build and install:
    ```
    $ cd kernel
    $ mvn install -DskipTests=true -Dmaven.javadoc.skip=true -Dgpg.skip=true
    ```
2. Build Docker for a service:
    ```
    $ cd <service folder>
    $ docker build -f Dockerfile
    ```
## Configuration files
Kernel OTP Manager uses the following configuration files that are accessible in this [repository](https://github.com/mosip/mosip-config/tree/master).
Please refer to the required released tagged version for configuration.
```
application-default.properties
kernel-default.properties
```

## Configuration
[Configuration-Application](https://github.com/mosip/mosip-config/blob/master/application-default.properties) and
[Configuration-Kernel](https://github.com/mosip/mosip-config/blob/master/kernel-default.properties) defined here.

## Deploy
To deploy Commons services on Kubernetes cluster using Dockers refer to [Sandbox Deployment](https://docs.mosip.io/1.2.0/deploymentnew/v3-installation).

## Test
Automated functional tests available in [Functional Tests repo](https://github.com/mosip/mosip-functional-tests).

## APIs
API documentation is available [here](https://mosip.github.io/documentation/1.2.0/kernel-otpmanager-service.html).

## License
This project is licensed under the terms of [Mozilla Public License 2.0](LICENSE).



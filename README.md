# Tanzania HRHIS - NHIF Mediator
[![Java CI Badge](https://github.com/SoftmedTanzania/nhif-mediator-hrhis/workflows/Java%20CI%20with%20Maven/badge.svg)](https://github.com/SoftmedTanzania/nhif-mediator-hrhis/actions?query=workflow%3A%22Java+CI+with+Maven%22)
[![Coverage Status](https://coveralls.io/repos/github/SoftmedTanzania/nhif-mediator-hrhis/badge.svg?branch=development)](https://coveralls.io/github/SoftmedTanzania/nhif-mediator-hrhis?branch=development)

An [OpenHIM](http://openhim.org/) mediator for handling system integration  from HRHIS to NHIF.

# Getting Started
Clone the repository and run `npm install`

Open up `src/main/resources/mediator.properties` and supply your OpenHIM config details and save:

```
  mediator.name=NHIF-Mediator-HRHIS
  # you may need to change this to 0.0.0.0 if your mediator is on another server than HIM Core
  mediator.host=localhost
  mediator.port=4000
  mediator.timeout=60000

  core.host=localhost
  core.api.port=8080
  # update your user information if required
  core.api.user=openhim-username
  core.api.password=openhim-password
```

To build and launch our mediator, run

```
  mvn install
  java -jar target/nhif-mediator-hrhis-0.1.0-jar-with-dependencies.jar
```
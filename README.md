# A Guide to deploying instances of Samply [Bridgehead](https://github.com/samply/bridgehead-deployment) and Samply [SampleLocator](https://github.com/samply/sample-locator).

Prerequisites for installing are: [_docker_](https://docs.docker.com/get-docker/) and [_docker-compose_](https://docs.docker.com/compose/).

[Recommeded hardware specifications](https://samply.github.io/bbmri-fhir-ig/howtoJoin.html#general-requirements).

## Deployment

Attached to this README.md should be two docker-compose.yml files. One for the Bridgehead and one for the SampleLocator. It is possible to deploy both of them on the same server, however since the goal is to simulate and test the environment for which these tools were designed it is recommended that they are deployed on separate servers. For the purposes of this guide lets assume that this is the case.

In order to access the full funcionality of both the Bridgehead and SampleLocator an edit of the SampleLocator docker-compose.yml file is required. Since both of these tools are still in development it is reasonable to assume that the steps in this guide might not be relevant for future releases, so this guide is relevant only to the versions specified in the docker-compose files. Specifically

First you need to `cd` into the directory which houses the docker-compose.yml file. They can be deployed by using:

`sudo docker-compose up -d`

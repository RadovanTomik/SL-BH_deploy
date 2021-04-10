# A Guide to deploying testing/demo instances of Samply [Bridgehead](https://github.com/samply/bridgehead-deployment) and Samply [SampleLocator](https://github.com/samply/sample-locator).

[Recommeded hardware specifications](https://samply.github.io/bbmri-fhir-ig/howtoJoin.html#general-requirements).

## Deployment

Attached to this README.md should be three `docker-compose.yml` files. One for the Bridgehead, one for the SampleLocator and one for both of them. It is possible to deploy both of them on the same server, however the goal is to simulate and test the environment for which these tools were designed, thus it is recommended that they are deployed on separate servers. Since both of these tools are still in development it is reasonable to assume that the steps in this guide might not be relevant for future releases, so this guide is relevant only to the versions specified in the docker-compose files.

### Bridgehead
1. Install git, docker and docker compose. Note: paste following commands into a shell of your choice, e.g. bash, .zsh.

  Debian:

 `sudo apt-get update && sudo apt-get upgrade && sudo apt-get install git && sudo apt-get install docker && sudo apt-get install docker-compose`

  MacOS:

 Install [homebrew](https://brew.sh), then:

 `brew install git docker docker-compose`

 2. Deploy docker images.

 - When deploying both tools on the same server:

 `sudo docker-compose -f docker-compose.both.yml up -d`

 - When deploying BridgeHead on a separate server:

`sudo docker-compose -f docker-compose.BH.yml up -d`

### Sample Locator
1. **Note: if you have already deployed both tools on the same server skip to step 2.**   
   Install git, docker and docker compose. Note: paste following commands into a shell of your choice, e.g. bash, .zsh.

  Debian:

 `sudo apt-get update && sudo apt-get upgrade && sudo apt-get install git && sudo apt-get install docker && sudo apt-get install docker-compose`

  MacOS:

 Install [homebrew](https://brew.sh), then:

 `brew install git docker docker-compose`

2. Modify docker-compose
3. Deploy docker images.

`sudo docker-compose -f docker-compose.SL.yml up -d`

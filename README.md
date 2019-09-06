
<!-- (SPDX-License-Identifier: CC-BY-4.0) -->  <!-- Ensure there is a newline before, and after, this line -->

# Hyperledger Explorer For Fabric v1.4.1 [![join the chat][rocketchat-image]][rocketchat-url]

[rocketchat-url]:https://chat.hyperledger.org/channel/hyperledger-explorer
[rocketchat-image]:https://open.rocket.chat/images/join-chat.svg
[![Build Status](https://jenkins.hyperledger.org/buildStatus/icon?job=blockchain-explorer-merge-x86_64)](https://jenkins.hyperledger.org/view/fabric/job/blockchain-explorer-merge-x86_64)
[![CII Best Practice](https://bestpractices.coreinfrastructure.org/projects/2710/badge)](https://bestpractices.coreinfrastructure.org/projects/2710)

<!-- badges -->

Hyperledger Explorer is a simple, powerful, easy-to-use, well maintained, open source utility to browse activity on the underlying blockchain network. Users have the ability to configure and build Hyperledger Explorer on MacOS and Ubuntu.

<a name="Release-Notes" />

# 1.0 Release Notes    <!-- do not remove this comment, ensure there is a blank line before each heading -->

| Hyperledger Explorer Version                                | Fabric Version Supported                                         | NodeJS Version Supported                          |
| --                                                          | --                                                               | --                                                |
| <b>[v0.3.9.4](release_notes/v0.3.9.4.md)</b> (June 18, 2019) | [v1.4.1](https://hyperledger-fabric.readthedocs.io/en/release-1.4) | [8.11.x](https://nodejs.org/en/download/releases) |
| <b>[v0.3.9.3](release_notes/v0.3.9.3.md)</b> (May 24, 2019) | [v1.4](https://hyperledger-fabric.readthedocs.io/en/release-1.4) | [8.11.x](https://nodejs.org/en/download/releases) |
| <b>[v0.3.9.2](release_notes/v0.3.9.2.md)</b> (May 16, 2019) | [v1.4](https://hyperledger-fabric.readthedocs.io/en/release-1.4) | [8.11.x](https://nodejs.org/en/download/releases) |
| <b>[v0.3.9.1](release_notes/v0.3.9.1.md)</b> (Feb 28, 2019) | [v1.4](https://hyperledger-fabric.readthedocs.io/en/release-1.4) | [8.11.x](https://nodejs.org/en/download/releases) |
| <b>[v0.3.9](release_notes/v0.3.9.md)</b> (Feb 7, 2019)      | [v1.4](https://hyperledger-fabric.readthedocs.io/en/release-1.4) | [8.11.x](https://nodejs.org/en/download/releases) |
| <b>[v0.3.8](release_notes/v0.3.8.md)</b> (Dec 13, 2018)     | [v1.3](https://hyperledger-fabric.readthedocs.io/en/release-1.3) | [8.x.x](https://nodejs.org/en/download/releases)  |
| <b>[v0.3.7](release_notes/v0.3.7.md)</b> (Sep 21, 2018)     | [v1.2](https://hyperledger-fabric.readthedocs.io/en/release-1.2) | [8.x.x](https://nodejs.org/en/download/releases)  |
| <b>[v0.3.6.1](release_notes/v0.3.6.1.md)</b> (Sep 21, 2018) | [v1.2](https://hyperledger-fabric.readthedocs.io/en/release-1.2) | [8.x.x](https://nodejs.org/en/download/releases)  |
| <b>[v0.3.6](release_notes/v0.3.6.md)</b> (Sep 6, 2018)      | [v1.2](https://hyperledger-fabric.readthedocs.io/en/release-1.2) | [8.x.x](https://nodejs.org/en/download/releases)  |
| <b>[v0.3.5.1](release_notes/v0.3.5.1.md)</b> (Sep 21, 2018) | [v1.1](https://hyperledger-fabric.readthedocs.io/en/release-1.1) | [8.x.x](https://nodejs.org/en/download/releases)  |
| <b>[v0.3.5](release_notes/v0.3.5.md)</b> (Aug 24, 2018)     | [v1.1](https://hyperledger-fabric.readthedocs.io/en/release-1.1) | [8.x.x](https://nodejs.org/en/download/releases)  |
| <b>[v0.3.4](release_notes/v0.3.4.md)</b> (Jul 13, 2018)     | [v1.1](https://hyperledger-fabric.readthedocs.io/en/release-1.1) | [8.x.x](https://nodejs.org/en/download/releases)  |

<a name="Dependencies" />

# 2.0 Dependencies    <!-- do not remove this comment, ensure there is a blank line before each heading -->

Verified Docker versions supported:
* [Docker CE 18.09.2 or later](https://hub.docker.com/search/?type=edition&offering=community&operating_system=linux)
* [Docker Compose 1.14.0](https://docs.docker.com/compose)

<a name="Fabric-Network-Setup" />

# 3.0 Fabric Network Setup    <!-- do not remove this comment, ensure there is a blank line before each heading -->

- <b>Note: This section will take some time to complete.</b>
- Setup your own network using the [Building Your First Network](http://hyperledger-fabric.readthedocs.io/en/latest/build_network.html) tutorial from Hyperledger. Once you setup the network, please modify the values in `/blockchain-explorer/app/platform/fabric/config.json` accordingly.
- Hyperledger Explorer defaults to utilize [fabric-samples/first-network](https://github.com/hyperledger/fabric-samples).
- Make sure to set the environment variables `CORE_PEER_GOSSIP_BOOTSTRAP` and `CORE_PEER_GOSSIP_EXTERNALENDPOINT` for each peer in the docker-compose.yaml file. These settings enable the Fabric discovery service, which is used by Hyperledger Explorer to discover the network topology.


<a name="Run-Hyperledger-Explorer-using-Docker" />

# 4.0 Run Hyperledger Explorer Using Docker    <!-- do not remove this comment, ensure there is a blank line before each heading -->

There is also an automated deployment of the **Hyperledger Explorer** available via **docker** given the following requirements are met:

* **BASH** installed
* **Docker** is installed on deployment machine.
* **Docker Compose** is installed on deployment machine.

<a name="Docker-Docker-Repository" />

## 4.1 Docker Repository   <!-- do not remove this comment, ensure there is a blank line before each heading -->

* Hyperledger Explorer docker repository `https://hub.docker.com/r/hyperledger/explorer/`
* Hyperledger Explorer PostgreSQL docker repository `https://hub.docker.com/r/hyperledger/explorer-db`


<a name="Run-Hyperledger-Explorer-Using-Docker-Compose" />

## 4.2 Run Hyperledger Explorer Using Docker Compose    <!-- do not remove this comment, ensure there is a blank line before each heading -->

* Modify an example of docker-compose.yaml to align with your environment
    * networks > mynetwork.com > external > name
    ```yaml
    networks:
        mynetwork.com:
            external:
                name: net_byfn
    ```
    * services > explorer.mynetwork.com > volumes
      * Connection profile path (ex. ./examples/net1/config.json)
      * Connection profile directory path (ex. ./examples/net1/connection-profile, which is referred from config.json)
      * Directory path for crypto artifacts of fabric network (ex. ./examples/net1/crypto)
    ```yaml
        volumes:
          - ./examples/net1/config.json:/opt/explorer/app/platform/fabric/config.json
          - ./examples/net1/connection-profile:/opt/explorer/app/platform/fabric/connection-profile
          - ./examples/net1/crypto:/tmp/crypto
    ```
    * When you connect the explorer to your fabric network through bridge network, you need to set `DISCOVERY_AS_LOCALHOST` to `false` for disabling hostname mapping into `localhost`.
    ```yaml
        explorer.mynetwork.com:
            ...
            environment:
            ...
            - DISCOVERY_AS_LOCALHOST=false
    ```

* Run the following to start up explore and explorer-db services after starting your fabric network:
    ```
    cd /blockchain-explorer
    docker-compose up -d
    ```

* To stop services without removing persistent data, run the following:
    ```
    docker-compose down
    ```

* In this docker-compose.yaml, two named volumes are allocated for persistent data (for Postgres data and user wallet), if you would like to clear these named volumes, run the following:
    ```
    docker-compose down -v
    ```

<a name="License" />

# 5.0 License    <!-- do not remove this comment, ensure there is a blank line before each heading -->

Hyperledger Explorer Project source code is released under the Apache 2.0 license. The README.md, CONTRIBUTING.md files, and files in the "images", "__snapshots__" folders are licensed under the Creative Commons Attribution 4.0 International License. You may obtain a copy of the license, titled CC-BY-4.0, at http://creativecommons.org/licenses/by/4.0/.

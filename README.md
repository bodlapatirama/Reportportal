# EPAM Report Portal
[![Join Slack chat!](https://reportporal-slack-auto.herokuapp.com/badge.svg)](https://reportporal-slack-auto.herokuapp.com)
[![stackoverflow](https://img.shields.io/badge/reportportal-stackoverflow-orange.svg?style=flat)](http://stackoverflow.com/questions/tagged/reportportal)
[![License](https://img.shields.io/badge/license-GPLv3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0.html)

Report Portal organized into multiple repositories.

Application Core based on micro-services architecture and includes list of mandatory services.
> IMAGE: 

### Repositories structure

ReportPortal consists of the following services:
- [`service-registry`](https://github.com/reportportal/service-registry) Redis. Used for distributed cache.
- [`service-authorization`](https://github.com/reportportal/service-authorization) Authorization Service. In charge of access tokens distribution
- [`service-gateway`](https://github.com/reportportal/service-gateway) Gateway Service. Main entry point to application. Port used by gateway should be opened and accessible from outside network.
- [`service-api`](https://github.com/reportportal/service-api) API Service. Application Backend
- [`service-ui`](https://github.com/reportportal/service-ui) UI Service. Application Frontend
- [`service-jira`](https://github.com/reportportal/service-jira) JIRA Service. Interaction with JIRA
- [`service-rally`](https://github.com/reportportal/service-rally) Rally Service. Interaction with Rally

Other repositories stored according to next rules
- `service-*` - micro-services which is a part of Application
- `commons-*` - common libraries, models, etc., used by micro-services

Addapters (client side code) related repositories:

- `client-*` - http clients, which process HTTP request sending
- `agent-*` - custom reporters (mostly custom Listeners), which monitor test events and trigger event sending via client-*
- `logger-*` - logger appenders, which helps to collect logs, wire it with test case via agent-* and send to server via client-*


### Installation steps with Docker

1. Install [Docker](http://docs-stage.docker.com/engine/installation/) (Docker Engine, Compose, Swarm, etc)
2. Deploy [mongoDB](https://docs.mongodb.com/manual/installation/) 
3. Deploy ReportPortal using `docker-compose`.

  ```
  docker-compose up 
  ```
  
  - Example of compose descriptor available in repository root: [docker_compose.yaml example](https://github.com/reportportal/reportportal/blob/master/docker-compose.yml)

## Contribution

There are many different ways to contribute to Report Portal's development, just find the one that best fits with your skills. Examples of contributions we would love to receive include:

- **Code patches**
- **Documentation improvements**
- **Translations**
- **Bug reports**
- **Patch reviews**
- **UI enhancements**

Big features are also welcome but if you want to see your contributions included in Report Portal codebase we strongly recommend you start by initiating a chat though our Team.

### Documentation

* [Wiki and Guides](https://github.com/reportportal/reportportal/wiki)
* [User Manual](http://reportportal.io/#documentation)

### Community / Support

* [Open Slack chat](https://reportporal-slack-auto.herokuapp.com)
* Report Portal Google Group (comming soon)
* [GitHub Issues](https://github.com/reportportal/reportportal/issues)
* [Stackoverflow Questions](http://stackoverflow.com/questions/tagged/reportportal)

### License

Report Portal is [GNU General Public License v3.0](http://www.gnu.org/licenses/gpl-3.0.html).


[![HitCount](https://hitt.herokuapp.com/reportportal/reportportal.svg)](https://github.com/reportportal/reportportal)

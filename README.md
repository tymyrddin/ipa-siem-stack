# IPA SIEM Stack

Setting up a SIEM stack for IPA to facilitate the collection of data from survivor devices to be able to investigate [tactics, techniques, and procedures (TTPs)](https://github.com/tymyrddin/ipa-siem-stack/wiki) used by adversaries in their surveillance of survivors, and with found indicators of compromise (IoCs), in the future, offer incident response handling to survivors.

## Deployment strategy

Initially, we do not expect the usual high amount of data for a SIEM stack. The simplest and safest route is to install Docker and Compose on our production host, then connect to it over SSH. We can beg, borrow, and steal, and fork existing Dockers to make changes and build our own stack for IPA project purposes.

### Docker host

* [Choose host (OS)](https://github.com/tymyrddin/ipa-siem-stack/issues/1)
* [Setting up and hardening Docker host](https://github.com/tymyrddin/ipa-siem-stack/issues/2)
* [Installing Docker and Docker Compose](https://github.com/tymyrddin/ipa-siem-stack/issues/3)
* [Set up certificates](https://github.com/tymyrddin/ipa-siem-stack/issues/4)

### Dockers

* [Wazuh Indexer (SIEM Backend storage)](https://github.com/tymyrddin/ipa-siem-stack/issues/5)
* [Wazuh Dashboard (Kibana)](https://github.com/tymyrddin/ipa-siem-stack/issues/6)
* [Graylog](https://github.com/tymyrddin/ipa-siem-stack/issues/7)
* [Wazuh Manager/Agents (Wazuh server)](https://github.com/tymyrddin/ipa-siem-stack/issues/8)
* Grafana
* MISP
* OpenCTI
* TheHIVE/Cortex
* Velociraptor/Agents
* Shuffle
* InfluxDB/Telegraf


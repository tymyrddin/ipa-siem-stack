# IPA SIEM Stack

Setting up a SIEM stack for IPA to facilitate the collection of data from survivor devices to be able to investigate tactics, techniques, and procedures (TTPs) used by adversaries in their surveillance of survivors, and with found indicators of compromise (IoCs), in the future, offer incident response handling to survivors.

## Deployment strategy

Initially, we do not expect the usual high amount of data for a SIEM stack. The simplest and safest route is to install Docker and Compose on our production host, then connect to it over SSH. We can beg, borrow, and steal, and fork existing Dockers to make changes and build our own stack for IPA project purposes.

### Docker host

* [Choose host (OS)](https://github.com/tymyrddin/ipa-siem-stack/issues/1)
* [Setting up and hardening Docker host](https://github.com/tymyrddin/ipa-siem-stack/issues/2)
* [Installing Docker and Docker Compose](https://github.com/tymyrddin/ipa-siem-stack/issues/3)
* [Set up certificates](https://github.com/tymyrddin/ipa-siem-stack/issues/4)

### Dockers

* [Wazuh Indexer (SIEM Backend storage)](https://github.com/tymyrddin/ipa-siem-stack/issues/5)
* Wazuh Dashboards (Kibana)
* Graylog
* Wazuh Manager/Agents
* Grafana
* MISP
* OpenCTI
* TheHIVE/Cortex
* Velociraptor/Agents
* Shuffle
* InfluxDB/Telegraf

## Resources

* [Stories from Survivors: Privacy & Security Practices when Coping with Intimate Partner Abuse](https://dl.acm.org/doi/10.1145/3025453.3025875) , Tara Matthews, Kathleen O’Leary, Anna Turner, Manya Sleeper, Jill Palzkill Woelfer, Martin Shelton, Cori Manthorne*, Elizabeth F. Churchill, Sunny Consolvo, Google, Mountain View, CA, USA
* The [Digital Defenders Partnership](https://www.digitaldefenders.org/about-ddp/) offers support to human rights defenders under digital threat, and works to strengthen local rapid response networks.

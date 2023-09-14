# IPA SIEM Stack

Setting up a SIEM stack for IPA to facilitate the collection of data from survivor devices to be able to investigate [tactics, techniques, and procedures (TTPs)](https://github.com/tymyrddin/ipa-siem-stack/wiki) used by adversaries in their surveillance of survivors, and with found indicators of compromise (IoCs), in the future, offer incident response handling to survivors.

* [Roadmap](https://github.com/tymyrddin/ipa-siem-stack/wiki/Roadmap)

We can use the [Wazuh-docker](https://github.com/wazuh/wazuh-docker), and will put a Graylog docker in between the Backend Storage and the Dashboard. So first study their Dockerfiles and docker-compose files.

## Requirements

Certificates. For local development, self-signed.




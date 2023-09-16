# IPA SIEM Stack

Setting up a SIEM stack for IPA to facilitate the collection of data from survivor devices to be able to investigate [tactics, techniques, and procedures (TTPs)](https://github.com/tymyrddin/ipa-siem-stack/wiki) used by adversaries in their surveillance of survivors, and with found indicators of compromise (IoCs), in the future, offer incident response handling to survivors. See [Roadmap](https://github.com/tymyrddin/ipa-siem-stack/wiki/Roadmap).



## Requirements

## Increase max_map_count on the Docker host

Give at least 6 GB of memory to the Docker host that creates the containers (this does not necessarily mean that it is used, but Elasticsearch requires it to work):

```text
sudo sysctl -w vm.max_map_count=262144
```

Update the `vm.max_map_count` setting in `/etc/sysctl.conf` to set this value permanently. Just add it at the bottom. To verify it is set after rebooting, run `sysctl vm.max_map_count`.

## Create certificates

For development (self-signed certs), use the wazuh script:

```text
$ sudo docker-compose -f generate-indexer-certs.yml run --rm generator
```

For production, put your certificates in the `config/wazuh_indexer_ssl_certs` directory:

***Wazuh indexer:***

config/wazuh_indexer_ssl_certs/root-ca.pem
config/wazuh_indexer_ssl_certs/wazuh.indexer-key.pem
config/wazuh_indexer_ssl_certs/wazuh.indexer.pem
config/wazuh_indexer_ssl_certs/admin.pem
config/wazuh_indexer_ssl_certs/admin-key.pem

***Wazuh manager:***

config/wazuh_indexer_ssl_certs/root-ca-manager.pem
config/wazuh_indexer_ssl_certs/wazuh.manager.pem
config/wazuh_indexer_ssl_certs/wazuh.manager-key.pem

***Wazuh dashboard:***

config/wazuh_indexer_ssl_certs/wazuh.dashboard.pem
config/wazuh_indexer_ssl_certs/wazuh.dashboard-key.pem
config/wazuh_indexer_ssl_certs/root-ca.pem

## Get it running

Start the environment with docker-compose:

***In the foreground:***

```
$ docker-compose up
```

***In the background:***

```
$ docker-compose up -d
```

In development version, point browser to https://localhost, in production to https://domainname or https://IPaddress.

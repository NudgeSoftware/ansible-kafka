#Kafka [![Build Status](https://travis-ci.org/katzefudder/ansible-kafka.svg?branch=master)](https://travis-ci.org/katzefudder/ansible-kafka)
Installs [kafka](https://kafka.apache.org/)

##Requirements
- zookeeper_hosts - comma separated list of host:port pairs.
- kafka_hosts - list of dictionaries  comma separated list of host:port pairs in the cluster, defaults to 'ansible_fqdn:9092' for a single node
 - host - defaults to 'ansible_fqdn' for a single node
 - id - optional: defines the id of the broker (if you don't want to use the index of the list)
 - advertised_listeners - optional: defines a list of specific addresses for kafka to advertise to consumers/producers


##Optional
- kafka_listeners - defines a specific address for kafka to listen on, by defaults listens on all interfaces
- monasca_log_level - Log level to be used for Kafka logs. Defaults to WARN
- monasca_wait_for_period - The time in seconds for how long to wait for Kafka's port to be available after starting it. Default is 30 seconds.
- run_mode - One of Deploy, Stop, Install, Start, or Use. The default is Deploy which will do Install, Configure, then Start.

##License
Apache

##Author Information
Tim Kuhlman

Monasca Team email monasca@lists.launchpad.net

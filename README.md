ceph-zabbix
===========

Zabbix plugin for Ceph monitoring

Installation
===========

copy files :

ceph-status.sh -> /etc/zabbix/scripts/ceph-status.sh 

zabbix_agent_ceph_plugin.conf -> /etc/zabbix/zabbix_agentd.d/zabbix_agent_ceph_plugin.conf



Add the xml template and link them to your node.

Link the ceph templates to your hosts

Add item in your hosts ceph.get[$ActiveServerIP, $HOST], your can varify the item interval to change the frequncy of collect.


==============

agent send directly from the script to zabbix trough zabbix-trapper

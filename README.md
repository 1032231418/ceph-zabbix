ceph-zabbix-active
===========

Zabbix active plugin for Ceph monitoring

Installation
===========

1. excute install cmd:

sh install.sh 

2. import the xml templates.

3. Link the ceph templates to your hosts

4. Add item ceph.get[$ActiveServerIP, $HOST] in your hosts  your can varify the item interval to change the frequncy of collect.


==============

agent send directly from the script to zabbix trough zabbix-trapper

ceph-zabbix-active
===========

Zabbix active plugin for Ceph monitoring

Installation
===========

On Ceph Monitor Hosts:

1. excute install cmd:

   sh install.sh 

2. restart zabbix-agent

On Zabbix DashBoad:

1. import the xml templates.

2. Link the ceph templates to your ZabbixHost

3. Add item ceph.get[$ActiveServerIP, $HOST, 1] in your ZabbixHost


How to push many MON hosts ceph data to the ZabbixHost?

1. install ceph-zabbix-active on Ceph MON1, MON2, MON3

1. Add zabbix agent interface on ZabbixHost using MON1,MON2,MON IP/DNS

2. Add item ceph.get[$ActiveServerIP, $HOST, 1] using MON1 zabbix agent interface  on your ZabbixHost

3. Add item ceph.get[$ActiveServerIP, $HOST, 2] using MON2 zabbix agent interface  on your ZabbixHost

4. Add item ceph.get[$ActiveServerIP, $HOST, 3] using MON3 zabbix agent interface  on your ZabbixHost



==============

agent send directly from the script to zabbix trough zabbix-trapper

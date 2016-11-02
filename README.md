ceph-zabbix-active
===========

Zabbix active plugin for Ceph monitoring

Installation
===========

On Ceph Monitor Hosts:

1. excute install cmd:

   sudo sh install.sh 
   
2. edit ceph_cron.txt to varify serverActiveIP and ZabbixHost to push

3. sudo crontab ceph_cron.txt

On Zabbix DashBoad:

1. import the xml templates.

2. Link the ceph templates to your ZabbixHost



How to push many MON hosts ceph data to the ZabbixHost?

1. install ceph-zabbix-active on Ceph MON1, MON2, MON3





==============

agent send directly from the script to zabbix trough zabbix-trapper

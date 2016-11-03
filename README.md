===========
主要改进：

1. 采用 zabbix-agent(active) 模式，效率更高

2. 采集脚本多机部署，数据发送到同一HOST，避免单点风险

3. 增加支持 read/write iops item；

4. 增加iops超高和ceph err告警

===========


ceph-zabbix-active
===========

Zabbix active plugin for Ceph monitoring

Installation
===========

A. On one Ceph Monitor Host:

1.  git clone https://github.com/BodihTao/ceph-zabbix.git

2. cd ceph-zabbix

3. sudo cp ceph-status.sh /etc/zabbix/scripts/
   
4. edit ceph_cron.txt to set the serverActiveIP and ZabbixHost to push

5. sudo crontab ceph_cron.txt

On the other Monitor Hosts:
the same with A step.
then if one monitor host is down, the ceph-cluser zabbix monitor will work fine.


B. On Zabbix DashBoad:

1. import the xml templates.

2. Link the ceph templates to your ZabbixHost





==============

agent send directly from the script to zabbix trough zabbix-trapper

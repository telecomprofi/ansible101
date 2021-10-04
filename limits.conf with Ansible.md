LIMITS.CONF WITH ANSIBLE
September 13, 2017
[root@localhost ~]# ansible-galaxy init limits.conf
– limits.conf was created successfully

[root@localhost ~]# ansible-doc pam_limits

[root@localhost ~]# vim limits.conf/tasks/main.yml
—
# tasks file for limits.conf
– pam_limits:
domain: “{{ item.domain }}”
limit_type: “{{ item.limit_type }}”
limit_item: “{{ item.limit_item }}”
value: “{{ item.value }}”
with_items: “{{ limits_conf_settings }}”

[root@localhost ~]# vim limits_conf.yml
—
– hosts: all
roles:
– limits.conf
vars:
limits_conf_settings:
– domain: joe
limit_type: soft
limit_item: nofile
value: 64000

[root@localhost ~]# ansible-playbook limits_conf.yml -C

PLAY [all] *************************************************************************************************************************************

TASK [Gathering Facts] *************************************************************************************************************************
ok: [localhost]

TASK [limits.conf : pam_limits] ****************************************************************************************************************
skipping: [localhost] => (item={u’domain’: u’joe’, u’limit_item’: u’nofile’, u’limit_type’: u’soft’, u’value’: 64000})

PLAY RECAP *************************************************************************************************************************************
localhost : ok=1 changed=0 unreachable=0 failed=0

Advertisements

REPORT THIS AD

[root@localhost ~]# ansible-playbook limits_conf.yml

PLAY [all] *************************************************************************************************************************************

TASK [Gathering Facts] *************************************************************************************************************************
ok: [localhost]

TASK [limits.conf : pam_limits] ****************************************************************************************************************
changed: [localhost] => (item={u’domain’: u’joe’, u’limit_item’: u’nofile’, u’limit_type’: u’soft’, u’value’: 64000})

PLAY RECAP *************************************************************************************************************************************
localhost : ok=2 changed=1 unreachable=0 failed=0

[root@localhost ~]# tail -n1 /etc/security/limits.conf
joe soft nofile 64000

[root@localhost ~]# su – joe
Last login: Wed Sep 13 09:05:21 IST 2017 on pts/0
[joe@localhost ~]$ ulimit -Sn
64000

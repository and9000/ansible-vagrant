mysql
=====

Role to install and manage MySQL server.


Role Variables
--------------

By default you don't need to define any variables, the role will use defaults/main.yml


defaults/main.yml

`mysql.pkg` (OPTIONAL - the package to install)

```
mysql:
  pkg: mysql-server-5.6
```

`mysql_my_cnf` (OPTIONAL)

  Relative or full path to the main my.cnf file that will be copied to remote.


`mysql_conf_d` (OPTIONAL)

  Relative or full path to additional configuration files that will be copied to remote's
  conf.d directory.


Example (Recommended to define in group_vars or host_vars):

```
host_vars/db01.example.org.yml
  mysql_my_cnf: host_files/db01.example.org/mysql/my.cnf
  mysql_conf_d: host_files/db01.example.org/mysql/conf.d


The actual configs:

host_files/db01.example.org/mysql
├── my.cnf
└── conf.d
    ├── replication.cnf
    └── config1.cnf
```

License
-------

MIT


Author Information
------------------

Tal Lannder

tal@pjili.org

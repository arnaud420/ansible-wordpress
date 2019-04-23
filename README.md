# ansible-wordpress

Discover ansible by deploying a WordPress site on multiple remote domains with a remote database connection.

# Installation

## Configuration

**remote user** : *./inventory.ini* 

```
remote_user = arnaud*
```

**Global config** : */group_vars/all.yml*

```
vhost_servername: servername

wp_mysql_db: dbname
wp_mysql_user: dbuser
wp_mysql_password: dbpassword
wp_mysql_host: host (private)

app_dir: /appdir
```

**Ip machines config** : 
-  */group_vars/app*
-  */group_vars/db/app.db.yml*

```
ansible_host: ipaddr
```

## Start-up

```
ansible-playbook bootstrap.yml
```

Once it's built go to the ip of your hosts
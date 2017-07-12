# Vagrant ansible centos7 php7

## How to set up
- `git clone https://github.com/keisukefunatsu/centos7_ansible.git`
- `cd centos7_ansible`
- `vagrant up`

## included packages
- centos7
- php70
- apache
- mariadb
- composer
- phpmyadmin


## synced_folder
Directories will be attached to /vagrant

## hosts
Add the following lines to your hosts file
```
192.168.100.100 app.dev
192.168.100.100 phpmyadmin.dev
```

- As for phpmyadmin, username and password are 'root'!

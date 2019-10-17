# foreman-katelleo-pulp

* You need to install vagrant and virtualbox
* Initialize your vagrant box with your preferred os.
   My example: `vagrant init centos/7`
* Start your vagrant box
   `vagrant up`
* Connect via ssh
   `vagrant ssh`
* Set hostname and add the ip to /etc/hosts
* Check ntp
* Start installing your software

```sh
yum -y localinstall https://fedorapeople.org/groups/katello/releases/yum/3.13/katello/el7/x86_64/katello-repos-latest.rpm
yum -y localinstall https://yum.theforeman.org/releases/1.23/el7/x86_64/foreman-release.rpm
yum -y localinstall https://yum.puppet.com/puppet6-release-el-7.noarch.rpm
yum -y localinstall https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
yum -y install foreman-release-scl
```

* Installation

```sh
yum -y update
yum -y install katello
foreman-installer --scenario katello --help' -> show all possible scenarios
```

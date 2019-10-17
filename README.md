# foreman-katelleo-pulp

1. You need to install vagrant and virtualbox
2. Initialize your vagrant box with your preferred os. 
   My example: 'vagrant init centos/7'
3. Start your vagrant box
   'vagrant up'
4. Connect via ssh
   'vagrant ssh'
5. Set hostname and add the ip to /etc/hosts
6. Check ntp
7. Start installing your software
   'yum -y localinstall https://fedorapeople.org/groups/katello/releases/yum/3.13/katello/el7/x86_64/katello-repos-latest.rpm'
   'yum -y localinstall https://yum.theforeman.org/releases/1.23/el7/x86_64/foreman-release.rpm'
   'yum -y localinstall https://yum.puppet.com/puppet6-release-el-7.noarch.rpm'
   'yum -y localinstall https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm'
   'yum -y install foreman-release-scl'
8. Installation
   'yum -y update'
   'yum -y install katello'
   'foreman-installer --scenario katello --help' -> show all possible scenarios




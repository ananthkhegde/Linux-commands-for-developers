# Linux-commands-for-developers
Linux commands for developers


install python3 and activate virtual environment
https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-local-programming-environment-on-centos-7

install latest cmake
https://geeksww.com/tutorials/operating_systems/linux/installation/downloading_compiling_and_installing_cmake_on_linux.php

build and install liboost python against python3.6
download libboost from boost.org
https://eb2.co/blog/2012/03/building-boost-python-for-python-3-2/

install python boost
sudo yum install boost-devel  


Please use sudo

utility functions
to delete bin
sudo rm -rf /usr/bin/adobe
 tar xzf boost_1_65_0.tar.gz


install boost python in /usr/include

sudo yum install -y python36u-devel.x86_64




dlib is present in /usr/lib64/python3.6/sitepackages


saved libboost in /usr/loib

yum install python-devel
yum install python-lxml

run pycharm in centos
https://www.lifewire.com/how-to-install-the-pycharm-python-ide-in-linux-4091033


installing postgresssql on centos7
https://www.linode.com/docs/databases/postgresql/how-to-install-postgresql-relational-databases-on-centos-7

start and stop postgres
service postgresql-9.6 start

run below command from test user
sudo -u postgres psql

installing tomcat8 on centos7
https://www.digitalocean.com/community/tutorials/how-to-install-apache-tomcat-8-on-centos-7 -- not required

https://www.vultr.com/docs/how-to-install-apache-tomcat-8-on-centos-7--not required

https://www.vultr.com/docs/how-to-install-apache-tomcat-8-on-centos-7

restart tomcat
sudo systemctl restart tomcat


psql connection in command line
 psql -U postgres -h localhost
create database mydb;
\l list all database
\c mydb;


open port on firewall
 sudo firewall-cmd --zone=public --permanent --add-port=8000/tcp

sudo firewall-cmd --reload

Force stop database connection 
SELECT pg_terminate_backend(pg_stat_activity.pid)
    FROM pg_stat_activity
    WHERE pg_stat_activity.datname = 'target_db'
      AND pid <> pg_backend_pid();

to run python django server
 python manage.py runserver 172.16.0.172:8000

to check tomcat logs top 500 logs
go to /opt/tomcat/logs/
tail -n 500 catalina.out

to check disk uses in file system
df -h / 


copy file from one machins to another
scp test@cstem.cstep.in:/home/test/ananth.txt .

remove failed downloads in maven
for linux
find ~/.m2  -name "*.lastUpdated" -exec grep -q "Could not transfer" {} \; -print -exec rm {} \;
for windows
cd %userprofile%\.m2\repository
for /r %i in (*.lastUpdated) do del %i


nginx
sudo yum install nginx

start nginx
sudo systemctl start nginx

check status of nginx
sudo systemctl status nginx



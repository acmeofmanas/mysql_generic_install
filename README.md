# INSTALL MYSQL GENERIC from tar ball

1. download mysql compress file 
2. groupadd mysql
3. useradd -r -g mysql -s /bin/false mysql
4. cd /usr/local
5. tar xvf /path/to/mysql-VERSION-OS.tar.xz
6. ln -s full-path-to-mysql-VERSION-OS mysql
7. cd mysql
8. mkdir mysql-files
9. chown mysql:mysql mysql-files
10. chmod 750 mysql-files
11. bin/mysqld --initialize --user=mysql
  Copy your root user and password from stdio.
12. bin/mysql_ssl_rsa_setup
    >  create log and run directory and give permission to mysql user example 
     "/var/log/mariadb" and "/var/run/mariadb"
13. bin/mysqld_safe --user=mysql &
# Next command is optional
shell> cp support-files/mysql.server /etc/init.d/mysql.server

# run example script

ln -s //var/lib/mysql/mysql.sock /tmp/mysql.sock

/usr/local/mysql/bin/mysql -u root -prioadmin

create user 'druid' identified by 'druid';
grant all on druid.* to 'druid';

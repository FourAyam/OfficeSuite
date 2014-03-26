OfficeSuite
===========
Installation Instruction.
Goto your hosting directory
Incase of apache it is located at /var/www/html
But you may have configure it elsewhere.
Check your hosting directory at /etc/httpd/conf/httpd.conf

1.Clone the Office Suite
>git clone https://github.com/FourAyam/OfficeSuite.git

2.Open your MySql database.
Create a database and import Officesuite.sql
located in Mysql Scripts folder.

3.Navigate to data\plugins\boot.conf\bootstrap.json
Change the following value for your environment
"DIBI_PRECONFIGURATION":{
      "mysql_username":"mysqluser",
      "mysql_password":"mysqlpassword",
      "mysql_host":"mysqlserver",
      "mysql_driver":"mysql",
      "mysql_database":"databasename",
      "group_switch_value":"mysql"

4.Finally change the directory permission of data folder.
chmod 777 -R /path/to/public_html/OfficeSuite/data

5.Now start your apache and mysql
>service httpd start
>service mysqld start

6.Goto http://localhost/OfficeSuite/

Default passwords
For root is asdf@1234
For manager is asdf@1234
For emp1 is asdf@1234
For emp2 is asdf@1234

Once logged in via root you can create/delete users and explore task management workspace.

Have fun. 

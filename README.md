# Initial-Server-Setup
Configurations on CentOS 7

อัปเดต CentOS 
```
yum check-update
yum upgrade
yum clean all
```
ติดตั้ง Apache
```
sudo yum install httpd
```
เปิด Service Apache
```
sudo systemctl enable httpd.service
sudo systemctl restart httpd.service
```
ตั้งค่า firewall
```
sudo firewall-cmd --add-service=http --permanent
sudo firewall-cmd --add-service=https --permanent
sudo systemctl restart firewalld
```
ติดตั้ง MariaDB package
```
sudo yum install mariadb-server
sudo systemctl start mariadb
sudo systemctl enable mariadb
```
ตั้งค่า MariaDB
```
sudo mysql_secure_installation
```
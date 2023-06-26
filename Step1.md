 # IMPLEMENT A CLIENT SERVER ARCHITECTURE USING MYSQL DATABASE MANAGEMENT SYSTEM (DBMS).
TASK – Implement a Client Server Architecture using MySQL Database Management System (DBMS). 
First, I'll create and configure two Linux-based virtual servers (EC2 instances in AWS).
```
Server A name - `mysql server`
Server B name - `mysql client`
```

2.On mysql server Linux Server I'll install MySQL Server software.
Interesting fact: MySQL is an open-source relational database management system. Its name is a combination of "My", the name of co-founder Michael Widenius’s daughter, and "SQL", the abbreviation for Structured Query Language.

3.On mysql client Linux Server I'll install MySQL Client software.

4.By default, both of my EC2 virtual servers are located in the same local virtual network, so they can communicate to each other using local IP addresses. I'll use mysql server's local IP address to connect from mysql client. MySQL server uses TCP port 3306 by default, so I will have to open it by creating a new entry in ‘Inbound rules’ in ‘mysql server’ Security Groups. For extra security, I'll not  allow all IP addresses to reach my ‘mysql server’ – I'll allow access only to the specific local IP address of my ‘mysql client’.

5.I might need to configure MySQL server to allow connections from remote hosts.
```
sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf
```
6.From mysql client Linux Server I'll connect remotely to mysql server Database Engine without using SSH. 
7.Now we can see that we have successfully connected to a remote MySQL server and can perform SQL queries:
```
Show databases;
```






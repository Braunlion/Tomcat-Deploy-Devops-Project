# Prerequisites

# VPC Settings

- VPC and Internet gateway Setup
- Subnets
- Natgateway
- Routetables
- Security
  -- Bastion Host SG
  -- SSH Port 22 from your ip

  -- Application Load Balancer SG
  -- HTTP 80 from 0.0.0.0/0
  -- HTTPS 443 from 0.0.0.0/0

  -- Websever SG
  -- SSH Port 22 from Bastion Host SG
  -- Customer  port 8080 add to Alb-SG   
  -- Backend SG
  -- MySQL 3306 from Websever SG --RDS MySQL
  -- Custom 11211 from Websever SG --Memcached
  -- Custom 5671 from Websever SG --RabbitMQ
  -- Edit and allow all traffic from itself to the server-sg

#

- JDK 17
- Maven 3.9.9
- MySQL 8

# Technologies

- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- Tomcat
- MySQL
- Memcached
- Rabbitmq
- ElasticSearch

# Database

Here,we used Mysql DB
sql dump file:

- /src/main/resources/db_backup.sql
- db_backup.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < db_backup.sql

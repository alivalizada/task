# AWS Architecture

This README is for describing content of this folder.

I have added AWS architecture diagram in three format: .drawio , .html , .jpg

Architecture consists of below elements:

* Route 53 for DNS
* Elastic Load Balancer for allocating incoming traffic among instances
* Frontend instances
* Backend instances
* Auto Scaling group for increasing/decreasing number of instances for HA
* Multi AZ helps us to spread instances to several Availability Zones
* Security group for RDS restricts traffic to RDS only from Backend instances
* Security group for Backend instances restricts traffic only from Frontend instances
* Security group for Frontend instances restricts traffic only from ELB
* Data is being saved/pulled from Backend instances to Amazon Relational Database Service
* Amazon RDS replica helps to have a backup for master, also make reads faster



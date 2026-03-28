# Ritual Roast Three Tier Web Application

Deployed a highly available 3-tier web application on Amazon Web Services using EC2, ALB and RDS with Multi-AZ support.

## Overview:
To design a secure, scalable and fault-tolerant 3-tier architecture on AWS for hosting a Ritual Roast Customer Contest web application (MVP). The application will use:
- Application Load Balancer (ALB) for routing traffic
- Amazon EC2 instances for compute 
- RDS for database tier

## Customer Flow Chart
- Customer (Web Browser)
	- Initiates access to the web via public internet
- Application Load Balancer
	- Receives all incoming traffic.
	- Distributes requests across a fleet of EC2 instances.
- EC2 instances (App + Web Tier Combined)
- Host both the Frontend (form and recipe table display) and the Backend (code to handle form submissions and DB queries)
	- Display a form to the user and render the table of submitted recipes. 
- Amazon RDS (MySQL, Multi-AZ)
	- Stores submitted recipe data.
	- Backend reads from this DB to populate the frontend dynamically.


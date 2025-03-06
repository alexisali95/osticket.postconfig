![68747470733a2f2f692e696d6775722e636f6d2f436c7a6a3758732e706e67](https://github.com/user-attachments/assets/5a14de90-e992-42f1-b7f2-5122927fbb97)

# osTicket - Post-Install Configuration 

In this tutorial, we will set up configuration settings and profiles for our small company in order to have a successful open-source help desk ticketing system.

## Environments and Technologies Used

* Microsoft Azure (Virtual Machines/Compute)
* Remote Desktop
* Internet Information Services (IIS)

## Operating Systems Used

* Windows 10 Pro (21H2)

## Post-Install Configuration Objectives

Before we can fully use our new ticketing system, we must add the required configuration settings through the admin panel.
We will customize departments, agents, teams, hot topics, e-mails, and system preferences. 
Be sure to remember all of the username and passwords we create during the installation process. 

## Configuration Objectives:

* Roles 
* Departments
* Teams
* System Preferences to allow ticket creation 
* Users (clients) 
* SLAs
* Help Topics

![1  opening page after admin log in](https://github.com/user-attachments/assets/f48a8e87-0749-4934-8856-792e4b3a6093)

This should be the first page you see after logging into the Admin Portal.

### Step 1. Configure Roles
![2  add new role (senior admin)](https://github.com/user-attachments/assets/af40f6c4-3e31-4538-bc3e-c05abfc017d6)
![3  click all for admin role](https://github.com/user-attachments/assets/fc8bc240-4e18-4d5a-99e2-4f083f6e0ab3)
![4  new role added](https://github.com/user-attachments/assets/1da9cf7f-4426-4def-a9ee-f94a78c03ebb)

Roles allow Agents to access particular departments. 
> Under the “Agents” tab > select “Roles” > Add New Role
> Definition > Name: “Senior Admin” > permissions > selects all boxes under Tickets, Tasks, and Knowlegebase

### Step 2. Configure Departments 
![5  system admin department created](https://github.com/user-attachments/assets/8eb8f8e1-d64d-4554-b00a-ca6f695a434a)

Departments allow the osTicket to route tickets in the Help Desk, each department consisting of many settings.
> Under Agents tab > select Department > create “System Administration” department > ok

### Step 3: Configure Teams
![6  level 2 team created](https://github.com/user-attachments/assets/13b52d10-49a0-48e0-bdd0-c1062db4daa4)

Teams allow members to create groups of Agents from different departments, giving you permission to assign tickets to separate teams based on the User's issue (Help Topic or Ticket Filter).
> Select “Teams” tab > Add New Team > Name: Level I Support > select members

> Add Level II Support department 

### Step 4: Configure Settings - Allow Anyone to Create Tickets
![7  allow any user to create a ticket](https://github.com/user-attachments/assets/704a02c2-4dd0-4c18-bf7c-1d43f936c47c)

This step allows you to enforce standard rules and regulations for each User when tickets are created at the Help Desk.
> Admin Panel > Settings > User Settings > check “Require registration and login to create tickets

### Step 5: Configure Agents
![8  create agents](https://github.com/user-attachments/assets/cc468787-923c-47ee-825c-ed8cd5eb9a78)

This step will allow Admins to assign Agents to be responsible for responding to and resolving tickets. To keep this running smoothly, each Agent has to be assigned to a primary department and given a primary role for handling tickets. If needed, their role can be extended to other departments by granting them access.
> Click Agents > add new Agents > set primary department and role > assign team

### Step 6: Configure Users (Clients)
![9  create users](https://github.com/user-attachments/assets/bfb44849-32cb-4545-910d-14d19e3d8f9e)
![9 1 make sure to register users](https://github.com/user-attachments/assets/208d5c0d-e69b-4022-9816-ec08a29ca0a5)

This section will allow us to create Users. When a ticket is submitted, the User is linked to their email address in the Help Desk’s directory. Users can be added or removed from the directory, but since they are tied to their email and tickets, deleting a User also requires deleting their associated tickets. 
> Agent Panel > Users > User Directory > Add New

Make sure to register Users for their passwords to log in.

### Step 7: Configure SLAs ( Service Level Agreements)
![10  create SLAs](https://github.com/user-attachments/assets/2abab413-8843-4a6a-b8cd-a5ddf4c9b28b)

SLA Plans define the time frame within the Help Desk that is expected to resolve a ticket. 
> Admin Panel > Manage > SLA > Add New SLA Plan > Name: SEV-A > Grace Period: 1 hour > Schedule 24/27 > Add Plan
> Add second plan > Name: SEV-B > Grace Period: 4 hours > Schedule 24/7 > Add Plan
> Add third plan > Name: SEV-C > Grace Period: 8 > Schedule: Mon - Friday 8am - 5pm > Add Plan

### Step 8: Configure Help Topics

![11  Add Help Topics](https://github.com/user-attachments/assets/0aed188c-b50e-4cf6-99b7-8c35be8f827b)
![12  hot topics list](https://github.com/user-attachments/assets/97c44b8e-f680-44b2-8cbb-852e7a0fe938)

Help Topics enhance the User’s Help Desk experience by ensuring tickets are properly categorized, assigned, and addressed promptly. 
> Add New Help Topic > Topic: Business Critical Outage > click New Ticket Options > Department: System Administrator > Status: Open > Priority: High > SLA Plan: SEV-A > Auto-assignTo: Michelle Obama > Add Topic 

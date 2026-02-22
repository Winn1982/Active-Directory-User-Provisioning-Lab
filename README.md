# Active-Directory-User-Provisioning-Lab

## Objective

To simulate an enterprise user onboarding process within a Windows Server 2022 Active Directory environment by creating a structured Organizational Unit (OU), provisioning a domain user, assigning role-based security group membership, and validating successful authentication on a domain-joined Windows 10 client machine.

## Lab Environment

- Windows Server 2022 (Domain Controller)
- Active Directory Domain Services (AD DS)
- Windows 10 (Domain-Joined VM)
- Oracle VirtualBox

## Scenario

- A new Sales Department employee requires:
- Placement in correct Organizational Unit
- Assignment to department security group
- Successful authentication to domain
- Validation of profile creation and access

## Steps Performed
1. Created Organizational Unit

- Created OU: Sales_Department
- Created the Sales_Department OU to prepare for department-based user and policy management.

  <p align="center"><img width="500" height="500" alt="Step 1-Created new OU Sales Department" src="https://github.com/user-attachments/assets/21562229-0b66-4f96-b745-ecb739b83413" />

 2. Created Department Security Group

- Group Name: Sales_Security_Group
- Group Scope: Global
- Group Type: Security

Purpose:
Implemented role-based access control model. 

<p align="center"><img width="437" height="377" alt="Step 2 Created New Group Sales Security Group Inside Sales OU" src="https://github.com/user-attachments/assets/ed3a57c2-c24e-4f30-b503-003650a65413" />


<p align="center"><img width="500" height="500" alt="Step 3 Sales Security Group created successfully" src="https://github.com/user-attachments/assets/a25e94db-9214-4a49-82b6-11f85235b56d" />

Step 3: Create New Domain User

Inside Sales_Department OU:Right-click → New → User

Filled in:
- First Name: John
- Last Name: Carter
- User Logon Name: jcarter
- For the jcarter's password it was set to something simple for lab purposes, but normally it would be a strong temporary password that the user would change on next logon. 

<p align="center"><img width="434" height="375" alt="image" src="https://github.com/user-attachments/assets/79188716-495c-4317-871b-bdc5b5cb4c5f"/>

<p align="center"><img width="432" height="373" alt="image" src="https://github.com/user-attachments/assets/c314b857-b4b9-4806-9172-b3587001c313" />

<p align="center"><img width="437" height="375" alt="image" src="https://github.com/user-attachments/assets/f213f26b-6982-4f6b-98da-9999627fff4d" />



  




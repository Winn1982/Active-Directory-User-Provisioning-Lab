<p align="center"><img width="306" height="180" alt="image" src="https://github.com/user-attachments/assets/c48f445a-fc13-4df8-a1f0-c5af0863f746" />


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

Step 5: Add User to Security Group
- Right-click user → Properties
- Click Member Of tab
- Click Add → Sales_Security_Group
- Click OK → Apply → Close

<p align="center"><img width="461" height="254" alt="image" src="https://github.com/user-attachments/assets/be673f1a-f58d-4813-a71f-4279524aca8e" />

<p align="center"><img width="409" height="537" alt="image" src="https://github.com/user-attachments/assets/eeea03e3-4a0f-49ef-b7fb-c6f0281bb102" />

Step 6: Test Domain Authentication on Windows 10 VM 
- On Windows 10 VM:
- Login Using Domain Credentials
- At login screen:
- Select Other User → Enter jcarter@mydomain.com and then their password. Received the message that the user's password must be changed before signing in.

<p align="center"><img width="500" height="500" alt="Step 9 User needs to change password before signing in" src="https://github.com/user-attachments/assets/2255921e-49c5-4cae-819d-ad43dc3a3c9a" />

<p align="center"><img width="463" height="191" alt="image" src="https://github.com/user-attachments/assets/f117a966-c3b5-4bb2-abe4-dd07a78baf8f" />

Summary and Outcome

This Active Directory user provisioning lab demonstrated foundational Identity and Access Management concepts within a Windows Server 2022 environment. A structured Organizational Unit was created to simulate enterprise directory organization, a security group was implemented to support role-based access control, and a domain user account was successfully provisioned and authenticated on a Windows 10 client VM.

The lab confirmed proper domain authentication, user profile creation, and security configuration practices commonly used in enterprise IT environments.








  

  




  




# Iam-joiner-mover-leaver-project

This project demonstrates a completed Identity and Access Management (IAM) workflow in my Active Directory home lab using the terrylab.local domain. I designed and tested a Joiner / Mover / Leaver (JML) process to simulate how a real company manages user provisioning, role changes, and secure offboarding.

# Environment
Domain: terrylab.local
Platform: Windows Server Active Directory
Project Type: Identity and Access Management
Focus Areas: User lifecycle management, role-based access control, access validation, secure deprovisioning

Organizational Units

# The following OUs were used in this project:

HR
Finance
Operations
Security
Engineers
IT
Disabled Users

# Security Groups

Department access was managed through security groups rather than assigning permissions directly to individual users.

Groups used:

HR_SG
Finance_SG
Operations_SG
Security_SG
Engineers_SG
IT_SG

# Shared Folders

Department resources were created as shared folders and permissioned through security groups.

Examples:

\\WIN-LP2H1C6RF94\HR
\\WIN-LP2H1C6RF94\Finance
\\WIN-LP2H1C6RF94\Operations
\\WIN-LP2H1C6RF94\Security
\\WIN-LP2H1C6RF94\Engineers
\\WIN-LP2H1C6RF94\IT

Each folder was configured using both:

Share permissions
NTFS permissions

This allowed access to be restricted by department and validated through testing.

# Project Objectives

Build a structured Active Directory IAM environment
Create department-based OUs and security groups
Simulate employee onboarding, transfers, and offboarding
Apply role-based access control through group permissions
Validate least-privilege access to shared folders
Demonstrate secure account deprovisioning

# Joiner Workflow
Scenario

A new employee was onboarded and assigned access based on department role.

Tasks Completed
Created a new Active Directory user account
Placed the user into the correct departmental OU
Set a temporary password
Added the user to the correct department security group
Validated successful access to the authorized department folder
Confirmed the user could not access unauthorized folders
Result

The joiner account was successfully provisioned with the correct department access and denied access to unauthorized resources.

[!Joiner Access for Sarah Mitchell](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/f65270902f33058928a263ea571b759223c6803b/iam-joiner-operations-folder-access.png)

[!](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/f65270902f33058928a263ea571b759223c6803b/iam-joiner-operations-folder-access.png)

[Joiner Access for Sarah Mitchell](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/f65270902f33058928a263ea571b759223c6803b/iam-joiner-operations-folder-access.png)

[Joiner Access for Sarah Mitchell](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/f65270902f33058928a263ea571b759223c6803b/iam-joiner-operations-folder-access.png)

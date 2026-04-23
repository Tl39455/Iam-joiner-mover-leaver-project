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

# Joiner Sarah Mitchell to the operations department

Sarah Mitchell Account
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/e67e8cf35b4c269f3bae9eab5af893f7cab4b5a3/iam-joiner-operations-smitchell-account.png)

Members Department Folder
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/9bf57075d2c588d381089306126262dbb053616b/iam-joiner-operations-members.png)

Checking Access
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/f65270902f33058928a263ea571b759223c6803b/iam-joiner-operations-folder-access.png)

Confirm Access
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/fd0568e42192c18e4033c32d78d82cc286c6b9e3/iam-joiner-operations-access-confirm.png)

Checking Other Department Access
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/fdfdffc22fadc2ab78786a1ef1b06a1f35c7fbec/iam-joiner-operations-folder-access-engineers.png)

Denied Confirmed
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/5d6efc99d21292aea8cde24868538af28777bebb/iam-joiner-engineers-access-denied.png)


# Mover Jimmy Carter from the Security department to the Engineers department

Jimmy Carter Account
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/03df610698591f88da03044bd0a0cf66091a36b4/iam-mover-jimmycarter-account.png)

Move From Operations Department
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/e398dbd08dbc1118cc428fc3f5cd9b61c0055f9f/iam-mover-from-operations-folder.png)

Members Department Folder
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/5e390011c490eaecbf711f0115a8c86c06e87884/iam-mover-engineers.png)

Checking Access
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/ff3faef23bee207b15feb118fde7de49b8ad8f32/iam-mover-jcarter-engineers-folder-access.png)

Confirm Access
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/63c5dca6e4c947d3f7076175816cf859969b4d3b/iam-mover-jcarter-engineers-folder-access-granted.png)

Checking Other Department Access
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/adf53b83f0feb4bee235e5ebf99a4f2f00abf0b3/iam-mover-operations-folder-access.png)

Denied Confirmed
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/f364e5fb11489446db0bfbbd3a4383b7cb8c5497/iam-mover-operations-folder-access-denied.png)


# Leaver Kathy Brooks from the company account disabling

Kathy Brooks Account Disabled
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/e67e8cf35b4c269f3bae9eab5af893f7cab4b5a3/iam-joiner-operations-smitchell-account.png)

Kathy Brooks Removal From HR Department Folder
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/e67e8cf35b4c269f3bae9eab5af893f7cab4b5a3/iam-joiner-operations-smitchell-account.png)

Move to Disabled Users Folder
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/9bf57075d2c588d381089306126262dbb053616b/iam-joiner-operations-members.png)

Confirm Login Access Restricted
![](https://github.com/Tl39455/Iam-joiner-mover-leaver-project/blob/f65270902f33058928a263ea571b759223c6803b/iam-joiner-operations-folder-access.png)

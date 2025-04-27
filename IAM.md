# AWS IAM (Identity and Access Management)

## Root Account
- Created by default (do not use daily)

## IAM Users
- Represent individual people
- Can belong to multiple Groups
- Can have individual Policies

## IAM Groups
- Contain only Users
- No nesting (Group inside Group not allowed)
- Assigned Policies (permissions)

## IAM Policies
- JSON documents
- Define Permissions (Allow / Deny)
- Key Components:
  - Version
  - Statement(s):
    - Effect
    - Action
    - Resource
    - (Optional) Condition
- Inline vs Managed Policies

## IAM Roles
- Assign permissions to AWS services
- Examples:
  - EC2 Instance Role
  - Lambda Function Role
  - CloudFormation Role
- Temporary security credentials

## Authentication Methods
- AWS Management Console (Username + Password + MFA)
- AWS CLI (Access Key ID + Secret Access Key)
- AWS SDK (Access Key ID + Secret Access Key)

## MFA (Multi-Factor Authentication)
- Virtual MFA (Google Authenticator, Authy)
- Hardware MFA (Key fob, U2F device like YubiKey)
- Strongly recommended for Root and IAM Users

## Password Policy
- Enforce strong passwords
- Set expiration and complexity rules
- Prevent password reuse

## Access Keys
- Programmatic Access (CLI / SDK)
- Access Key ID = Username
- Secret Access Key = Password
- **Never share Access Keys!**

## IAM Security Tools
- IAM Credentials Report (account-wide)
- IAM Access Advisor (user-specific)

## Best Practices
- Don't use Root Account except for setup
- Enable MFA for all users
- Apply least privilege principle
- Rotate Access Keys regularly
- Use Roles for service permissions
- Audit with Credential Reports and Access Advisor

## Shared Responsibility Model![IAM](https://github.com/user-attachments/assets/e583af0c-78ec-46b8-b5f9-3ee32ea4225d)

### AWS manages:
- Global infrastructure security
- Physical data centers

### Customer manages:
- Users, Groups, Roles, Policies
- MFA and Key rotation
- Permissions monitoring
- Data access



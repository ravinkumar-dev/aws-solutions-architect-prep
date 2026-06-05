IAM (Identity and Access Management)
====================================

Imagine you have a big house (your AWS account) with many rooms (services and resources). You want to control who can enter which room and what they can do inside. IAM helps you do just that!

---

## What is IAM?

IAM is a tool from AWS that helps you manage who can access your AWS resources and what they can do. It uses:
- **Users**: People who need access (like you or your teammates)
- **Groups**: Collections of users with similar permissions
- **Roles**: Special access passes that can be used by people, apps, or AWS services
- **Policies**: Rules that say what actions are allowed or not allowed

---

## What is an IAM Role?

Think of an IAM Role as a guest pass. It isn’t tied to one person. Instead, anyone (or anything) you trust can use it for a while to do specific tasks.

**Example:**
- You want an EC2 server to read files from an S3 bucket. Instead of giving the server your own keys, you give it a role with just the permissions it needs.

### Why use Roles?
- Safer than sharing passwords or keys
- You can control exactly what the role can do
- Roles can be used by AWS services, apps, or even users from other accounts



**In short:** IAM helps you decide who can do what in your AWS account. Roles are like guest passes with specific powers, making your cloud safer and easier to manage!

--------------------------------------------------------------------------------

🔍 Inline Policies
Attached directly to a single IAM identity (user, group, or role).

Not reusable — if you want the same permissions for multiple identities, you must duplicate them.

Best for unique, one-off permissions that apply only to a specific identity.

Example: A temporary inline policy granting a single user access to a test S3 bucket.

🔍 Customer Managed Policies
Created and controlled by you in your AWS account.

Reusable — can be attached to multiple users, groups, or roles.

Versioning supported — IAM stores up to 5 versions, allowing rollback if needed.

Best for custom, organization-specific permissions.

Example: A policy granting developers read/write access to a specific DynamoDB table.

🔍 AWS Managed Policies
Prebuilt by AWS for common scenarios (e.g., AmazonS3ReadOnlyAccess, AdministratorAccess).

Cannot be modified — AWS updates them automatically when new services or APIs are added.

Best for quick setup and standard use cases.

Example: Attaching ReadOnlyAccess to auditors who need visibility across all AWS services.

------------------------

AWS organizations 
---------------------

AWS Organizations is a multi-account governance framework where accounts are grouped into OUs and governed using SCPs attached at the Root, OU, or Account level.

---

## Project Title

*Example: IAM User & Group Management Lab*

---

### Objective
Briefly state what the project achieves and why it matters.

*Example: Securely manage AWS users and groups with least privilege.*

---

### Architecture Diagram
Include a simple diagram (e.g., architecture.png) showing the main components and their relationships.

---

### Steps Performed
List the main steps you took, in order.

*Example:*
1. Created Admin, Developer, and ReadOnly groups
   
  **AWS CLI Commands:**
  ```sh
  aws iam create-group --group-name Admin
  aws iam create-group --group-name Developer
  aws iam create-group --group-name ReadOnly
  ```
2. Added users to groups


3. Attached policies
4. Tested permissions

---

### Concepts Covered
- IAM Users
- IAM Groups
- Policies
- Least privilege

---

*Example:*
- Avoid hardcoded credentials
- Prefer IAM roles over access keys
- Follow least privilege principle

---

sample JSON policies, CLI commands, or Lemon language snippets.

*Example:*
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": ["s3:GetObject", "s3:ListBucket"],
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}
```

---

### Screenshots
Add screenshots of the AWS Console, CLI output, or policy simulator results.


## Best Projects for Immediate Impact

| Priority | Project                       |
|----------|-------------------------------|
| 1        | EC2 → S3 IAM Role             |    --- completed
| 2        | IAM User & Group Management   |    --- completed
| 3        | S3 Restricted Access          |    --- completed
| 4        | MFA Implementation            |    --- completed
| 5        | Lambda Execution Role         |

---

iam-best-practices.md
------------------------------

- Least privilege
- MFA
- Role-based access
- Access key rotation


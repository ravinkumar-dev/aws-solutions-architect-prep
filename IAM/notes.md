---

### Creating IAM Groups with Boto3 (Python)

You can also automate the creation of IAM groups using Boto3, the AWS SDK for Python. Here’s a simple script:

```python
import boto3

iam = boto3.client('iam')

groups = ['Admin', 'Developer', 'ReadOnly']
for group in groups:
  response = iam.create_group(GroupName=group)
  print(f"Created group: {group}")
```

**How to Document:**
1. Run the script above in your Python environment.
2. Take a screenshot of the IAM groups in the AWS Console after creation.
3. Save the screenshot in the `screenshots/` folder of your project.
4. Reference the screenshot in your GitHub documentation for visual proof.
# AWS IAM Project Documentation
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

### Security Learnings
Summarize what you learned about security and best practices.

*Example:*
- Avoid hardcoded credentials
- Prefer IAM roles over access keys
- Follow least privilege principle

---

### Example Policies/Code
Show sample JSON policies, CLI commands, or Lemon language snippets.

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

---

### Bonus/Advanced
Mention any extra features, such as custom policies or troubleshooting steps.

---

## Best Projects for Immediate Impact

| Priority | Project                       |
|----------|-------------------------------|
| 1        | EC2 → S3 IAM Role             |    --- completed
| 2        | IAM User & Group Management   |    --- completed
| 3        | S3 Restricted Access          |    --- completed
| 4        | MFA Implementation            |    --- completed
| 5        | Lambda Execution Role         |

---

## How to Make Projects Look Professional

For EACH project include:
1. Objective
2. Architecture Diagram
3. Steps Performed
4. Security Learnings

Extra Powerful Addition: Create `iam-best-practices.md` with:
- Least privilege
- MFA
- Role-based access
- Access key rotation


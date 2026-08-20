# IAM Working Overview

## AIM

To understand and implement **Identity and Access Management (IAM)** concepts for securely managing identities, permissions, roles, and access to cloud resources.

## Introduction

Identity and Access Management (IAM) is a framework of policies, technologies, and practices used to manage digital identities and control access to resources. IAM ensures that the **right users have the right level of access to the right resources at the right time**.

IAM is an important part of cloud and enterprise security because it helps protect sensitive data and resources from unauthorized access.

## Objectives

* To understand the purpose and benefits of IAM.
* To learn about the core components of IAM.
* To gain hands-on experience in setting up and managing IAM policies.
* To understand authentication and authorization.
* To explore IAM security best practices.
* To learn how IAM activity can be monitored and audited.

## Prerequisites

Before working with IAM, a basic understanding of the following is recommended:

* Cloud services such as AWS, Azure, or Google Cloud.
* Basic networking and security concepts.
* Basic programming knowledge such as Python or Bash.
* Basic understanding of Git and version control.
* Familiarity with command-line tools.

## Core Components of IAM

IAM consists of several important components that work together to provide secure access management.

### 1. Identities

Identities represent users, applications, services, or other entities that need access to cloud resources.

Examples include:

* Users
* Applications
* Services
* External partners

### 2. Policies

Policies define what actions an identity is allowed or denied to perform on specific resources.

For example, a policy can allow a user to read objects from an Amazon S3 bucket without allowing them to delete those objects.

### 3. Roles

Roles provide permissions that can be temporarily assumed by users, applications, or services. Roles are useful when different resources need controlled access without permanently assigning credentials.

### 4. Authentication

Authentication is the process of verifying the identity of a user or service.

Examples include:

* Username and password
* Access keys
* Security tokens
* Multi-Factor Authentication (MFA)

### 5. Authorization

Authorization determines what an authenticated identity is allowed to access or modify. Authorization is generally controlled through IAM policies and permissions.

## IAM Best Practices

1. **Follow the Principle of Least Privilege**
   Give users and services only the permissions they actually need.

2. **Enable Multi-Factor Authentication (MFA)**
   Use an additional authentication factor to provide stronger account security.

3. **Use Role-Based Access Control (RBAC)**
   Assign permissions based on user roles instead of individually managing permissions whenever possible.

4. **Regularly Audit Access**
   Review permissions and access logs regularly to identify unnecessary or suspicious access.

5. **Manage Access Keys Carefully**
   Avoid unnecessary long-term credentials and rotate access keys when required.

6. **Monitor IAM Activity**
   Use logging and monitoring services to track changes and access attempts.

## Setup Guide

### 1. Configure IAM Roles and Policies

**Step 1:** Create an IAM role with the required permissions.

**Step 2:** Attach an appropriate IAM policy to the role.

**Step 3:** Ensure that the permissions follow the principle of least privilege.

**Step 4:** Test the role by assuming it and performing permitted actions.

### 2. Enable Multi-Factor Authentication (MFA)

**Step 1:** Open the IAM console.

**Step 2:** Select the required user account.

**Step 3:** Open **Security Credentials**.

**Step 4:** Configure and enable MFA for the account.

### 3. Set Up Identity Federation

Identity federation allows users to access cloud resources using an external identity provider.

**Step 1:** Configure an identity provider such as SAML or OpenID Connect.

**Step 2:** Establish trust between the identity provider and the cloud environment.

**Step 3:** Map users or groups to appropriate IAM roles.

**Step 4:** Test federated access.

### 4. Monitor and Audit Using CloudTrail

**Step 1:** Enable AWS CloudTrail to record account and IAM activity.

**Step 2:** Review recorded events and access attempts.

**Step 3:** Monitor changes to users, roles, and policies.

**Step 4:** Investigate suspicious or unauthorized activities.

## Examples

### Create an IAM User

```bash
aws iam create-user --user-name NewUser
```

### Attach a Policy to a User

```bash
aws iam attach-user-policy \
  --user-name NewUser \
  --policy-arn arn:aws:iam::aws:policy/ReadOnlyAccess
```

### Create an Access Key

```bash
aws iam create-access-key --user-name NewUser
```

> **Note:** Access keys should be handled securely and should not be uploaded to public repositories.

## Limitations

Although IAM provides strong access control, it has some limitations:

* Complex IAM policies can result in unintended permissions.
* Incorrect configurations may expose sensitive resources.
* Permissions require continuous review and maintenance.
* Managing a large number of users, roles, and policies can become complex.
* Proper knowledge of IAM policies is required to avoid security misconfigurations.

## Output

The implementation demonstrates the configuration and management of IAM components such as:

* IAM users
* IAM roles
* IAM policies
* MFA
* Identity federation
* Access monitoring and auditing

Screenshots of the IAM configuration and implementation steps are included in this repository as evidence of the practical work.

<img width="1916" height="988" alt="Screenshot 2026-08-16 205221" src="https://github.com/user-attachments/assets/db0a4c4a-996a-430e-88b0-13d07e1a399c" />

<img width="1919" height="955" alt="Screenshot 2026-08-16 205440" src="https://github.com/user-attachments/assets/10870a16-ff6c-4ef5-98d8-c06922e70091" />

<img width="1919" height="975" alt="Screenshot 2026-08-16 205615" src="https://github.com/user-attachments/assets/960c625c-a3b5-47a3-baf6-68e4e05213fa" />


<img width="1915" height="949" alt="Screenshot 2026-08-17 195304" src="https://github.com/user-attachments/assets/7db76b64-d04f-4549-b76d-d4fa872f09bb" />



<img width="1919" height="960" alt="Screenshot 2026-08-17 205041" src="https://github.com/user-attachments/assets/6fa479bd-0130-456d-8ba9-290834d141c8" />



<img width="1918" height="997" alt="Screenshot 2026-08-18 091828" src="https://github.com/user-attachments/assets/32f57b74-4ba8-4f61-a8e5-828ecb3c6581" />



<img width="1919" height="1092" alt="Screenshot 2026-08-18 094617" src="https://github.com/user-attachments/assets/79d3d63e-2c8f-484a-9d1c-0cfc03ef4f0a" />


## Conclusion

IAM is a fundamental part of cloud security. It helps organizations control who can access their resources and what actions they are allowed to perform.

By implementing **least-privilege access, MFA, role-based access control, regular auditing, and activity monitoring**, organizations can reduce security risks and protect their cloud resources from unauthorized access.

---

## Technologies Used

* **Amazon Web Services (AWS)**
* **AWS IAM**
* **AWS CloudTrail**
* **AWS CLI**
* **Git & GitHub**

## Author

**IAM Working Overview Project**

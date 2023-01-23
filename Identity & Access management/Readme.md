## Authentication vs. Authorization

- `Identity` and `access management` are key parts of an information security program and ensure that only `authorized` and `authenticated` users are able to access your resources and that they do so only in a manner that you intend.
- By using `identity` and `access management`, you define who has access to which resources and outline what can be done to those resources.

### Authentication

- Authentication is the process of `validating` that users are who they claim to be. 
- The most common method of authentication is using passwords as credentials.

### Authorization 

- Authorization is the process of giving the user permission to access a specific resource or function. 
- Giving someone permission to download a file and providing users with administrative access are some examples of authorization. 
- Sometimes in Authorization, the most important question is not what can users do, but what can they NOT do.

### Identity and access management approaches

You can consider a number of different approaches when addressing identity and access management. Two of the most important to consider are `protecting AWS credential`s and `establishing fine-grained authorization`.

1. Protecting credentials
 - It is important that you carefully manage the access credentials for your AWS resources. 
 - Every interaction with AWS is authenticated, so it is a foundation of security to establish appropriate credential management practices so that only authenticated users can take action in your account. 

2. Fine-grained authorization
 - You should establish a principle of least privilege to ensure that only authenticated users are permitted to perform only the most minimal functions to complete a specific task. 
 - This principle limits the potential impact of inappropriate use of the resources. 

### AWS services for identity and access management

There are numerous AWS services to protect credentials and allow for user authentication and authorization. Some of them are as follows: 

1. `Amazon Cognito` is a service for simple and secure user sign-up, sign-in, and access control to your web and mobile apps.
2. `AWS Directory Service` is a managed service offering that provides directories that contain information about your organization, including users, groups, computers, and other resources. As a managed offering, AWS Directory Service is designed to reduce management tasks, thereby allowing you to focus more of your time and resources on your business.
3. `AWS Identity and Access Management (IAM)` is a service that enables you to securely manage access to AWS services and resources in your account. You can create users and groups and apply permissions to allow or deny access to AWS resources.
4. `AWS IAM Identity Center (or AWS Single Sign-On)` is a cloud SSO service that allows for the central management of SSO access to multiple AWS accounts and business applications. It enables users to sign in to a user portal with their existing corporate credentials and access all of their assigned accounts and applications from one place. IAM Identity Center includes built-in Security Assertion Markup Language (SAML) integrations to many business applications. IAM Identity Center may be integrated with Microsoft Active Directory, which means your employees can sign in to your user portal using their corporate Active Directory credentials. 

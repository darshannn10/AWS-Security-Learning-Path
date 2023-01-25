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

1. Protecting Credentials
 - It is important that you carefully manage the access credentials for your AWS resources. 
 - Every interaction with AWS is authenticated, so it is a foundation of security to establish appropriate credential management practices so that only authenticated users can take action in your account. 

2. Fine-grained Authorization
 - You should establish a principle of least privilege to ensure that only authenticated users are permitted to perform only the most minimal functions to complete a specific task. 
 - This principle limits the potential impact of inappropriate use of the resources. 

### AWS services for identity and access management

There are numerous AWS services to protect credentials and allow for user authentication and authorization. Some of them are as follows: 

1. `Amazon Cognito` is a service for simple and secure user sign-up, sign-in, and access control to your web and mobile apps.
2. `AWS Directory Service` is a managed service offering that provides directories that contain information about your organization, including users, groups, computers, and other resources. As a managed offering, AWS Directory Service is designed to reduce management tasks, thereby allowing you to focus more of your time and resources on your business.
3. `AWS Identity and Access Management (IAM)` is a service that enables you to securely manage access to AWS services and resources in your account. You can create users and groups and apply permissions to allow or deny access to AWS resources.
4. `AWS IAM Identity Center (or AWS Single Sign-On)` is a cloud SSO service that allows for the central management of SSO access to multiple AWS accounts and business applications. It enables users to sign in to a user portal with their existing corporate credentials and access all of their assigned accounts and applications from one place. IAM Identity Center includes built-in Security Assertion Markup Language (SAML) integrations to many business applications. IAM Identity Center may be integrated with Microsoft Active Directory, which means your employees can sign in to your user portal using their corporate Active Directory credentials. 
---

## AWS IAM for Access Management

AWS IAM enables you to securely control individual and group access to AWS resources. Using AWS IAM you can create and manage AWS user's and AWS group's persmissions for you user's services.

AWS services can be accessed using `AWS Management Console`, `AWS CLI` or `AWS SDKs` or through `APIs`

You can create individual IAM users within your AWS account that corresponds to the users in your account where each user can have it's own credentials for authenticating the AWS

`IAM groups` can also be created into your AWS account. As the number of users managing AWS environment increases, it's helpful to manage permissions for multiple IAM users using IAM groups which ensures that each member of the group will be provisioned with the same permission policy.


#### Service features and benefits

- __IAM__ lets you create roles, which allows you to define a set of permissions and then let authenticated users assume them. This feature increases your security posture by granting temporary access to the resources you define.
- __IAM__ provides the __granularity to control__ a user’s access to specific AWS services and resources using permissions.
- You can use __IAM__ to grant your employees and applications access to the `AWS Management Console` and to `AWS service APIs` using your existing identity systems. 
- Grant only least privilege to each IAM entity by starting with no access and gradually granting appropriate rights.
- Your security team and administrators can use `IAM Access Analyzer` to identify resources that can be accessed from outside an AWS account.
- IAM is integrated into most AWS services. This integration provides the ability to define access controls from one place in the `AWS Management Console` that will take effect throughout your AWS environment.

```
IAM Policies are JSON documents used to describe permission within AWS
```

The following image is an example for `IAM policy`

![iam-sample-policies](https://user-images.githubusercontent.com/87711310/214519592-10227e9a-9529-445c-8473-d878be751ead.png)

#### Use case: IAM groups and permissions

- An `IAM group` is a collection of users. Groups allow you to specify permissions for similar types of users. 
- For example, if you have a group named Developers, you can give that group the types of permissions that developers typically need.
- This feature can be considered a form of role-based access control.

Different IAM groups that can be created for a company using the Amazon Elastic Cloud (Amazon EC2) instances are: 
1. `AllUsers`: You can easily create a group called AllUsers to apply any account wide permissions to all users in the AWS account.
2. `System Administrators`: This group needs permission to create and manage AWS Machine Images (AMI), instances, snapshots, volume, security groups and so on.
3. `Developers`: Developers need the ability to work with instances only. You can create and attach a policy to the Developers group that allows developers to call only DescribeInstances, RunInstances, StopInstances, StartInstances, and TerminateInstances.
4. `Managers`: Managers should not be able to perform any Amazon EC2 actions except listing the Amazon EC2 resources currently available. Therefore, Managers should be assigned a policy that lets them call only Amazon EC2 __Describe__ API operations.


## Amazon Cognito for Mobile Authentication

Amazon Cognito lets you easily add user sign-up and authentication to your mobile and web apps. In addition, Amazon Cognito enables you to save data locally on user devices allowing your applications to work even when the devices are offline, so that the app experience remains consists regardless of the device that users use. Amazon Cognito also enables you to authenticate users through an external identity provider and provides temporary security credentials to access your app's backend resources in AWS or any service behind Amazon API Gateway.

User Identity is a unique identifier you associate with a particular end user. The three mechanisms that facilate are `Authentication`, `Authorization` and `User Management`

The two main components of Amazon Cognito are `user pools` and `identity pools`. `User pools` are user directories that provide sign-up and sign-in options for your app users. `Identity pools` enable you to grant your users access to other AWS services. You can use identity pools and user pools separately or together.

The following image shows user authentication in AWS Cognito with the help of Identity providers (IDPs)
![user-pool-saml-federation](https://user-images.githubusercontent.com/87711310/214571429-28828fff-af80-4a75-8e18-06031d84ce36.png)

#### Service features and benefits
- Amazon Cognito is a standards based identity provider and supports identity and access management standards, such as __Oauth 2.0__, __SAML 2.0__, and __OpenID Connect__. 
- With Amazon Cognito identity pools, your can create unique identities for your users so they can sign in through social identity providers such as __Google__, __Facebook__, and __Amazon__ and through enterprise identity providers such as __Microsoft Active Directory__ via __SAML__. 
- Amazon Cognito supports __MFA__ and encryption of data at rest and data in transit, meeting compliance requirements from several compliance organizations.
- With a built-in user interface (UI) and easy configuration for federating identity providers, you can integrate Amazon Cognito to add user sign-in, sign-up, and access control to your app.


## AWS Directory Service for User Federation

`Directory Service` provides multiple directory choices for customers who want to use existing `Microsoft Active Directory` or `Lightweight Directory Access Protocol (LDAP)`-aware applications in the cloud. You can choose directory services with the features and scalability that best meet your needs. 

There are few Directory Service solutions provided by AWS, they're: 
1. `AWS Managed Microsoft AD`: If you need an actual `Microsoft Active Directory` in the `AWS Cloud` that supports __Active Directory-aware workloads__, or that supports AWS applications and services such as Amazon WorkSpaces and Amazon QuickSight, then `AWS Directory Service for Microsoft Active Directory` would use to be very useful.
2. `Active Directory Connector`: If all you need is to allow you on-premises users to log in to AWS applications and services with their Active Directory credentials, you can use `AD connector`. You can also use AD Connector to join Amazon Elastic Compute Cloud (Amazon EC2) instances to your existing Active Directory domain.
3. if you need a low-scale, low-cost directory with basic Active Directory compatibility that supports `Samba 4` compatible applications or if you need `LDAP` compatibility for LDAP-aware applications, then you can use Simple AD. Simple AD provides a subset of the features that AWS Managed Microsoft AD offers, including the ability to manage user accounts and group memberships, create and apply group policies, securely connect to `mazon EC2` instances, and provide `Kerberos-based` single sign-on.

![aws-cloud](https://user-images.githubusercontent.com/87711310/214586310-7cf7933e-5564-4dff-ad72-a894d7f67043.png)

Useful Resources to look at: 
1. [Create a Simple Active Directory](https://docs.aws.amazon.com/directoryservice/latest/admin-guide/simple_ad_tutorial_create.html)
2. [Use Cases for AWS Managed Microsoft AD](https://docs.aws.amazon.com/directoryservice/latest/admin-guide/ms_ad_use_cases.html)

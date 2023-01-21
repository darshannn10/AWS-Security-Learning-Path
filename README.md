# AWS-Security-Learning-Path

## Security in the AWS Cloud

### `Confidentiality`, `Integrity`, and `Availability`
- Security is the practice of protecting your intellectual property from unauthorized access, use, or modification. 
- The `confidentiality`, `integrity`, and `availability` (CIA) triad model highlights the important aspects of information security within an organization.

- __`Confidentiality`__ refers to limiting information access and disclosure to authorized users (the right people) and preventing access by unauthorized people.

- __`Integrity`__ involves maintaining the consistency, accuracy, and trustworthiness of data over its entire life cycle.

- __`Availability`__ refers to the readiness of information resources. An information system that is not available when you need it is almost as useless as not having an information system. 


### AWS shared responsibility model

- AWS is responsible for protecting the global infrastructure that runs all of the services offered in the AWS Cloud. This infrastructure comprises the hardware, software, networking, and facilities that run AWS services.

- As an AWS customer, you are responsible for securing your data, operating systems, networks, platforms, and other resources that you create in the AWS Cloud. You are responsible for protecting the confidentiality, integrity, and availability of your data and for meeting any specific business or compliance requirements for your workloads.

![aws-shared-responsible-model](https://user-images.githubusercontent.com/87711310/213884585-233cf1d0-b369-47b5-894c-12b4c8133411.png)

### Security design principles
1. __Implement a strong identity foundation__: An organizational security culture should be built on the principles of least privilege and strong authentication. Grant access to data and other resources to only the people who really need that access. 
2. __Enable traceability__: With AWS, you can monitor, alert, and audit actions and changes to your environment in real time. AWS provides native logging and services to provide greater visibility in near-real time for occurrences in your environment.
3. __Apply security at all layers__: Rather than focusing on the protection of a single outer layer, apply a defense-in-depth approach with other security controls. This approach means applying security to all layers, such as your network, application, and data store.
4. __Automate security best practices__: AWS offers purpose-built security tools that automate many of the routine tasks security experts normally spend time on. Security engineering and operations functions can be automated using a comprehensive set of APIs and tools.
5. __Protect data in transit and at rest__: Safeguarding data is a critical part of building and operating information systems. AWS provides services and features that give you several options to protect your data at rest and in transit. These options include fine-grained access controls to objects, creating and controlling the encryption keys used to encrypt your data, selecting appropriate encryption methods, validating integrity, and appropriately retaining data. 
6. __Minimize your attack surface__: Generally, a cyber attack ends for one of two reasons: the attackers exhaust themselves and give up, or the attackers achieve their goal. Be ready to scale and absorb the attack and minimize or remove the possibility of an unprotected device. 
7. __Prepare for security events__: Even with mature preventive and detective controls, you should still put processes in place to respond to and mitigate the potential impact of security incidents. Put tools and access in place ahead of a security incident. Then, routinely practice incident response through game days. This helps you ensure that your architecture can accommodate timely investigation and recovery.

## The AWS Well-Architected Framework

- The `AWS Well-Architected Framework` helps you understand the pros and cons of decisions you make while building systems on AWS. 
- By using the `AWS Well-Architected Framework`, you will learn architectural best practices for designing and operating __reliable__, __secure__, __efficient__, and __cost-effective__ systems in the cloud. 
- It provides a way for you to consistently measure your architectures against best practices and identify areas for improvement. 
- The framework is based on six pillars: 

1. __Operational Excellence__: The operational excellence pillar focuses on running and monitoring systems to deliver business value and continually improving processes and procedures. 
2. __Security__: The security pillar focuses on protecting information and systems. 
3. __Reliabilty__: The reliability pillar focuses on the ability to prevent and quickly recover from failures to meet business and customer demand.
4. __Performance Efficiency__: The performance efficiency pillar focuses on using IT and computing resources efficiently.
5. __Cost Optimization__: Cost optimization focuses on avoiding unneeded costs.
6. __Sustainability__: The sustainability pillar is based on recommendations and strategies to use when designing cloud architectures that maximize efficiency and reduce waste.

### The security pillar

- The security pillar signifies the ability to protect information, systems, and assets while delivering business value through risk assessments and mitigation strategies. 
- The security pillar is made up of five different areas for security in the cloud.
1. __Identity and Access Management__: Identity and access management are key parts of a security program. They ensure that only authorized and authenticated users are able to access your resources and that these users do so only in a manner that you intend.
2. __Detective Controls__: You can use detective controls to identify a potential security threat or incident. Device controls are an essential part of governance frameworks and can be used to support threat identification and response efforts. 
3. __Infrastructure Protection__: Infrastructure protection ensures that systems and services within your workload are protected against unintended and unauthorized access and potential vulnerabilities.
4. __Data Protection__: Data protection means protecting data at rest and in transit via encryption methods and access control and also classifying data based on levels of sensitivity.
5. __Incident Response__: Even with extremely mature preventive and detective controls, your organization should still put processes in place to respond to and mitigate the potential impact of security incidents.

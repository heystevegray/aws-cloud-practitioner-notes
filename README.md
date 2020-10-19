# Overview

- [Overview](#overview)
- [AWS Documentation](#aws-documentation)
- [Compute](#compute)
  - [Amazon EC2](#amazon-ec2)
    - [EC2 data](#ec2-data)
      - [Metadata](#metadata)
      - [User data](#user-data)
  - [Amazon Lightsail](#amazon-lightsail)
    - [Resources](#resources)
- [Database](#database)
  - [Amazon Aurora](#amazon-aurora)
  - [DynamoDB](#dynamodb)
- [Storage](#storage)
  - [Amazon S3 Glacier](#amazon-s3-glacier)
  - [AWS Snow Family](#aws-snow-family)
    - [AWS Snowmobile](#aws-snowmobile)
    - [AWS Snowball](#aws-snowball)
      - [Resources](#resources-1)
    - [AWS Snowcone](#aws-snowcone)
      - [Resources](#resources-2)
- [Billing & Cost Management](#billing--cost-management)
  - [AWS Cost and Usage Reports](#aws-cost-and-usage-reports)
  - [AWS Billing and Cost Management](#aws-billing-and-cost-management)
    - [Forecasting with Cost Explorer](#forecasting-with-cost-explorer)
    - [Cost Explorer](#cost-explorer)
  - [AWS Support Plans](#aws-support-plans)
  - [Amazon EC2 Pricing Plans](#amazon-ec2-pricing-plans)
    - [On-Demand](#on-demand)
    - [Spot instances](#spot-instances)
    - [Reserved instances](#reserved-instances)
    - [Dedicated Hosts](#dedicated-hosts)
- [Security, Identity, & Compliance](#security-identity--compliance)
  - [AWS Identity & Access Management (IAM)](#aws-identity--access-management-iam)
    - [Authentication](#authentication)
      - [User](#user)
      - [Group](#group)
      - [Role](#role)
    - [Authorization](#authorization)
      - [Policy Document](#policy-document)
  - [Amazon Cognito](#amazon-cognito)
    - [Web-identity federation](#web-identity-federation)
      - [Resources](#resources-3)
  - [AWS Artifact](#aws-artifact)
  - [AWS Directory Service](#aws-directory-service)
  - [AWS Security Hub](#aws-security-hub)
  - [Amazon Inspector](#amazon-inspector)
    - [Resource](#resource)
  - [Amazon GuardDuty (S3 Duty)](#amazon-guardduty-s3-duty)
  - [Amazon Macie](#amazon-macie)
- [Machine Learning](#machine-learning)
  - [Amazon CodeGuru](#amazon-codeguru)
- [Networking & Content Delivery](#networking--content-delivery)
  - [ELB](#elb)
  - [Amazon VPC](#amazon-vpc)
    - [VPC Peering](#vpc-peering)
      - [Resources](#resources-4)
  - [Amazon Route 53](#amazon-route-53)
    - [Resources](#resources-5)
    - [Reflecting changes globally](#reflecting-changes-globally)
- [Management & Governance](#management--governance)
  - [AWS Trusted Advisor](#aws-trusted-advisor)
  - [AWS Trusted Advisor best practice recommendations](#aws-trusted-advisor-best-practice-recommendations)
    - [Cost optimization](#cost-optimization)
    - [Performance](#performance)
    - [Security](#security)
    - [Fault Tolerance](#fault-tolerance)
    - [Service limits](#service-limits)
  - [Amazon CloudWatch](#amazon-cloudwatch)
  - [AWS Systems Manager](#aws-systems-manager)
  - [AWS Service Catalog](#aws-service-catalog)
    - [Resources](#resources-6)
  - [AWS CloudFormation](#aws-cloudformation)
  - [AWS Control Tower](#aws-control-tower)
  - [AWS Organizations](#aws-organizations)
    - [Managing organizational units (OUs)](#managing-organizational-units-ous)
- [Developer Tools](#developer-tools)
  - [AWS CodePipeline](#aws-codepipeline)
  - [AWS CodeStar](#aws-codestar)
  - [AWS CodeBuild](#aws-codebuild)
  - [AWS Cloud9](#aws-cloud9)
- [Cryptography & PKI](#cryptography--pki)
  - [AWS CloudHSM](#aws-cloudhsm)
  - [AWS Certificate Manager (ACM)](#aws-certificate-manager-acm)
  - [AWS Key Management Service (KMS)](#aws-key-management-service-kms)
- [Other](#other)
  - [AWS Personal Health Dashboard](#aws-personal-health-dashboard)
  - [Shared Responsibility Model](#shared-responsibility-model)
- [AWS Well-Architected Framework](#aws-well-architected-framework)
  - [AWS Well-Architected and the Five Pillars](#aws-well-architected-and-the-five-pillars)
    - [Operational Excellence Pillar](#operational-excellence-pillar)
    - [Security Pillar](#security-pillar)
    - [Reliability Pillar](#reliability-pillar)
    - [Performance Efficiency Pillar](#performance-efficiency-pillar)
    - [Cost Optimization Pillar](#cost-optimization-pillar)
- [Whizlabs Tricky questions](#whizlabs-tricky-questions)
- [Resources](#resources-7)
  - [AWS](#aws)
    - [Courses](#courses)
    - [Other](#other-1)
  - [Intellipaat](#intellipaat)
  - [Pluralsight](#pluralsight)
  - [Tutorials Dojo](#tutorials-dojo)
  - [Whizlabs](#whizlabs)
  - [Preparation](#preparation)

# AWS Documentation

- [All AWS Documentation](https://docs.aws.amazon.com/index.html?nc2=h_ql_doc_do_v)

# Compute

## Amazon EC2

Virtual servers in the cloud | [Source](https://aws.amazon.com/ec2/?nc2=type_a&ec2-whats-new.sort-by=item.additionalFields.postDateTime&ec2-whats-new.sort-order=desc)

Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud.

### EC2 data

#### Metadata

Instance metadata is data about your instance that you can use to configure or manage the running instance. Instance metadata is divided into categories, for example, host name, events, and security groups. | [Source](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html)

#### User data

> User data is information that is passed to in instance's operating system, this can be in the form of a bash script written in plaintext. | [Source - Whizlabs Free Practice Test for AWS Certified Cloud Practitioner](https://www.whizlabs.com/learn/course/aws-certified-cloud-practitioner-practice-tests/)

**Important**

> Although you can only access instance metadata and user data from within the instance itself, the data is not protected by authentication or cryptographic methods. Anyone who has direct access to the instance, and potentially any software running on the instance, can view its metadata. Therefore, you should not store sensitive data, such as passwords or long-lived encryption keys, as user data. | [Source](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html)

## Amazon Lightsail

Lightsail is an easy-to-use cloud platform that offers you everything needed to build an application or website, plus a cost-effective, monthly plan. | [Source](https://aws.amazon.com/lightsail/?nc2=type_a)

Lightsail is an easy-to-use cloud platform that offers you everything needed to build an application or website, plus a cost-effective, monthly plan.

### Resources

- [Amazon Lightsail features](https://aws.amazon.com/lightsail/features/)

# Database

## Amazon Aurora

High performance managed relational database | [Source](https://aws.amazon.com/rds/aurora/?nc2=type_a&aurora-whats-new.sort-by=item.additionalFields.postDateTime&aurora-whats-new.sort-order=desc)

A MySQL and PostgreSQL-compatible relational database built for the cloud, that combines the performance and availability of traditional enterprise databases with the simplicity and cost-effectiveness of open source databases.

Amazon Aurora is fully managed by [Amazon Relational Database Service (RDS)](https://aws.amazon.com/rds/), which automates time-consuming administration tasks like hardware provisioning, database setup, patching, and backups.

## DynamoDB

Fast and flexible NoSQL database service for any scale | [Source](https://aws.amazon.com/dynamodb/?nc2=type_a)

Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale.

# Storage

## Amazon S3 Glacier

Low-cost archive storage in the cloud | [Source](https://aws.amazon.com/glacier/?nc2=type_a)

Amazon S3 Glacier and S3 Glacier Deep Archive are a secure, durable, and extremely low-cost Amazon S3 cloud storage classes for data archiving and long-term backup. They are designed to deliver 99.999999999% durability, and provide comprehensive security and compliance capabilities that can help meet even the most stringent regulatory requirements.

## AWS Snow Family

> Highly-secure, portable devices to collect and process data at the edge, and migrate data into and out of AWS | [Source](https://aws.amazon.com/snow/)

[The AWS Snow Family members](https://aws.amazon.com/snow/#AWS_Snow_Family_members):

- AWS Snowmobile
- AWS Snowball
- AWS Snowcone

The AWS Snow Family is a service that helps customers who need to run operations in austere, non-data center environments, and in locations where there's no consistent network connectivity. | [Source](https://docs.aws.amazon.com/snowball/?id=docs_gateway)

### AWS Snowmobile

Migrate or transport exabyte-scale data sets into and out of AWS | [Source](https://aws.amazon.com/snowmobile/)

AWS Snowmobile is an Exabyte-scale data transfer service used to move extremely large amounts of data to AWS. You can transfer up to 100PB per Snowmobile, a 45-foot long ruggedized shipping container, pulled by a semi-trailer truck.

### AWS Snowball

Edge computing and petabyte-scale data transport | [Source](https://aws.amazon.com/snowball/?nc2=type_a)

AWS Snowball, a part of the [AWS Snow Family](https://aws.amazon.com/snow/), is an edge computing, data migration, and edge storage device that comes in two options. | [Source](https://aws.amazon.com/snowball/?nc2=type_a&whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc)

#### Resources

- [AWS Snowball User Guide](https://docs.aws.amazon.com/snowball/latest/ug/whatissnowball.html)

### AWS Snowcone

AWS Snowcone is the smallest member of the [AWS Snow Family](https://aws.amazon.com/snow/) of edge computing, edge storage, and data transfer devices, weighing in at 4.5 pounds (2.1 kg) with 8 terabytes of usable storage. | [Source](https://aws.amazon.com/snowcone/?nc2=type_a)

AWS Snowcone is a portable, rugged, and secure device for edge computing and data transfer. You can use Snowcone to collect, process, and move data to AWS, either offline by shipping the device to AWS, or online by using AWS DataSync. | [Source](https://docs.aws.amazon.com/snowball/latest/snowcone-guide/snowcone-what-is-snowcone.html)

#### Resources

- [AWS Snowcone User Guide](https://docs.aws.amazon.com/snowball/latest/snowcone-guide/snowcone-what-is-snowcone.html)

# Billing & Cost Management

## AWS Cost and Usage Reports

The AWS Cost and Usage Reports (AWS CUR) contains the most comprehensive set of cost and usage data available. | [Source](https://docs.aws.amazon.com/cur/latest/userguide/what-is-cur.html)

## AWS Billing and Cost Management

AWS Billing and Cost Management is the service that you use to pay your AWS bill, monitor your usage, and analyze and control your costs. | [Source](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/billing-what-is.html)

### Forecasting with Cost Explorer

You create a forecast by selecting a future time range for your report. | [Source](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/ce-forecast.html)

### Cost Explorer

Cost Explorer is a tool that enables you to view and analyze your costs and usage. | [Source](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/ce-what-is.html)

[AWS Cost Explorer now Supports Usage-Based Forecasts](https://aws.amazon.com/about-aws/whats-new/2019/07/usage-based-forecasting-in-aws-cost-explorer/)

## AWS Support Plans

[Compare AWS Support Plans](https://aws.amazon.com/premiumsupport/plans/)

Plans

- Basic
- Developer
- Business
- Enterprise

Basic Support is included for all AWS customers and includes:

- Customer Service and Communities - 24x7 access to customer service, [documentation](https://docs.aws.amazon.com/), [whitepapers](https://aws.amazon.com/whitepapers/?whitepapers-main.sort-by=item.additionalFields.sortDate&whitepapers-main.sort-order=desc), and [support forums](https://forums.aws.amazon.com/index.jspa).
- [AWS Trusted Advisor](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/) - Access to the 7 core Trusted Advisor checks and guidance to provision your resources following best practices to increase performance and improve security.
- [AWS Personal Health Dashboard](https://aws.amazon.com/premiumsupport/technology/personal-health-dashboard/) - A personalized view of the health of AWS services, and alerts when your resources are impacted.

## Amazon EC2 Pricing Plans

[Source](https://aws.amazon.com/ec2/pricing/)

### On-Demand

With On-Demand instances, you pay for compute capacity by the hour or the second depending on which instances you run. No longer-term commitments or upfront payments are needed. You can increase or decrease your compute capacity depending on the demands of your application and only pay the specified per hourly rates for the instance you use.

### Spot instances

Amazon EC2 Spot instances allow you to request spare Amazon EC2 computing capacity for up to 90% off the On-Demand price.

### Reserved instances

Reserved Instances provide you with a significant discount (up to 75%) compared to On-Demand instance pricing. In addition, when Reserved Instances are assigned to a specific Availability Zone, they provide a capacity reservation, giving you additional confidence in your ability to launch instances when you need them.

### Dedicated Hosts

A Dedicated Host is a physical EC2 server dedicated for your use. Dedicated Hosts can help you reduce costs by allowing you to use your existing server-bound software licenses, including Windows Server, SQL Server, and SUSE Linux Enterprise Server (subject to your license terms), and can also help you meet compliance requirements.

# Security, Identity, & Compliance

## AWS Identity & Access Management (IAM)

### Authentication

#### User

A **permanent** named operator. Could be human, could be machine. | [Source - AWS Cloud Practitioner Essentials (Second Edition)](https://www.aws.training/Details/Curriculum?id=27076)

#### Group

A collection of Users. | [Source - AWS Cloud Practitioner Essentials (Second Edition)](https://www.aws.training/Details/Curriculum?id=27076)

#### Role

Not permissions. It's an authentication method. An operator (human or machine) with **temporary** credentials. | [Source - AWS Cloud Practitioner Essentials (Second Edition)](https://www.aws.training/Details/Curriculum?id=27076)

> You can use roles to delegate access to users, applications, or services that don't normally have access to your AWS resources. | [Source](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html)

> Everything in AWS is an api. | Blain

This means that we have to authenticate and authorize.

### Authorization

#### Policy Document

> Lists the specific api, or wildcard group of api's, that I am allowing against which resources, are there conditions, certain times of day. | Blain

Can be attached to a User, Group, or Role. | [Source - AWS Cloud Practitioner Essentials (Second Edition)](https://www.aws.training/Details/Curriculum?id=27076)

**Example: An operator wants to put and Object into an S3 bucket.**

That is an API call. This is the flow of events:

1. The API call is made with credentials attached (username / password).
2. The call is presented to the IAM engine, is it looks at the credentials and makes sure they are active credentials for a User, Group, or Role.
3. Policy Documents for a User, Group, or Role are then checked to make sure the call is **authorized**.

The Security Manager can execute a single API statement that removes all the policy documents from all User, Groups, or Roles. A hacker trying to remove an asset, the api action is evaluated by the IAM engine. Since there are no Policy documents associated with the credentials, they are not **authorized** to execute the action. It's also logged on CloudTrail... every api action is recorded, successful or declined.

## Amazon Cognito

Identity management for your apps | [Source](https://aws.amazon.com/cognito/?nc2=type_a)

Amazon Cognito lets you add user sign-up, sign-in, and access control to your web and mobile apps quickly and easily. Amazon Cognito scales to millions of users and supports sign-in with social identity providers, such as Facebook, Google, and Amazon, and enterprise identity providers via SAML 2.0.

### Web-identity federation

Your app users can sign in either directly through a user pool, or federate through a third-party identity provider (IdP). | [Source](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pools-identity-federation.html)

#### Resources

- [Providing access to externally authenticated users (identity federation)](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_common-scenarios_federated-users.html)

## AWS Artifact

No cost, self-service portal for on-demand access to AWS’ compliance reports. | [Source](https://aws.amazon.com/artifact/?nc2=type_a)

AWS Artifact is your go-to, central resource for compliance-related information that matters to you.

## AWS Directory Service

Procides multiple ways to use Microsoft [Active Directory](https://en.wikipedia.org/wiki/Active_Directory) (AD) with other AWS services | [Source](https://docs.aws.amazon.com/directoryservice/latest/admin-guide/what_is.html)

## AWS Security Hub

Centrally view and manage security alerts and automate security checks | [Source](https://aws.amazon.com/security-hub/?aws-security-hub-blogs.sort-by=item.additionalFields.createdDate&aws-security-hub-blogs.sort-order=desc)

AWS Security Hub gives you a comprehensive view of your security alerts and security posture across your AWS accounts.

## Amazon Inspector

Analyze application security | [Source](https://aws.amazon.com/inspector/?nc2=type_a)

> Assesses applications for exposure, vulnerabilities, and deviations from best practices | [Source](https://aws.amazon.com/inspector/?nc2=type_a)

> Automated security assessments service | [Source](https://aws.amazon.com/inspector/?nc2=type_a)

Tell inspector what targets to assess, and how often. Inspector can provide assessments at any stage in the deployment lifecycle.

Amazon Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS. Amazon Inspector automatically assesses applications for exposure, vulnerabilities, and deviations from best practices.

### Resource

- [What is Amazon Inspector?](https://docs.aws.amazon.com/inspector/latest/userguide/inspector_introduction.html)

## Amazon GuardDuty (S3 Duty)

Managed threat detection service | [Source](https://aws.amazon.com/guardduty/?nc2=type_a)

Amazon GuardDuty is a threat detection service that continuously monitors for malicious activity and unauthorized behavior to protect your AWS accounts, workloads, and data stored in Amazon S3.

## Amazon Macie

Discover, clasify, and protect your data | [Source](https://aws.amazon.com/macie/?nc2=type_a)

Macie, macie-ine language security service

Amazon Macie is a fully managed data security and data privacy service that uses machine learning and pattern matching to discover and protect your sensitive data in AWS.

# Machine Learning

## Amazon CodeGuru

Find your most expensive lines of code | [Source](https://aws.amazon.com/codeguru/)

Amazon CodeGuru is a developer tool powered by machine learning that provides intelligent recommendations for improving code quality and identifying an application’s most expensive lines of code.

# Networking & Content Delivery

## ELB

Achieve fault tolerance for any application | [Source](https://aws.amazon.com/elasticloadbalancing/?nc2=type_a)

Elastic Load Balancing automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, IP addresses, and Lambda functions.

## Amazon VPC

Isolated cloud resources | [Source](https://aws.amazon.com/vpc/?nc2=type_a)

Amazon Virtual Private Cloud (Amazon VPC) lets you provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define. You have complete control over your virtual networking environment, including selection of your own IP address range, creation of subnets, and configuration of route tables and network gateways.

### VPC Peering

> VPC peering can be established between VPCs in different AWS Regions and in separate AWS Accounts. | [Source - Whizlabs Free Practice Test for AWS Certified Cloud Practitioner](https://www.whizlabs.com/learn/course/aws-certified-cloud-practitioner-practice-tests/)

A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them using private IPv4 addresses or IPv6 addresses. Instances in either VPC can communicate with each other as if they are within the same network. You can create a VPC peering connection between your own VPCs, or with a VPC in another AWS account. The VPCs can be in different regions (also known as an inter-region VPC peering connection). | [Source](https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html)

#### Resources

- [What is VPC peering?](https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html)

## Amazon Route 53

Scalable domain name system (DNS) | [Source](https://aws.amazon.com/route53/?nc2=type_a)

Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service.

> In Amazon Route 53, the geolocation routing policy allows for different resources to serve content base on the origin of the request. This in turn makes it possible in the scenario for different versions of the website to be served. | [Source - Whizlabs Free Practice Test for AWS Certified Cloud Practitioner](https://www.whizlabs.com/learn/course/aws-certified-cloud-practitioner-practice-tests/)

### Resources

- [Geolocation routing](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-geo)

### Reflecting changes globally

Each record has a TTL (time to live) value that specifies how long, in seconds, that you want DNS resolvers to cache the information in the record, such as the IP address for a web server. Until the amount of time that is specified by the TTL passes, DNS resolvers will continue to return the old value in response to DNS queries. | [Source](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/troubleshooting-new-dns-settings-not-in-effect.html#troubleshooting-new-dns-settings-not-in-effect-cached-resource-record-set)

# Management & Governance

## AWS Trusted Advisor

Optimize performance and security | [Source](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

AWS Trusted Advisor is an online tool that provides you real time guidance to help you provision your resources following AWS best practices. Trusted Advisor checks help optimize your AWS infrastructure, increase security and performance, reduce your overall costs, and monitor service limits.

## AWS Trusted Advisor best practice recommendations

### Cost optimization

AWS Trusted Advisor can save you money on AWS by eliminating unused and idle resources or by making commitments to reserved capacity. | [Source](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

### Performance

AWS Trusted Advisor can improve the performance of your service by checking your service limits, ensuring you take advantage of provisioned throughput, and monitoring for over-utilized instances. | [Source](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

### Security

AWS Trusted Advisor can improve the security of your application by closing gaps, enabling various AWS security features, and examining your permissions. | [Source](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

### Fault Tolerance

AWS Trusted Advisor can increase the availability and redundancy of your AWS application by take advantage of auto scaling, health checks, multi AZ, and backup capabilities. | [Source](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

### Service limits

AWS Trusted Advisor checks for service usage that is more than 80% of the service limit. Values are based on a snapshot, so your current usage might differ. Limit and usage data can take up to 24 hours to reflect any changes. | [Source](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

## Amazon CloudWatch

Monitor resources and applications | [Source](https://aws.amazon.com/cloudwatch/?nc2=type_a)

Amazon CloudWatch is a monitoring and observability service built for DevOps engineers, developers, site reliability engineers (SREs), and IT managers.

## AWS Systems Manager

Gain operational insights and take action | [Source](https://aws.amazon.com/systems-manager/?nc2=type_a)

Safely manage and operate you entire infrastructure.

AWS Systems Manager gives you visibility and control of your infrastructure on AWS. Systems Manager provides a unified user interface so you can view operational data from multiple AWS services and allows you to automate operational tasks across your AWS resources. With Systems Manager, you can group resources, like Amazon EC2 instances, Amazon S3 buckets, or Amazon RDS instances, by application, view operational data for monitoring and troubleshooting, and take action on your groups of resources.

## AWS Service Catalog

Create and use standardized products | [Source](https://aws.amazon.com/servicecatalog/?nc2=type_a&aws-service-catalog.sort-by=item.additionalFields.createdDate&aws-service-catalog.sort-order=desc)

AWS Service Catalog allows organizations to create and manage catalogs of IT services that are approved for use on AWS. These IT services can include everything from virtual machine images, servers, software, and databases to complete multi-tier application architectures.

Enables organizations to create and manage catalogs of IT services that are approved for use on AWS. | [Source](https://docs.aws.amazon.com/servicecatalog/latest/adminguide/introduction.html)

AWS Service Catalog allows organizations to centrally manage commonly deployed IT services, and helps organizations achieve consistent governance and meet compliance requirements.

### Resources

- [AWS Service Catalog - Getting Started](https://www.youtube.com/watch?v=A9kKy6WhqVA&ab_channel=AmazonWebServices)

## AWS CloudFormation

Create and manage AWS resources stacks with templates | [Source](https://aws.amazon.com/cloudformation/?nc2=type_a)

Manage your "Infrastructure Architecture". CloudFormation can provision and configure your AWS resource stack. Configureable with a JSON "template" or you can choose from prebuilt templates.

AWS CloudFormation gives you an easy way to model a collection of related AWS and third-party resources, provision them quickly and consistently, and manage them throughout their lifecycles, by treating infrastructure as code.

## AWS Control Tower

Set up and govern a secure, compliant multi-account environment | [Source](https://aws.amazon.com/controltower/)

If you’re an organization with multiple AWS accounts and teams, cloud setup and governance can be complex and time consuming, slowing down the very innovation you’re trying to speed up. AWS Control Tower provides the easiest way to set up and govern a new, secure, multi-account AWS environment based on best practices established through AWS’ experience working with thousands of enterprises as they move to the cloud.

## AWS Organizations

Policy-based management for multiple AWS accounts. | [Source](https://aws.amazon.com/organizations/?nc2=type_a)

AWS Organizations helps you centrally govern your environment as you grow and scale your workloads on AWS.

### Managing organizational units (OUs)

You can use organizational units (OUs) to group accounts together to administer as a single unit. | [Source](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_ous.html)

For example, you can attach a policy-based control to an OU, and all accounts within the OU automatically inherit the policy.

# Developer Tools

## AWS CodePipeline

Release software using continuous delivery | [Source](https://aws.amazon.com/codepipeline/?nc2=type_a)

A fully managed continuous delivery service that helps you automate your release pipelines for fast and reliable application and infrastructure updates.

## AWS CodeStar

Quickly develop, build, and deploy applications on AWS | [Source](https://aws.amazon.com/codestar/?c=10&pt=8)

AWS CodeStar enables you to quickly develop, build, and deploy applications on AWS. AWS CodeStar provides a unified user interface, enabling you to easily manage your software development activities in one place.

## AWS CodeBuild

Build and test code | [Source](https://aws.amazon.com/codebuild/?nc2=type_a)

Build and test code with continuous scaling. Pay only for the build time you use.

AWS CodeBuild is a fully managed continuous integration service that compiles source code, runs tests, and produces software packages that are ready to deploy.

## AWS Cloud9

Write, run, and debug code on a cloud IDE | [Source](https://aws.amazon.com/codebuild/?nc2=type_a)

A cloud IDE for writing, running, and debugging code

# Cryptography & PKI

## AWS CloudHSM

Managed hardware security module (HSM) on the AWS Cloud. | [Source](https://aws.amazon.com/cloudhsm/?nc2=type_a)

AWS CloudHSM is a cloud-based hardware security module (HSM) that enables you to easily generate and use your own encryption keys on the AWS Cloud.

## AWS Certificate Manager (ACM)

Provision, manage, and deploy SSL/TLS certificates | [Source](https://aws.amazon.com/certificate-manager/?nc2=type_a)

AWS Certificate Manager is a service that lets you easily provision, manage, and deploy public and private Secure Sockets Layer/Transport Layer Security (SSL/TLS) certificates for use with AWS services and your internal connected resources.

## AWS Key Management Service (KMS)

Managed creation and control of encryption keys | [Source](https://aws.amazon.com/kms/?nc2=type_a)

AWS Key Management Service (KMS) makes it easy for you to create and manage cryptographic keys and control their use across a wide range of AWS services and in your applications.

# Other

## AWS Personal Health Dashboard

Personalized view of AWS service health | [Source](https://aws.amazon.com/premiumsupport/technology/personal-health-dashboard/)

AWS Personal Health Dashboard provides alerts and remediation guidance when AWS is experiencing events that may impact you. Personal Health Dashboard gives you a personalized view into the performance and availability of the AWS services underlying your AWS resources.

## Shared Responsibility Model

Security and Compliance is a shared responsibility between AWS and the customer | [Source](https://aws.amazon.com/compliance/shared-responsibility-model/)

![Image of the AWS Shared Responsibility Model](assets/shared-responsibility-model.png)

# AWS Well-Architected Framework

[AWS Well-Architected Framework](https://wa.aws.amazon.com/index.en.html)

Review and improve your workloads | [Source](https://aws.amazon.com/architecture/well-architected/?wa-lens-whitepapers.sort-by=item.additionalFields.sortDate&wa-lens-whitepapers.sort-order=desc)

AWS Well-Architected helps cloud architects build secure, high-performing, resilient, and efficient infrastructure for their applications and workloads.

## AWS Well-Architected and the Five Pillars

### Operational Excellence Pillar

The operational excellence pillar focuses on running and monitoring systems to deliver business value, and continually improving processes and procedures. Key topics include automating changes, responding to events, and defining standards to manage daily operations. | [Source](https://aws.amazon.com/architecture/well-architected/?wa-lens-whitepapers.sort-by=item.additionalFields.sortDate&wa-lens-whitepapers.sort-order=desc)

### Security Pillar

The security pillar focuses on protecting information and systems. Key topics include confidentiality and integrity of data, identifying and managing who can do what with privilege management, protecting systems, and establishing controls to detect security events. | [Source](https://aws.amazon.com/architecture/well-architected/?wa-lens-whitepapers.sort-by=item.additionalFields.sortDate&wa-lens-whitepapers.sort-order=desc)

[More information can be found here](https://d1.awsstatic.com/whitepapers/architecture/AWS-Security-Pillar.pdf).

### Reliability Pillar

The reliability pillar focuses on ensuring a workload performs its intended function correctly and consistently when it’s expected to. A resilient workload quickly recovers from failures to meet business and customer demand. Key topics include distributed system design, recovery planning, and how to handle change. | [Source](https://aws.amazon.com/architecture/well-architected/?wa-lens-whitepapers.sort-by=item.additionalFields.sortDate&wa-lens-whitepapers.sort-order=desc)

### Performance Efficiency Pillar

The performance efficiency pillar focuses on using IT and computing resources efficiently. Key topics include selecting the right resource types and sizes based on workload requirements, monitoring performance, and making informed decisions to maintain efficiency as business needs evolve. | [Source](https://aws.amazon.com/architecture/well-architected/?wa-lens-whitepapers.sort-by=item.additionalFields.sortDate&wa-lens-whitepapers.sort-order=desc)

### Cost Optimization Pillar

The cost optimization pillar focuses on avoiding unnecessary costs. Key topics include understanding and controlling where money is being spent, selecting the most appropriate and right number of resource types, analyzing spend over time, and scaling to meet business needs without overspending. | [Source](https://aws.amazon.com/architecture/well-architected/?wa-lens-whitepapers.sort-by=item.additionalFields.sortDate&wa-lens-whitepapers.sort-order=desc)

[More information can be found here](https://wa.aws.amazon.com/wat.pillar.costOptimization.en.html).

# Whizlabs Tricky questions

Here are some notes from their [free practice exam](https://www.whizlabs.com/learn/course/aws-certified-cloud-practitioner-practice-tests/).

- There is no "AWS Resource center" - [Getting Started Resource Center](https://aws.amazon.com/getting-started/)
- There is no "Premium" AWS Support Plan
- "AWS Service health dashboard" - [https://status.aws.amazon.com/](https://status.aws.amazon.com/)
  - "AWS Publishes most up-to-the-minute information on AWS service availability here."

# Resources

## AWS

### Courses

- [AWS Cloud Practitioner Essentials (Second Edition)](https://www.aws.training/Details/Curriculum?id=27076)

### Other

- [Schedule and AWS Certified Cloud Practitioner exam](https://aws.amazon.com/certification/certified-cloud-practitioner/)
- [Overview of Amazon Web Services](https://d0.awsstatic.com/whitepapers/aws-overview.pdf)
- [Architecting for the Cloud AWS Best Practices](https://d1.awsstatic.com/whitepapers/AWS_Cloud_Best_Practices.pdf)
- [How AWS Pricing Works](https://d0.awsstatic.com/whitepapers/aws_pricing_overview.pdf)
- [The Total Cost of (Non) Ownership of Web Applications in the Cloud](https://media.amazonwebservices.com/AWS_TCO_Web_Applications.pdf)
- [Compare AWS Support Plans](https://aws.amazon.com/premiumsupport/plans/)

## Intellipaat

- [AWS Basic Cheat Sheet](https://intellipaat.com/mediaFiles/2019/02/AWS-Basic-Cheat-Sheet.png)

## Pluralsight

- [Fundamental cloud concepts AWS](https://app.pluralsight.com/library/courses/fundamental-cloud-concepts-aws/table-of-contents)

## Tutorials Dojo

- [https://tutorialsdojo.com/](https://tutorialsdojo.com/)

## Whizlabs

- [Free Practice Test for AWS Certified Cloud Practitioner](https://www.whizlabs.com/learn/course/aws-certified-cloud-practitioner-practice-tests/)

## Preparation

- [Prepare for Your AWS Certification Exam](https://aws.amazon.com/certification/certification-prep/)
- [Sample Questions](https://d1.awsstatic.com/training-and-certification/docs-cloud-practitioner/AWS-Certified-Cloud-Practitioner_Sample-Questions.pdf)
- [Exam Guide](https://d1.awsstatic.com/training-and-certification/docs-cloud-practitioner/AWS-Certified-Cloud-Practitioner_Exam-Guide.pdf)
- [John Fay's notes](https://github.com/keonik/AWS-cloud-practitioner-notes)

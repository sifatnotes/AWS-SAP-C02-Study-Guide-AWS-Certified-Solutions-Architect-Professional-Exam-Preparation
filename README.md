# AWS-SAP-C02-Study-Guide-AWS-Certified-Solutions-Architect-Professional-Exam-Preparation
Community-driven AWS SAP-C02 study guide with architecture notes, AWS service concepts, practical labs, exam strategy, and a 30-day preparation plan.
# AWS SAP-C02 Study Guide

A practical community study guide for the **AWS Certified Solutions Architect – Professional (SAP-C02)** exam. It focuses on architecture decisions, AWS service selection, security, reliability, performance, cost optimization, migration, modernization, and the AWS Well-Architected Framework.

> **Current exam note:** AWS states that SAP-C02 is being updated to SAP-C03. Registration for SAP-C03 opens October 27, 2026, and the last day to take SAP-C02 is November 17, 2026. Verify the current exam version before scheduling.

## Exam Overview

| Item | Details |
|---|---|
| Vendor | Amazon Web Services (AWS) |
| Certification | AWS Certified Solutions Architect – Professional |
| Exam Code | SAP-C02 |
| Level | Professional |
| Duration | 180 minutes |
| Questions | 75 total |
| Question Types | Multiple choice and multiple response |
| Scored Questions | 65 |
| Unscored Questions | 10 |
| Passing Score | 750 / 1000 |
| Recommended Experience | 2+ years designing and implementing AWS solutions |

The exam validates advanced ability to design optimized AWS solutions using the AWS Well-Architected Framework. AWS describes the target candidate as someone capable of evaluating application requirements, recommending AWS architectures, and providing guidance across complex organizations.

## Who Should Take It?

SAP-C02 is intended for experienced cloud professionals such as:

- Solutions architects
- Cloud architects
- Senior cloud engineers
- Infrastructure architects
- Technical consultants
- Engineers responsible for large AWS environments

Strong knowledge of networking, security, databases, compute, storage, automation, migration, disaster recovery, and cost management is important.

## Exam Domains

### Domain 1 — Design Solutions for Organizational Complexity — 26%

Study:

- Multi-account AWS Organizations architectures
- VPC connectivity and segmentation
- Transit Gateway and hybrid networking
- Direct Connect and VPN
- IAM and IAM Identity Center
- Centralized logging and security
- Cross-account access
- High availability and resilience
- Cost visibility and optimization

### Domain 2 — Design for New Solutions — 29%

Focus on:

- Deployment strategies
- Business continuity
- Security controls
- Reliability
- Performance optimization
- Cost-aware architecture
- Serverless and event-driven systems
- Containerized workloads
- Data-storage architecture

### Domain 3 — Continuous Improvement for Existing Solutions — 25%

Understand how to improve:

- Operational excellence
- Security
- Performance
- Reliability
- Observability
- Scalability
- Cost efficiency
- Existing application architectures

### Domain 4 — Accelerate Workload Migration and Modernization — 20%

Study:

- Migration assessment
- 7 migration strategies
- AWS migration services
- Database migration
- Storage migration
- Application modernization
- Rehosting, replatforming and refactoring
- Hybrid architectures
- Post-migration optimization

## Detailed Study Notes

### 1. AWS Networking

Know when to use:

- **VPC** — isolated network environment
- **Transit Gateway** — centralized connectivity between VPCs and networks
- **Direct Connect** — dedicated private connectivity to AWS
- **Site-to-Site VPN** — encrypted network connection
- **Route 53** — DNS and routing
- **CloudFront** — global content delivery

Example:

For many VPCs across multiple accounts, compare centralized Transit Gateway connectivity with simpler VPC peering based on scale and operational requirements.

### 2. Security

Review:

- IAM policies
- IAM roles
- IAM Identity Center
- KMS
- ACM
- CloudTrail
- Security Hub
- GuardDuty
- AWS Config
- Network ACLs
- Security groups
- Organizations SCPs

Prefer least privilege, centralized visibility, encryption, and automated controls where they satisfy the requirements.

### 3. Reliability and Disaster Recovery

Know the differences between:

- Backup and restore
- Pilot light
- Warm standby
- Multi-site active/active

Understand RTO and RPO.

Example:

A workload requiring very low recovery time may need a warm-standby or active/active design rather than a simple backup-and-restore strategy.

### 4. Storage and Databases

Compare services according to workload requirements:

- S3 for object storage
- EBS for block storage
- EFS for shared file storage
- FSx for specialized managed file systems
- RDS/Aurora for relational workloads
- DynamoDB for highly scalable NoSQL workloads
- ElastiCache for caching

### 5. Serverless and Decoupling

Understand how these services work together:

`API Gateway → Lambda → DynamoDB`

and:

`Application → SQS → Worker`

Use queues and event-driven designs when asynchronous processing, loose coupling, buffering, or independent scaling is required.

### 6. Cost Optimization

Practice comparing:

- On-Demand
- Reserved Instances
- Savings Plans
- Spot Instances
- Storage tiers
- Data-transfer costs
- Right-sizing
- Serverless pricing

The cheapest option is not automatically correct; architecture must satisfy the stated reliability, security, performance, and business requirements.

### 7. Migration

Know the common migration strategies:

1. Rehost
2. Replatform
3. Repurchase
4. Refactor/re-architect
5. Retire
6. Retain
7. Relocate

Understand when services such as AWS Application Migration Service, AWS Database Migration Service, Migration Hub, and DataSync can be appropriate.

## Practical Labs

Build small, legal AWS environments and destroy resources afterward.

1. Create a multi-AZ VPC with public/private subnets.
2. Configure an Application Load Balancer with Auto Scaling.
3. Build an S3 + CloudFront architecture.
4. Create an event-driven SQS/Lambda workflow.
5. Configure cross-account access using IAM roles.
6. Test RDS Multi-AZ concepts.
7. Build a Transit Gateway lab with multiple VPCs.
8. Practice CloudTrail and centralized logging.
9. Create a disaster-recovery design and document its RTO/RPO.
10. Compare two architectures for cost, performance, security, and reliability.

## Study Strategy

Use a requirements-first approach for scenario questions:

1. Identify the business requirement.
2. Identify constraints.
3. Determine security requirements.
4. Determine availability and RTO/RPO.
5. Consider performance and scalability.
6. Consider operational complexity.
7. Compare AWS services.
8. Eliminate options that violate requirements.
9. Choose the architecture that satisfies the complete scenario.

Do not memorize isolated service definitions only. Practice explaining **why one architecture is more appropriate than another**.

## 30-Day Study Plan

### Days 1–5
AWS Well-Architected Framework, IAM, Organizations, accounts, governance and security.

### Days 6–10
VPC, Transit Gateway, Direct Connect, VPN, Route 53 and CloudFront.

### Days 11–15
EC2, Auto Scaling, ELB, containers, Lambda, API Gateway, SQS, SNS and EventBridge.

### Days 16–20
S3, EBS, EFS, RDS, Aurora, DynamoDB, caching and data architectures.

### Days 21–24
High availability, disaster recovery, backup strategies, observability and cost optimization.

### Days 25–27
Migration, modernization, hybrid architecture and database migration.

### Days 28–29
Timed practice questions. Review every incorrect answer and identify the architectural principle behind it.

### Day 30
Full revision, weak-topic review, AWS service comparison notes and exam-day preparation.

## Common Mistakes

- Choosing a service without reading the complete scenario.
- Ignoring cost requirements.
- Confusing RTO with RPO.
- Treating security as an afterthought.
- Selecting a complex architecture when a simpler one satisfies the requirements.
- Forgetting cross-account and multi-Region considerations.
- Memorizing services without understanding their trade-offs.
- Spending too much time on one difficult question.

## Exam-Day Tips

- Read the final requirement carefully.
- Identify keywords such as **most cost-effective**, **least operational overhead**, **highly available**, **lowest latency**, or **minimum changes**.
- Eliminate clearly unsuitable architectures first.
- For multiple-response questions, verify every selected option.
- Keep track of time because the scenarios can be lengthy.
- AWS states that unanswered questions are scored incorrect and there is no penalty for guessing.

## Final Checklist

- [ ] AWS Well-Architected Framework
- [ ] Multi-account architecture
- [ ] VPC and hybrid networking
- [ ] IAM and security services
- [ ] HA and disaster recovery
- [ ] Storage and databases
- [ ] Serverless and event-driven architecture
- [ ] Containers
- [ ] Performance and scalability
- [ ] Cost optimization
- [ ] Migration strategies
- [ ] Modernization
- [ ] Monitoring and operational excellence
- [ ] Timed practice completed
- [ ] Current SAP-C02/SAP-C03 exam status verified

## Official Resources

- AWS Certified Solutions Architect – Professional:
  https://aws.amazon.com/certification/certified-solutions-architect-professional/

- AWS SAP-C02 Exam Guide:
  https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-professional-02/solutions-architect-professional-02.html

- AWS Certification Exam Guides:
  https://docs.aws.amazon.com/aws-certification/latest/examguides/aws-certification-exam-guides.html

- AWS Documentation:
  https://docs.aws.amazon.com/

## SAP-C02 Exam Voucher

Learn SecByte provides certification voucher options and discounts where available.

Voucher:
https://learn.secbyte.org/vouchers/aws-sap-c02

Always verify the voucher price, availability, eligibility, and applicable terms before purchase.

## Disclaimer

This is an independent community study guide and is not affiliated with or endorsed by Amazon Web Services, Inc. AWS and related service names are trademarks of Amazon.com, Inc. or its affiliates. Exam objectives, services, policies, pricing, and availability can change, so verify the latest information with AWS before scheduling the exam.

This repository does not contain exam dumps, leaked questions, or recalled exam questions.

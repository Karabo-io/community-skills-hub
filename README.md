# Community Skills & Opportunity Hub
AWS re/Start Project

<img width="1361" height="1030" alt="aws drawio" src="https://github.com/user-attachments/assets/c939c7a8-3c09-4e14-bf33-471c5ecd4729" />

> A serverless platform connection unemployed South African youth with skills development resources and local job opportunities


## Table of Contents

- [Project Overview](#-project-overview)
- [Problem Statement](#-problem-statement)
- [Solution](#-solution)
- [Architecture](#-architecture)
- [AWS Services Used](#-aws-services-used)
- [Key Features](#-key-features)
- [Data Model](#-data-model)
- [API Endpoints](#-api-endpoints)
- [AWS re/Start Skills Demonstrated](#-aws-restart-skills-demonstrated)
- [Screenshots & Demo](#-screenshots--demo)
- [Repository Structure](#-repository-structure)
- [Deployment Guide](#-deployment-guide)
- [Testing](#-testing)
- [Security](#-security)
- [Monitoring & Logging](#-monitoring--logging)
- [Cost Optimization](#-cost-optimization)
- [Challenges & Lessons Learned](#-challenges--lessons-learned)
- [Future Roadmap](#-future-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Acknowledgements](#-acknowledgements)
- [Contact](#-contact)


## Project Overview

The **Community Skills & Opportunity Hub** is a cloud-native, serverless web application built on AWS. It addresses the critical youth unemployment crisis in South Africa by providing a centralized platform where young people can:

- Discover local job opportunities
- Identify skill gaps and find relevant training programmes
- Access free digital skills resources
- Track their job applications

This project was developed as a capstone to demonstrate the skills acquired during the **AWS re/Start** programme, including Linux, Python, networking, security, databases, and core AWS services.


##  Problem Statement

South Africa faces a deepening socio-economic crisis that disproportionately affects young people:

- **Youth Unemployment:** According to the Quarterly Labour Force Survey (QLFS) Q2 2026, **51% of young South Africans (aged 15–34) were neither working nor able to find work**. The Department of Employment and Labour has described this as "a national emergency demanding an urgent, coordinated response."
- **Cost of Living:** The 2026 Cost of Living Report highlights that the crisis is "also a water, energy and food crisis." Households face rising interest rates, utility costs, and transport costs, making it even harder for unemployed youth to afford data, transport to interviews, or training fees.
- **Skills Development Gap:** Economic growth was only 1.1% in 2026, and findings show that "skills development and SME integration remains weak." Many young people lack the digital skills demanded by the modern economy.
- **Wealth Inequality:** The top 1% by wealth in South Africa hold **55% of the wealth**, while the bottom 50% have negative net wealth. This structural inequality limits access to opportunities for the majority.

**The result:** A generation of talented young people is locked out of the economy, not due to lack of potential, but due to lack of access to information, networks, and skills.

## The Solution
The Community Skills & Opportunity Hub provides a **free, accessible, mobile-friendly platform** that bridges the gap between unemployed youth and opportunity. It leverages serverless AWS services to remain low-cost, highly scalable, and resilient, even under load.

**Core value proposition:**
- **For youth:** One place to find jobs, learn what skills are needed, and access free training.
- **For communities:** A tool that can be deployed by local NGOs, municipalities, or TVET colleges.
- **For employers:** A pipeline of motivated, upskilled candidates.
  
A serverless web platform that:

- Lists local job opportunities filtered by location and skill
- Matches users to relevant learnerships and free training
- Curates digital skills resources (AWS Educate, Tangible Africa, TVET)
- Tracks applications and provides admin tools

  ## Architecture
  Built entirely on AWS serverless services:

  ```mermaid
graph TD
    A[User - Mobile/Desktop] --> B[CloudFront CDN]
    B --> C[S3 Bucket - Static Frontend]
    C --> D[API Gateway - REST API]
    D --> E[Lambda - Jobs Service]
    D --> F[Lambda - Skills Matcher]
    D --> G[Lambda - User Service]
    E --> H[DynamoDB - Jobs Table]
    F --> I[DynamoDB - Skills Table]
    G --> J[DynamoDB - Users Table]
    E --> K[CloudWatch Logs & Metrics]
    F --> K
    G --> K
    D --> L[SNS - Notifications Optional]
    L --> M[Email/SMS Alerts]
    

| Layer | Service | Purpose |
|-------|---------|---------|
| Frontend | S3 + CloudFront | Static hosting + CDN |
| API | API Gateway | REST endpoints |
| Compute | Lambda (Python) | Business logic |
| Data | DynamoDB | Jobs, skills, users |
| Security | IAM | Least-privilege access |
| Monitoring | CloudWatch | Logs, metrics, alarms |


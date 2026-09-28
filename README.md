# Community Skills & Opportunity Hub
AWS re/Start Project

> A serverless platform connection unemployed South African youth with skills development resources and local job opportunities


<img width="1361" height="1030" alt="aws drawio" src="https://github.com/user-attachments/assets/c939c7a8-3c09-4e14-bf33-471c5ecd4729" />



## The Problem

South Africa's youth unemployment rate reached **51% in Q2 2026**, with skills development and SME integration remaining weak. The cost of living crisis compounds this, households face rising utility, transport, and food costs while digital skills gaps exclude millions from the growing tech economy.

## The Solution
A serverless web platform that:
- Lists local job opportunities filtered by location and skill
- Matches users to relevant learnerships and free training
- Curates digital skills resources (AWS Educate, Tangible Africa, TVET)
- Tracks applications and provides admin tools

  ## Architecture
  Built entirely on AWS serverless services:

| Layer | Service | Purpose |
|-------|---------|---------|
| Frontend | S3 + CloudFront | Static hosting + CDN |
| API | API Gateway | REST endpoints |
| Compute | Lambda (Python) | Business logic |
| Data | DynamoDB | Jobs, skills, users |
| Security | IAM | Least-privilege access |
| Monitoring | CloudWatch | Logs, metrics, alarms |


# Community Skills & Opportunity Hub
AWS re/Start Project

<img width="1361" height="1030" alt="aws drawio" src="https://github.com/user-attachments/assets/c939c7a8-3c09-4e14-bf33-471c5ecd4729" />
[![AWS](https://img.shields.io/badge/AWS-Serverless-FF9900?logo=amazon-aws)](https://aws.amazon.com/)
[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?logo=python)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![AWS re/Start](https://img.shields.io/badge/AWS%20re%2FStart-Graduate-blue)](https://aws.amazon.com/training/restart/)


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


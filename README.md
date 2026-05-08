<div align="center">

# AnyCompany-Bicycle-Shop-Microservices

### Refactoring a Django Bicycle Parts Monolith into a React + AWS Serverless Microservices Architecture

<p align="center">
  <img src="https://img.shields.io/badge/status-in_progress-2ea44f?style=flat-square" alt="Status Badge" />
  <img src="https://img.shields.io/badge/phase-4_packaged-1f6feb?style=flat-square" alt="Phase Badge" />
  <img src="https://img.shields.io/badge/frontend-React-61dafb?style=flat-square&logo=react&logoColor=white" alt="React Badge" />
  <img src="https://img.shields.io/badge/framework-django-0c4b33?style=flat-square&logo=django&logoColor=white" alt="Django Badge" />
  <img src="https://img.shields.io/badge/cloud-AWS-232f3e?style=flat-square&logo=amazonaws&logoColor=white" alt="AWS Badge" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/runtime-Lambda-ff9900?style=flat-square" alt="Lambda Badge" />
  <img src="https://img.shields.io/badge/api-API_Gateway-7a3cff?style=flat-square" alt="API Gateway Badge" />
  <img src="https://img.shields.io/badge/database-DynamoDB-4053d6?style=flat-square" alt="DynamoDB Badge" />
  <img src="https://img.shields.io/badge/hosting-S3-f59e0b?style=flat-square" alt="S3 Badge" />
</p>

<p align="center">
  <b>Current Phase:</b> Phase 4 packaged with React storefront, Products and Orders APIs, DynamoDB-backed data, SAM infrastructure, and personal AWS account deployment guides for every phase archive
</p>

</div>

---

## Overview

This project focuses on refactoring the **AnyCompany Bicycle Parts application** from a Django monolith into a **React + AWS serverless microservices architecture**.

The project starts from an existing Django ecommerce application and follows a phased sprint sequence centered on frontend modernization, service decomposition, serverless API development, DynamoDB-backed service data, and AWS deployment readiness.

At the current stage, this repository functions as the **documentation and packaged-deliverable record** for the microservices project. Phases 1 through 4 are preserved as archived zip packages under `docs/phase-zips/`.

> **Schedule note:** Phases 1-4 were completed during one accelerated project week, so the sprint log below bakes all four phase deliverables into the Week 1 entry.

---

## Repository Description

AWS Cloud Institute project repository for documenting project progress, storing architecture assets, and maintaining packaged application snapshots for the AnyCompany Bicycle Parts microservices refactor.

---

## Client Scenario

**AnyCompany Bicycle Parts** has an existing Django web application that supports product listing, order submission, order lookup, and low-inventory reporting.

The existing monolith stores Products, Orders, Order Items, and Inventory in a single relational database and deploys the application as one tightly coupled unit. This project modernizes that baseline by introducing a React frontend, AWS serverless service boundaries, API Gateway routes, Lambda handlers, DynamoDB tables, and S3-hosted assets.

Original monolith reference: https://github.com/Levi-Breedlove/AnyCompany-Bicycle-Shop

---

## Current Status

| Category | Current State |
|----------|---------------|
| Project Status | In Progress |
| Timeline | Accelerated multi-phase microservices build |
| Repository Type | Documentation and packaged phase artifacts |
| Deployment Target | AWS static frontend and serverless microservices |
| Application Type | React frontend with preserved Django baseline and AWS serverless backend packages |
| Current Focus | Phase 4 complete: Products API, order history, order details, order creation, DynamoDB data, SAM infrastructure, S3 image assets, and personal AWS deployment guides |

---

## Architecture Diagram

This project uses the class activity's target AWS microservices design for refactoring the AnyCompany Bicycle Parts application.

<p align="center">
  <img src="docs/images/bicycle-parts-microservices-architecture.png" alt="Bicycle Parts Microservices Architecture Diagram" width="100%" />
</p>

**Architecture flow**  
`React UI on Amazon S3 -> Amazon API Gateway -> AWS Lambda microservices -> Amazon DynamoDB service-owned tables`

The Phase 4 package implements the core serverless pattern for catalog and order workflows. The preserved Django monolith remains available in Phase 1 for comparison and decomposition reference.

---

## Platform and Tooling

<table>
  <tr>
    <td valign="top" width="50%">

### AWS Services

| Service | Purpose |
|---------|---------|
| AWS Code Editor / EC2 | Lab development workstation and preview environment |
| GitHub / Git | Source-control handoff workflow |
| AWS CodeCommit | Optional source-control target used in class lab flow |
| Amazon S3 | Hosts frontend builds and browser-readable image assets |
| Amazon API Gateway | HTTP integration layer for service endpoints |
| AWS Lambda | Compute layer for Products and Orders microservices |
| Amazon DynamoDB | Serverless datastore for Products and Orders tables |
| AWS SAM / CloudFormation | Serverless build and deployment workflow |
| IAM | Deployment and runtime permissions for SAM, Lambda, DynamoDB, S3, and API Gateway |
| Amazon CloudWatch Logs | Lambda runtime logging and troubleshooting |

  </td>
  <td valign="top" width="50%">

### Tech Stack

| Layer | Tools / Services |
|-------|------------------|
| Frontend | React, Vite, JavaScript |
| Backend Baseline | Python, Django |
| Serverless Backend | Python 3.12 Lambda handlers, AWS SAM |
| Source Control | Git, GitHub, AWS CodeCommit |
| Testing | Vitest, React Testing Library, Django test runner, Coverage.py |
| Code Quality | ESLint, Pylint, pylint-django |
| Documentation | Markdown, architecture image assets, AWS setup guides |

  </td>
  </tr>
</table>

---

## Project Scope and What This Capstone Demonstrates

This capstone-style project takes an existing Django bicycle parts ecommerce application through a microservices refactor while building practical experience across frontend development, service decomposition, test automation, AWS service selection, and packaged sprint delivery.

Through the completed phase sequence, this project demonstrates:

- working from an existing Django monolith
- preserving a baseline application snapshot for future comparison
- creating a React/Vite frontend foundation
- replacing static product data with a Products API
- adding order history, order details, and order creation workflows
- deploying service APIs through AWS SAM, API Gateway, Lambda, and DynamoDB
- hosting frontend image assets from Amazon S3
- documenting all personal-account AWS deployment prerequisites, IAM roles, policies, and cleanup steps
- packaging phase deliverables as clean zip archives

---

## Phase Guide and Package Notes

This repository serves as the documentation and packaging layer for the microservices project rather than the live application source itself.

At this stage, the repository contains:

- project documentation
- architecture image assets used in the README
- packaged **Phase 1**, **Phase 2**, **Phase 3**, and **Phase 4** application snapshots under `docs/phase-zips/`
- a personal AWS account setup guide inside every phase package

The live React, Django, and serverless project files are preserved inside the archived packages and are not expanded into the root repository as active source code. Each zip package acts as a point-in-time snapshot that can be used for reference, backup, migration, deployment practice, or later extraction into a live working codebase.

### AWS Setup Guide Locations

| Phase | Zip Package | AWS Guide Inside Zip |
|---|---|---|
| Phase 1 | `docs/phase-zips/phase-1-bicycle-shop-microservices.zip` | `AWS_SETUP_GUIDE.md` |
| Phase 2 | `docs/phase-zips/phase-2-bicycle-shop-microservices.zip` | `AWS_SETUP_GUIDE.md` |
| Phase 3 | `docs/phase-zips/phase-3-bicycle-shop-microservices.zip` | `microservices/AWS_SETUP_GUIDE.md` |
| Phase 4 | `docs/phase-zips/phase-4-bicycle-shop-microservices.zip` | `microservices/AWS_SETUP_GUIDE.md` |

Each guide covers the AWS services, IAM deployer permissions, Lambda runtime roles, inline policies, seed/upload script permissions, deployment commands, frontend environment values, smoke tests, troubleshooting, cleanup, and official AWS references needed to deploy that phase in a personal AWS account.

---

## Repository Structure

```bash
.
|-- docs/
|   |-- images/
|   |   `-- bicycle-parts-microservices-architecture.png
|   `-- phase-zips/
|       |-- phase-1-bicycle-shop-microservices.zip
|       |-- phase-2-bicycle-shop-microservices.zip
|       |-- phase-3-bicycle-shop-microservices.zip
|       `-- phase-4-bicycle-shop-microservices.zip
`-- README.md
```

---

## Phase Package Contents

<details>
<summary><b>Phase 1 Package Contents</b></summary>

The archived Phase 1 package contains the React/Vite frontend foundation, the preserved Django monolith baseline, and supporting development files.

```bash
phase-1-bicycle-shop-microservices.zip
|-- AWS_SETUP_GUIDE.md                         # Personal AWS S3 frontend deployment guide
|-- .gitignore
|-- bikify.sh
|-- bike-app/                                  # React/Vite frontend foundation
|   |-- deployment.md
|   |-- package.json
|   |-- vite.config.js
|   |-- public/
|   `-- src/
`-- django/                                    # Preserved Django monolith baseline
    |-- bicycle_app/
    |-- bicycle_project/
    |-- media/
    |-- static/
    |-- deployment.md
    |-- local_build.sh
    |-- products.json
    |-- requirements.txt
    |-- requirements-dev.txt
    `-- setup.sh
```

### Structure Notes

- Establishes the frontend foundation and keeps the original Django monolith available for comparison.
- Includes local validation scripts for React and Django baseline work.
- Includes `AWS_SETUP_GUIDE.md` for personal-account S3 static hosting and clear notes that API Gateway, Lambda, DynamoDB, SAM, and CloudWatch Logs arrive in later phases.

</details>

<details>
<summary><b>Phase 2 Package Contents</b></summary>

The archived Phase 2 package introduces the Products microservice and connects the React product catalog to AWS serverless backend resources.

```bash
phase-2-bicycle-shop-microservices.zip
|-- AWS_SETUP_GUIDE.md                         # Personal AWS Products service deployment guide
|-- bike-app/                                  # React app configured for API Gateway and S3 image URLs
|   |-- .env.example
|   |-- package.json
|   |-- public/images/
|   `-- src/components/Products.jsx
|-- backend/
|   |-- sam-app/
|   |   |-- template.yaml                      # Products table, GetProducts Lambda, API route
|   |   |-- handlers/get_products/
|   |   `-- tests/
|   `-- utils/
|       |-- create_products/
|       `-- s3/
|-- products-django.json
|-- products-transformed.json
`-- create_images_bucket.py
```

### Structure Notes

- Adds a DynamoDB-backed `Products` table and `GET /get_products` Lambda endpoint through AWS SAM.
- Requires the personal AWS account to create the lab-style `LambdaApplicationRoleSam` runtime role before deployment.
- Includes seed and S3 image bucket utilities. The AWS setup guide documents the manual S3 image upload step needed by this phase.

</details>

<details>
<summary><b>Phase 3 Package Contents</b></summary>

The archived Phase 3 package expands the serverless backend with order-history and order-detail read workflows.

```bash
phase-3-bicycle-shop-microservices.zip
`-- microservices/
    |-- AWS_SETUP_GUIDE.md                     # Personal AWS Products and Orders read deployment guide
    |-- bike-app/
    |   |-- .env.example
    |   |-- package.json
    |   |-- public/images/
    |   `-- src/components/
    |       |-- Products.jsx
    |       |-- OrderHistory.jsx
    |       `-- OrderDetails.jsx
    `-- backend/
        |-- sam-app/
        |   |-- template.yaml                  # Products, Orders, and read-only Lambda routes
        |   |-- handlers/get_products/
        |   |-- handlers/get_orders/
        |   `-- handlers/get_order/
        `-- utils/
            |-- create_products/
            |-- create_orders/
            `-- s3/
```

### Structure Notes

- Adds `Orders` table support plus `GET /orders` and `GET /orders/{order_id}` API routes.
- Keeps the lab-style `LambdaApplicationRoleSam` dependency and documents the exact trust policy, CloudWatch Logs managed policy, and DynamoDB read permissions required.
- Includes sample order seed data and a personal AWS setup guide with Phase 3 smoke tests.

</details>

<details>
<summary><b>Phase 4 Package Contents</b></summary>

The archived Phase 4 package completes the first end-to-end customer order workflow.

```bash
phase-4-bicycle-shop-microservices.zip
`-- microservices/
    |-- AWS_SETUP_GUIDE.md                     # Personal AWS end-to-end deployment guide
    |-- bike-app/
    |   |-- .env.example
    |   |-- package.json
    |   |-- public/images/
    |   `-- src/components/
    |       |-- Products.jsx                   # Product catalog, cart, POST /orders
    |       |-- OrderHistory.jsx
    |       `-- OrderDetails.jsx
    `-- backend/
        |-- sam-app/
        |   |-- template.yaml                  # API, Lambda, DynamoDB, IAM role, CORS
        |   |-- handlers/create_order/
        |   |-- handlers/get_products/
        |   |-- handlers/get_orders/
        |   `-- handlers/get_order/
        `-- utils/
            |-- create_products/
            |-- create_orders/
            `-- s3/
```

### Structure Notes

- Adds `POST /orders` with a `CreateOrderFunction` Lambda handler.
- Updates the SAM template to create the Lambda execution role inside the stack instead of depending on a pre-existing lab role.
- Includes S3 image upload support, richer product detail data, and a full personal AWS deployment guide covering IAM, deployment, seed data, frontend configuration, smoke tests, troubleshooting, and cleanup.

</details>

---

## Weekly Sprint Log

<details>
<summary><b>Week 1</b> - Accelerated Phase 1-4 Microservices Sprint</summary>

### Sprint Focus
- Package the React/Vite frontend foundation and preserve the Django monolith baseline
- Build the Products microservice with API Gateway, Lambda, DynamoDB, and S3 image assets
- Add order history and order detail read workflows
- Add order creation with `POST /orders` and DynamoDB persistence
- Document personal AWS account deployment requirements for every packaged phase

### Status
**Completed**

### Outcome
Week 1 produced all four packaged phase deliverables. The project moved from a preserved Django monolith baseline to a React + AWS serverless microservices package with Products and Orders APIs, DynamoDB-backed data, SAM infrastructure, S3 image asset guidance, and personal AWS account deployment guides in every phase archive.

### Phase Deliverables
| Phase | Package | Completed Work |
|---|---|---|
| Phase 1 | `phase-1-bicycle-shop-microservices.zip` | React/Vite frontend foundation, preserved Django monolith baseline, local setup and validation scripts, personal AWS S3 frontend guide |
| Phase 2 | `phase-2-bicycle-shop-microservices.zip` | Products API, `Products` DynamoDB table, `GetProductsFunction`, API Gateway route, product seed utility, S3 image bucket guidance |
| Phase 3 | `phase-3-bicycle-shop-microservices.zip` | `Orders` table, order history API, order detail API, React order views, sample order seed utility |
| Phase 4 | `phase-4-bicycle-shop-microservices.zip` | Order creation API, SAM-managed Lambda execution role, explicit API Gateway CORS, React cart checkout flow, S3 image upload workflow |

### What Was Added
- `docs/phase-zips/phase-1-bicycle-shop-microservices.zip`
- `docs/phase-zips/phase-2-bicycle-shop-microservices.zip`
- `docs/phase-zips/phase-3-bicycle-shop-microservices.zip`
- `docs/phase-zips/phase-4-bicycle-shop-microservices.zip`
- `AWS_SETUP_GUIDE.md` or `microservices/AWS_SETUP_GUIDE.md` inside every phase ZIP
- README package summaries, AWS guide path table, and completed milestone tracking for Phases 1-4

### What Was Tested
| Area | Tests / Checks | Result |
|---|---|---|
| Phase 1 package | `unzip -tq phase-1-bicycle-shop-microservices.zip` | Passed |
| Phase 2 package | `unzip -tq phase-2-bicycle-shop-microservices.zip` | Passed |
| Phase 3 package | `unzip -tq phase-3-bicycle-shop-microservices.zip` | Passed |
| Phase 4 package | `unzip -tq phase-4-bicycle-shop-microservices.zip` | Passed |
| AWS guide paths | `unzip -Z1` checks for each guide path | Present |

### Summary
Week 1 is the full accelerated sprint record for Phases 1-4. The separate phase archives remain intact as point-in-time deliverables, but the sprint log now treats them as one completed Week 1 body of work.

</details>

---

## Milestones

- [x] Archive structure prepared under `docs/phase-zips/`
- [x] `phase-1-bicycle-shop-microservices.zip` completed with the React frontend foundation, Django monolith baseline, local setup workflow, starter validation, and AWS setup guide
- [x] `phase-2-bicycle-shop-microservices.zip` completed with the Products microservice, DynamoDB Products table, Lambda/API Gateway integration, seed utilities, S3 image guidance, and AWS setup guide
- [x] `phase-3-bicycle-shop-microservices.zip` completed with order history and order details microservices, Orders table support, seed utilities, frontend order views, and AWS setup guide
- [x] `phase-4-bicycle-shop-microservices.zip` completed with order creation, SAM-managed Lambda execution role, explicit API Gateway CORS, S3 image upload workflow, and AWS setup guide
- [x] Architecture asset stored under `docs/images/`
- [x] Weekly sprint log updated with Phases 1-4 baked into the completed Week 1 sprint entry
- [x] Personal AWS deployment guides added to every phase archive

<div align="center">

# AnyCompany-Bicycle-Shop-Microservices

### Refactoring a Django Bicycle Parts Monolith into a React + AWS Serverless Microservices Architecture

<p align="center">
  <img src="https://img.shields.io/badge/status-in_progress-2ea44f?style=flat-square" alt="Status Badge" />
  <img src="https://img.shields.io/badge/phase-1_packaged-1f6feb?style=flat-square" alt="Phase Badge" />
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
  <b>Current Phase:</b> Phase 1 packaged with React/Vite frontend foundation, preserved Django monolith baseline, local validation scripts, and AWS microservices design guidance
</p>

</div>

---

## Overview

This project focuses on refactoring the **AnyCompany Bicycle Parts application** from a Django monolith into a **React + AWS serverless microservices architecture**.

The project starts from an existing Django ecommerce application and follows a multi-sprint sequence centered on frontend modernization, service decomposition, serverless API development, DynamoDB-backed service data, and eventual AWS deployment.

At the current stage, this repository functions as the **documentation and packaged-deliverable record** for the microservices project. Phase 1 is preserved as an archived zip package and has not been expanded into the repository as live source code.

---

## Repository Description

AWS Cloud Institute project repository for documenting project progress, storing architecture assets, and maintaining packaged application snapshots for the AnyCompany Bicycle Parts microservices refactor.

---

## Client Scenario

**AnyCompany Bicycle Parts** has an existing Django web application that supports product listing, order submission, order lookup, and low-inventory reporting.

The existing monolith stores Products, Orders, Order Items, and Inventory in a single relational database and deploys the application as one tightly coupled unit. This project continues the modernization work by preparing the frontend foundation, preserving the original Django baseline, and documenting the target AWS serverless microservices design.

Original monolith reference: https://github.com/Levi-Breedlove/AnyCompany-Bicycle-Shop

---

## Current Status

| Category | Current State |
|----------|---------------|
| Project Status | In Progress |
| Timeline | Multi-sprint microservices build |
| Repository Type | Documentation and packaged phase artifacts |
| Deployment Target | Future AWS static frontend and serverless microservices |
| Application Type | React frontend with preserved Django baseline |
| Current Focus | Phase 1 complete: frontend foundation, Django baseline package, local validation scripts, and AWS target architecture documentation |

---

## Architecture Diagram

This project uses the class activity's target AWS microservices design for refactoring the AnyCompany Bicycle Parts application.

<p align="center">
  <img src="docs/images/bicycle-parts-microservices-architecture.png" alt="Bicycle Parts Microservices Architecture Diagram" width="100%" />
</p>

**Architecture flow**  
`React UI on Amazon S3 → Amazon API Gateway → AWS Lambda microservices → Amazon DynamoDB service-owned tables`

> This architecture represents the target deployment pattern for the Bicycle Parts microservices project and will continue to be refined as later phases are completed.
>
> Phase 1 is narrower than the final target architecture: the package establishes the React/Vite frontend foundation and preserves the Django monolith baseline. API Gateway, Lambda, DynamoDB service tables, AWS SAM templates, and production hosting remain roadmap items for later phases.

---

## Platform and Tooling

<table>
  <tr>
    <td valign="top" width="50%">

### AWS Services and Roadmap

| Service | Purpose |
|---------|---------|
| AWS Code Editor / EC2 | Lab development workstation and preview environment |
| GitHub / Git | Stores source code changes for the current handoff workflow |
| AWS CodeCommit | Optional source-control target used in the class lab flow |
| Amazon S3 | Roadmap static hosting target for the React frontend |
| Amazon API Gateway | Roadmap HTTP integration layer for service endpoints |
| AWS Lambda | Roadmap compute layer for Products, Orders, and Inventory services |
| Amazon DynamoDB | Roadmap serverless NoSQL datastore owned by each service |
| AWS SAM | Roadmap serverless build and deployment workflow |

  </td>
  <td valign="top" width="50%">

### Tech Stack

| Layer | Tools / Services |
|-------|------------------|
| Frontend | React, Vite, JavaScript |
| Backend Baseline | Python, Django |
| Source Control | Git, GitHub, AWS CodeCommit |
| Testing | Vitest, React Testing Library, Django test runner, Coverage.py |
| Code Quality | ESLint, Pylint, pylint-django |
| Documentation | Markdown, architecture image assets, class PDF references |
| Future Cloud Services | Amazon S3, Amazon API Gateway, AWS Lambda, Amazon DynamoDB |

  </td>
  </tr>
</table>

---

## Project Scope and What This Capstone Demonstrates

This capstone-style project is designed to take an existing Django bicycle parts ecommerce application through a microservices refactor while building practical experience across frontend development, service decomposition, test automation, AWS service selection, and packaged sprint delivery.

Through the planned sprint sequence, this project demonstrates:

- working from an existing Django monolith
- preserving a baseline application snapshot for future comparison
- creating a React/Vite frontend foundation
- adding local validation scripts for both frontend and backend baseline code
- documenting a target AWS serverless microservices architecture
- preparing for future Products, Orders, and Inventory microservices
- packaging phase deliverables as clean zip archives

---

## Phase Guide and Package Notes

This repository currently serves as the documentation and packaging layer for the microservices project rather than the live application source itself.

At this stage, the repository contains:

- project documentation
- architecture image assets used in the README
- packaged **Phase 1** application snapshot stored as a zip archive under `docs/phase-zips/`

The live React and Django project files for Phase 1 are preserved inside the archived package and are not yet extracted into the root repository as active source code.

This approach keeps the repository clean while still preserving the project deliverables, architecture assets, class references, and the current state of work completed so far.

Each zip package acts as a point-in-time snapshot of the application and can be used for reference, backup, migration, or later extraction into a live working codebase.

---

## Repository Structure

```bash
.
├── docs/                                                       # Project documentation and supporting assets
│   ├── images/                                                # Images used in documentation and README
│   │   └── bicycle-parts-microservices-architecture.png       # Target AWS microservices architecture diagram
│   └── phase-zips/                                            # Archived phase deliverables
│       └── phase-1-bicycle-shop-microservices.zip             # Phase 1 packaged React frontend and Django baseline snapshot
└── README.md                                                  # Project overview, architecture, and status tracking
```

---

## Phase Package Contents

<details>
<summary><b>Phase 1 Package Contents</b></summary>

The archived Phase 1 application package contains the React/Vite frontend foundation, the preserved Django monolith baseline, and supporting development files.

```bash
phase-1-bicycle-shop-microservices.zip
├── .gitignore
├── bikify.sh
├── bike-app/                                      # React/Vite frontend foundation
│   ├── .env.example                              # Optional Vite environment values
│   ├── deployment.md                             # Frontend local and AWS preview guide
│   ├── eslint.config.js                          # ESLint configuration
│   ├── index.html                                # Vite HTML entry point
│   ├── package-lock.json                         # Locked npm dependency graph
│   ├── package.json                              # Frontend scripts and dependencies
│   ├── vite.config.js                            # Vite, React, test, and preview configuration
│   ├── public/                                   # Public favicon and icon assets
│   └── src/                                      # React source code, components, tests, and assets
└── django/                                       # Preserved Django monolith baseline
    ├── bicycle_app/                              # Django app: models, views, URLs, templates, tests
    │   ├── migrations/                           # Database schema migration files
    │   ├── templates/                            # Django HTML templates
    │   ├── admin.py                              # Django admin registrations
    │   ├── apps.py                               # App configuration
    │   ├── models.py                             # Product, Order, and Order_Item models
    │   ├── tests.py                              # Baseline Django tests
    │   ├── urls.py                               # App-level URL routing
    │   └── views.py                              # Monolith view logic and order workflow
    ├── bicycle_project/                          # Django project configuration
    │   ├── settings.py                           # Environment-aware Django settings
    │   ├── urls.py                               # Root URL configuration
    │   └── wsgi.py                               # WSGI entry point for deployment
    ├── media/                                    # Product image assets referenced by products.json
    ├── static/                                   # Template CSS and image assets required for local Django rendering
    ├── .env.example                              # Template for required environment variables
    ├── local_build.sh                            # Runs Pylint, tests, and coverage in one command
    ├── manage.py                                 # Django management CLI entry point
    ├── deployment.md                             # Phase 1 local and AWS deployment guide
    ├── products.json                             # Product fixture data
    ├── requirements-dev.txt                      # Dev dependencies: coverage, pylint-django, XML reporting
    ├── requirements.txt                          # Production dependencies: Django, Gunicorn, AWS/storage support
    └── setup.sh                                  # One-command Django local setup script
```

### Structure Notes

- **`phase-1-bicycle-shop-microservices.zip`** contains the Phase 1 React frontend and Django baseline snapshot.
- Includes `bike-app/deployment.md` with local React setup, AWS Code Editor preview, source-control handoff, and current AWS roadmap guidance.
- Includes `django/deployment.md` with local Django setup, monolith baseline notes, AWS deployment scope, and future serverless target guidance.
- `bike-app` validates with ESLint, Vitest, React Testing Library, and a Vite production build.
- `django/local_build.sh` validates the Django baseline with Django system checks, Pylint, tests, and coverage.
- Generated artifacts and unnecessary duplicate assets are excluded from the zip, including `node_modules/`, `dist/`, `.venv/`, `.coverage`, coverage reports, SQLite databases, collected static admin assets, Python cache folders, and unused screenshot/media duplicates.

</details>

---

## Weekly Sprint Log

<details>
<summary><b>Week 1</b> - Package Frontend Foundation and Monolith Baseline</summary>

### Sprint Focus
- Create and preserve the React/Vite frontend foundation
- Preserve the original Django Bicycle Parts monolith as the baseline application
- Add local setup, build, test, and deployment guidance inside the phase package
- Align the root repository with a packaged-deliverable documentation structure

### Status
**Completed**

### Outcome
The Phase 1 package now contains a validated React frontend and a preserved Django baseline. The repository root functions as a professional documentation and packaged-artifact record, while implementation details and local execution steps live inside package-level `deployment.md` files.

### What Was Added
- `docs/phase-zips/phase-1-bicycle-shop-microservices.zip` - packaged Phase 1 deliverable
- `bike-app/deployment.md` - React local development, AWS preview, and handoff guidance
- `bike-app/.env.example` - optional frontend environment configuration
- `django/` - original Django monolith baseline copied into the phase package
- `django/setup.sh` - one-command local Django setup workflow
- `django/local_build.sh` - Pylint, Django tests, and coverage validation
- `django/deployment.md` - Django baseline and AWS deployment scope guide
- `django/requirements.txt` and `django/requirements-dev.txt` - production and development dependency sets
- `django/.env.example` - local Django environment template
- `django/bicycle_app/tests.py` - baseline Django tests for package validation

### What Was Tested
| Area | Tests / Checks | Result |
|---|---|---|
| React frontend | `npm install`, `npm run lint`, `npm test -- --run`, `npm run build` | Passed |
| Django baseline | `./local_build.sh` | Passed |
| Django Pylint | `pylint-django` through `local_build.sh` | 10.00/10 |
| Django tests | Django test runner through Coverage.py | 2 tests passed |

### Summary
Week 1 established the packaged project baseline for the Bicycle Parts microservices series. The frontend foundation is ready for later API integration, the Django monolith is retained for comparison and decomposition, and the root README now follows the same documentation pattern as the referenced packaged capstone repository.

</details>

<!-- Upcoming sprint entries are retained for later updates and hidden until completed.

<details>
<summary><b>Week 2</b> - Create the Products Microservice</summary>

### Sprint Focus
- Replace static product data with a Products API
- Build the Products service with AWS serverless components
- Store product data in Amazon DynamoDB

### Status
**Roadmap / Not Started**

### Outcome
Move product listing data behind a dedicated microservice.

### Summary
This phase will begin the backend service decomposition by implementing the Products service.

</details>

<details>
<summary><b>Week 3</b> - Create Orders and Order Details Microservices</summary>

### Sprint Focus
- Add order retrieval workflows
- Add order details retrieval workflows
- Connect frontend order views to service APIs

### Status
**Roadmap / Not Started**

### Outcome
Extend the backend with order retrieval capabilities.

### Summary
This phase will expand service coverage beyond product listing into customer order lookups.

</details>

<details>
<summary><b>Week 4</b> - Create the Process Orders Microservice</summary>

### Sprint Focus
- Add POST request handling for order submission
- Persist orders in DynamoDB
- Connect the React frontend to the order submission workflow

### Status
**Roadmap / Not Started**

### Outcome
Complete the first end-to-end customer order workflow in the microservices design.

### Summary
This phase will move order creation out of the monolith and into a dedicated service.

</details>

-->

---

## Milestones

---

- [x] Archive structure prepared under `docs/phase-zips/`
- [x] `phase-1-bicycle-shop-microservices.zip` completed with the React frontend foundation, Django monolith baseline, local setup workflow, starter validation, and `deployment.md`
- [x] Architecture asset stored under `docs/images/`
- [x] Weekly sprint log aligned with the completed Week 1 zip coverage
- [ ] Phase 2 Products microservice package pending
- [ ] Phase 3 Orders and Order Details microservices package pending
- [ ] Phase 4 Process Orders microservice package pending

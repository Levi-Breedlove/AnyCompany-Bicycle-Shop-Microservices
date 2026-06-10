<div align="center">

<p>
  <img src="https://img.shields.io/badge/AWS_Serverless_Release-Phase_7_Complete-2ea44f?style=for-the-badge&logo=amazonaws&logoColor=white" alt="AWS Serverless Release Badge" />
</p>

# AnyCompany Bicycle Shop Microservices

### Django Monolith to AWS Serverless Microservices

<p align="center">
  <b>Cloud-native ecommerce platform with secure employee workflows, event-driven reporting, and distributed observability.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Frontend-React_+_Vite-61dafb?style=flat-square&logo=react&logoColor=white" alt="React and Vite Badge" />
  <img src="https://img.shields.io/badge/Backend-Python_3.12_Lambda-ff9900?style=flat-square&logo=python&logoColor=white" alt="Python Lambda Badge" />
  <img src="https://img.shields.io/badge/IaC-AWS_SAM_+_CloudFormation-232f3e?style=flat-square&logo=amazonaws&logoColor=white" alt="AWS SAM and CloudFormation Badge" />
  <img src="https://img.shields.io/badge/Auth-Cognito-dd344c?style=flat-square" alt="Cognito Badge" />
  <img src="https://img.shields.io/badge/Tracing-X--Ray-7a3cff?style=flat-square" alt="X-Ray Tracing Badge" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/API-API_Gateway-527fff?style=flat-square" alt="API Gateway Badge" />
  <img src="https://img.shields.io/badge/Compute-Lambda-ff9900?style=flat-square" alt="Lambda Badge" />
  <img src="https://img.shields.io/badge/Data-DynamoDB-4053d6?style=flat-square" alt="DynamoDB Badge" />
  <img src="https://img.shields.io/badge/Workflow-Step_Functions-cf3df6?style=flat-square" alt="Step Functions Badge" />
  <img src="https://img.shields.io/badge/Messaging-SNS-c17bff?style=flat-square" alt="SNS Badge" />
  <img src="https://img.shields.io/badge/Storage-S3-569a31?style=flat-square" alt="S3 Badge" />
</p>

</div>

---

## Summary

AnyCompany Bicycle Shop Microservices is a serverless modernization of a Django bicycle parts application. The platform provides public product and order workflows, authenticated employee operations, inventory report generation, email notification, and end-to-end request tracing.

The application is delivered as versioned phase packages under `docs/phase-zips/`. The current release package is Phase 7, which includes the React frontend, Python Lambda services, AWS SAM backend template, DynamoDB seed utilities, Cognito-protected routes, Step Functions report orchestration, SNS notification, S3 report storage, and AWS X-Ray tracing configuration.

Original monolith reference: https://github.com/Levi-Breedlove/AnyCompany-Bicycle-Shop

---

## Architecture

<p align="center">
  <img src="docs/images/bicycle-parts-microservices-architecture.png" alt="Bicycle shop serverless microservices architecture" width="100%" />
</p>

| Flow | Path |
|---|---|
| Customer catalog | `React UI -> API Gateway -> GetProducts Lambda -> Products table` |
| Customer checkout | `React UI -> API Gateway -> CreateOrder Lambda -> Orders table` |
| Employee access | `React UI -> Cognito hosted login -> API Gateway Cognito authorizer` |
| Employee orders | `Authenticated request -> GetOrders / GetOrderDetails Lambda -> Orders table` |
| Inventory report | `CreateReport Lambda -> Step Functions -> report Lambdas -> S3 report -> SNS email` |
| Observability | `API Gateway + Lambda + Step Functions -> X-Ray traces -> CloudWatch context` |

---

## Platform Services

| Layer | Service / Tooling | Responsibility |
|---|---|---|
| Frontend | React, Vite | Browser application for catalog, cart, order history, employee login, and report creation |
| API ingress | Amazon API Gateway | REST API entry point, CORS, Cognito authorizer integration, stage tracing |
| Compute | AWS Lambda, Python 3.12 | Product, order, authentication-aware, and report workflow handlers |
| Data | Amazon DynamoDB | Products, Orders, and Inventory tables |
| Authentication | Amazon Cognito | Employee user pool, hosted login, app client, token issuance |
| Workflow | AWS Step Functions | Inventory report orchestration and parallel report processing |
| Storage | Amazon S3 | Product image assets and generated report HTML objects |
| Messaging | Amazon SNS | Inventory report email notification with presigned report link |
| Observability | AWS X-Ray, CloudWatch Logs | Distributed traces and runtime diagnostics |
| Infrastructure | AWS SAM, CloudFormation | Repeatable serverless resource definition and deployment |

---

## Application Capabilities

- Browse product catalog data served from DynamoDB through a Lambda-backed API.
- Create customer orders through a server-side validated checkout workflow.
- Authenticate employees through Amazon Cognito hosted login.
- Protect employee order history, order detail, and report routes with an API Gateway Cognito authorizer.
- Generate inventory reports through a Step Functions workflow.
- Store generated report HTML in S3 and distribute access with a presigned URL.
- Notify employees through SNS when an inventory report is ready.
- Trace distributed requests across API Gateway, Lambda, and Step Functions with X-Ray.

---

## API Surface

| Route | Method | Access | Handler |
|---|---:|---|---|
| `/get_products` | `GET` | Public | `GetProductsFunction` |
| `/orders` | `POST` | Public | `CreateOrderFunction` |
| `/orders` | `GET` | Cognito protected | `GetOrdersFunction` |
| `/orders/{order_id}` | `GET` | Cognito protected | `GetOrderDetailsFunction` |
| `/create-report` | `POST` | Cognito protected | `CreateReportFunction` |

---

## Current Release

| Field | Value |
|---|---|
| Release | Phase 7 |
| Package | `docs/phase-zips/phase-7-bicycle-shop-microservices.zip` |
| Stack definition | `microservices/backend/sam-app/template.yaml` |
| Frontend app | `microservices/bike-app/` |
| Runtime | Python 3.12 Lambda, React + Vite |
| Tracing | X-Ray enabled for API Gateway, Lambda, and Step Functions |

### Phase 7 Updates

- Lambda tracing configured with `Globals.Function.Tracing: Active`.
- API Gateway stage tracing configured with `TracingEnabled: true`.
- Step Functions tracing configured with `Tracing.Enabled: true`.
- Source template and included SAM build template kept in sync.
- Inventory report workflow preserved from Phase 6.

### Validation

| Check | Result |
|---|---|
| ZIP integrity | Passed: `unzip -t docs/phase-zips/phase-7-bicycle-shop-microservices.zip` |
| YAML syntax | Passed for source and included SAM build templates |
| X-Ray configuration | Confirmed in source and included SAM build templates |

---

## Deployment

Extract the current release package.

```bash
unzip docs/phase-zips/phase-7-bicycle-shop-microservices.zip
```

Install and run the frontend.

```bash
cd microservices/bike-app
npm install
npm run dev
```

Validate and build the backend.

```bash
cd ../backend/sam-app
sam validate
sam build
```

Deploy the serverless stack.

```bash
sam deploy --config-file samconfig.toml
```

Before deployment, set environment-specific values for Cognito callback URLs, SNS email endpoint, S3 bucket names, report bucket identifiers, and frontend `.env` values.

---

## Operations

| Area | Standard |
|---|---|
| Configuration | Environment-specific values are isolated in frontend `.env` files and SAM template parameters or resource properties |
| Authentication | Employee routes require Cognito-issued tokens |
| Authorization | API Gateway authorizer protects employee-only API paths |
| Data integrity | Lambda handlers validate order data server-side before persistence |
| Reporting | Step Functions controls report workflow execution and SNS notification |
| Observability | X-Ray tracing and CloudWatch Logs provide request and runtime diagnostics |
| Release packaging | Release ZIP packages preserve deployable application snapshots |

---

## Repository Structure

```bash
.
|-- docs/
|   |-- images/
|   |   |-- bicycle-parts-microservices-architecture.png
|   |   |-- bicycle-parts-microservices-architecture2.png
|   |   `-- bicycle-parts-microservices-architecture3.png
|   `-- phase-zips/
|       |-- phase-1-bicycle-shop-microservices.zip
|       |-- phase-2-bicycle-shop-microservices.zip
|       |-- phase-3-bicycle-shop-microservices.zip
|       |-- phase-4-bicycle-shop-microservices.zip
|       |-- phase-5-bicycle-shop-microservices.zip
|       |-- phase-6-bicycle-shop-microservices.zip
|       `-- phase-7-bicycle-shop-microservices.zip
`-- README.md
```

---

## Release History

| Phase | Package | Outcome |
|---|---|---|
| Phase 1 | `docs/phase-zips/phase-1-bicycle-shop-microservices.zip` | React/Vite frontend foundation and Django baseline |
| Phase 2 | `docs/phase-zips/phase-2-bicycle-shop-microservices.zip` | Products API with API Gateway, Lambda, DynamoDB, and S3 image support |
| Phase 3 | `docs/phase-zips/phase-3-bicycle-shop-microservices.zip` | Order history and order detail read APIs |
| Phase 4 | `docs/phase-zips/phase-4-bicycle-shop-microservices.zip` | Order creation workflow and SAM-managed backend deployment |
| Phase 5 | `docs/phase-zips/phase-5-bicycle-shop-microservices.zip` | Cognito employee authentication and protected order reads |
| Phase 6 | `docs/phase-zips/phase-6-bicycle-shop-microservices.zip` | Authenticated inventory report workflow with Step Functions, S3, and SNS |
| Phase 7 | `docs/phase-zips/phase-7-bicycle-shop-microservices.zip` | Distributed tracing configuration with AWS X-Ray |

---

## Project Status

Phase 7 is complete. The repository contains the current serverless release package, architecture documentation, validation record, and phase history for the AnyCompany Bicycle Shop modernization.

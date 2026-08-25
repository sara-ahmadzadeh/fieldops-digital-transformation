# FieldOps Digital Transformation

## Reconstructing Project Economics in a Field-Service Security SME

An end-to-end business intelligence and digital transformation project focused on a small security systems company operating across product sales, installation, repair, and field services.

> **The goal is not to build a dashboard. The goal is to understand how the business actually works, reconstruct the economics of individual projects, and design a better operating and information system.**

---

## 1. The Business Problem

The company has been operating successfully for years and generates consistent business through:

- CCTV and security systems
- Theft and fire alarms
- Electric shutters
- Automatic, fireproof and anti-theft doors
- Smart locks
- Organizational gates
- Installation and field services
- Repair services

However, its information is distributed across different processes.

Operational information is recorded through technician reports and an operational Excel system, while financial information, invoices, purchases and payments are handled separately through an accounting application.

As a result, management can review different parts of the business, but does not consistently have a complete economic view of an individual project.

The central question became:

> **How much did this project actually make or lose, and why?**

---

## 2. Initial Investigation

The project began as a data-analysis exercise.

Historical operational data was available, so the initial instinct was to analyze the existing Excel data and search for patterns.

However, repeated analysis did not produce sufficiently actionable insights.

The investigation then shifted from:

> "What can we find in the historical data?"

to:

> "What information does the business actually need in order to understand and manage its economics?"

This changed the direction of the project from simple retrospective analysis toward business process reconstruction and operational intelligence.

---

## 3. Current Business Flow

The current installation workflow was reconstructed as:

Customer inquiry
→ Site survey
→ Product and service estimation
→ Combined quotation
→ Customer approval and deposit
→ Procurement
→ Scheduling
→ Execution
→ Testing and handover
→ Final invoicing and payment
→ Warranty / rework when required

Repair services follow a somewhat different operational pattern and are therefore treated separately during analysis.

---

## 4. A Key Discovery: The Project Is the Economic Unit

The investigation suggests that product sales and service execution cannot be understood independently when evaluating the economics of a complete project.

A project may contain:

### Product economics
- Product selling price
- Actual purchase price
- Quantity
- Product margin

### Service economics
- Service revenue
- Internal technician effort
- Outsourced installation
- Transportation
- Tools and company resources
- Additional work

### Post-completion economics
- Warranty visits
- Rework
- Callback costs
- Customer-requested additional work

The project therefore needs to become the central unit connecting operational and financial information.

---

## 5. Different Execution Models

Installation projects may be executed through different models:

### Internal execution

Company technicians perform the work using company resources.

### Outsourced execution — installer resources

An external installer performs the installation using their own tools and transportation and receives the agreed installation payment.

### Outsourced execution — company resources

An external installer performs the work using company resources such as vehicles and tools.

The installer receives an agreed portion of the installation revenue and the company retains the remainder.

The profitability of these models has not yet been assumed.

It will be investigated through historical project reconstruction.

---

## 6. Project Economics Reconstruction

The current phase of the project is focused on reconstructing historical projects.

The company has agreed to reconstruct approximately 20 complete historical projects in order to connect:

- Customer information
- Project type
- Customer type
- Quotation
- Products sold
- Actual products used
- Purchase cost
- Service revenue
- Execution model
- Actual work performed
- Additional work
- Outsourcing
- Payments
- Warranty / rework
- Final project economics

The purpose is not simply to collect more data.

The purpose is to determine which information is necessary to understand the economic reality of a project.

---

## 7. Customer Segmentation

Customer type will be captured as part of the reconstruction process.

Initial categories include:

- Residential
- Commercial
- Organizational
- Industrial
- Other

These categories are currently data dimensions rather than proven business segments.

Their usefulness will be evaluated after sufficient project data has been reconstructed.

---

## 8. Data Transformation Direction

The intended future information model is project-centered:

Customer
→ Project
→ Quotation
→ Products
→ Services
→ Execution
→ Additional Work
→ Warranty / Rework
→ Invoice
→ Payment
→ Project Economics

The eventual system may require role-based access because financial information is intentionally restricted within the organization.

Operational users should only see the information required for their responsibilities, while management should be able to access the complete economic picture.

---

## 9. Project Objectives

The project aims to determine:

1. How profitable individual projects actually are.
2. How product and service economics interact.
3. Whether different execution models produce different economic outcomes.
4. Where untracked or unbilled work occurs.
5. How much warranty and rework actually costs.
6. Whether repair services are profitable.
7. Which operational information should be collected in the future.
8. How operational and financial information can be connected.
9. Which KPIs are genuinely useful for management.
10. What kind of digital operating system could support the improved process.

---

## 10. Methodology

The project follows an iterative approach:

**Discover → Model → Reconstruct → Analyze → Validate → Redesign → Implement**

The business model and assumptions are validated with management before being treated as established facts.

Historical project reconstruction is then used to test those assumptions against actual business activity.

---

## 11. Current Status

### Completed

- Initial business investigation
- Historical operational data review
- Identification of the disconnected operational/financial processes
- Current-state workflow reconstruction
- Initial business model
- Identification of project economics as the central analytical problem
- Definition of the historical project reconstruction approach
- Identification of multiple execution models
- Identification of customer type as a potentially useful analytical dimension

### In progress

- CEO validation of the business model
- Mapping available data sources
- Reconstructing historical projects
- Connecting operational information to financial records
- Defining the final project economics model

### Future

- Data model
- Data quality assessment
- Project profitability analysis
- KPI framework
- Future-state process
- Digital architecture
- Role-based information model
- Dashboard / analytical layer
- Transformation roadmap

---

## 12. Confidentiality

This project is based on a real business environment.

The company's operational and financial information is confidential.

No confidential customer information, financial records, personal information, proprietary documents, or identifiable company data will be published in this repository.

Published datasets and examples will be anonymized, aggregated, or synthetically recreated where necessary.

---

## 13. Repository Structure

The repository will evolve alongside the project.

```

fieldops-digital-transformation/
│
├── README.md
│
├── docs/
│   ├── discovery/
│   ├── business-model/
│   ├── project-economics/
│   ├── data-model/
│   └── decisions/
│
├── data/
│   ├── raw/              # Never contains confidential company data
│   ├── processed/
│   └── synthetic/
│
├── analysis/
│
├── models/
│
├── dashboards/
│
├── architecture/
│
└── application/
```

## 14. Decision Lod


## 15. Why This Project

This project combines:
- Business analysis
- Data analysis
- Business intelligence
- Operational intelligence
- Data modeling
- Project economics
- Process redesign
- Digital transformation
- Information architecture

# Information and Responsibility Flow

## Purpose

This document describes how information moves through the current business process and how access to information differs between roles.

The purpose is to identify where operational and financial information become disconnected.

---

# 1. Functional Roles

Although the company does not necessarily operate through formally separated departments, several functional responsibilities can be identified.

| Functional area | Main responsibility |
|---|---|
| Secretary / Office | Customer communication, project follow-up, operational data entry |
| CEO | Commercial decisions, pricing, approvals, exception handling, financial oversight |
| Executive Manager | Survey, quotation, procurement, scheduling, execution management, pricing |
| Technician / Senior Technician | Field execution, operational reporting, testing and handover |
| Accountant | Financial records, invoices, payments and financial reporting |

The same person may perform multiple functions because of the company's size.

---

# 2. Customer Information

Customer information can enter the company through several channels:

- Office / secretary
- CEO
- Executive manager
- Occasionally technicians
- In-person office visits

Typical information includes:

- Customer name
- Phone number
- Address
- Inquiry date
- Requested work
- Project category

The secretary normally handles the initial record and subsequent customer communication.

Complex inquiries may be transferred to the CEO.

---

# 3. Quotation Information

Quotation decisions are primarily controlled by the CEO and executive manager.

They determine or approve:

- Required products
- Product purchase considerations
- Product selling prices
- Required installation work
- Estimated labor/time
- Service price
- Final quotation

The secretary may enter prices into the quotation when requested.

The customer receives a combined quotation covering product and service components.

---

# 4. Financial Information Access

Financial information is intentionally restricted.

A simplified access model identified during discovery is:

| Information | Technician | Service / Execution | Product / Sales | Executive Manager | Accountant | CEO |
|---|---:|---:|---:|---:|---:|---:|
| Customer information | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Product selling price | Limited | Limited | ✓ | ✓ | ✓ | ✓ |
| Product purchase price | — | — | ✓ | ✓ | ✓ | ✓ |
| Technician cost | — | — | — | Limited | ✓ | ✓ |
| Project total profit | — | — | — | Limited | ✓ | ✓ |

This table represents the current understanding and should be validated with management.

The confidentiality requirement is an important design constraint for any future information system.

---

# 5. Operational Information

Technicians receive the information required to execute the work.

They generally do not receive confidential financial information.

Technicians record operational information through standardized reports.

Since 1404, the technician reports and operational Excel structure have been synchronized.

Typical information includes:

- Time
- Materials used
- Work performed
- Additional work
- Problems encountered
- Completion information

The secretary subsequently enters or maintains operational information in the Excel system.

---

# 6. Product Information

Product information exists across different processes.

Operational records may identify products used in a project, while financial records contain purchasing and invoice information.

Important product-level economic information includes:

- Product identity
- Quantity
- Purchase price
- Selling price

The operational system does not currently contain the complete financial product information required to calculate product-level profitability.

This is one of the information gaps to be investigated through historical reconstruction.

---

# 7. Service Information

Service information is primarily controlled by the executive manager and CEO.

Relevant information includes:

- Required work
- Estimated labor/time
- Service selling price
- Assigned technicians
- Actual execution time
- Number of visits
- Additional work
- Execution problems

The operational process captures much of the execution information.

However, the financial consequences of that execution are maintained separately.

---

# 8. Outsourced Execution Information

Outsourced installation introduces an additional information requirement.

Two models have been identified.

### External resources

The installer provides their own:

- Tools
- Transportation

The installer receives the agreed installation payment.

### Company resources

The installer uses company resources such as:

- Vehicle
- Tools

The installer receives part of the installation wage.

The company retains the remainder.

The economic result of the second model is currently unknown.

To evaluate it, the project reconstruction must connect:

- Installation revenue
- Installer payment
- Company vehicle/resource usage
- Other directly attributable costs

---

# 9. Additional Work Information

Additional work can be identified by:

- Executive manager
- CEO
- Senior technician
- Technician during execution

The executive manager determines whether the customer should be charged.

Additional work may therefore exist in several information states:

1. Identified and billed
2. Identified but partially billed
3. Identified but absorbed by the company
4. Reported operationally but not connected to financial records
5. Not consistently recorded

This creates a potential gap between:

**Work performed → Work recorded → Work billed → Revenue collected**

---

# 10. Accounting Information

The accounting process contains financial information that is not currently integrated with the operational Excel data.

Relevant information includes:

- Product purchases
- Purchase costs
- Customer invoices
- Customer payments
- Outstanding balances
- Financial reporting
- Major warranty/rework costs when recorded

The accountant has access to the financial details.

The operational analyst does not currently have direct access to the complete accounting system.

Historical reconstruction therefore requires controlled access to relevant project-level financial records.

---

# 11. Payment Information

The accountant records financial transactions.

The secretary follows up with customers regarding outstanding payments.

The CEO reviews financial information:

- Regularly
- Monthly
- When anomalies occur

However, the current management process does not consistently connect payment information to the complete operational history of each project.

---

# 12. Warranty and Rework Information

Warranty/rework information is distributed across operational and management processes.

The executive manager normally receives the complaint and decides the response with the CEO when necessary.

The technician performs the assigned work.

Major costs may be recorded financially and attached to the original project.

Minor warranty and callback work may not be consistently recorded.

Therefore:

**Actual warranty cost ≠ necessarily recorded warranty cost**

This must be tested rather than assumed.

---

# 13. The Central Information Problem

The current system can be represented as several partially connected information flows:

```text
CUSTOMER
   │
   ▼
SECRETARY
   │
   ▼
OPERATIONAL RECORD
   │
   ├──────────────► EXECUTION
   │                    │
   │                    ▼
   │              TECHNICIAN REPORT
   │
   ▼
QUOTATION
   │
   ▼
PROJECT
   │
   ├──────────────► PROCUREMENT
   │                    │
   │                    ▼
   │               ACCOUNTING
   │
   └──────────────► PAYMENT
                        │
                        ▼
                    ACCOUNTING

```

The important problem is not that information does not exist.

Much of the required information already exists.

The problem is that it exists in different processes, systems, documents and access boundaries, without a consistent project-level connection.

# 14. Project ID as a Future Integration Principle

The historical reconstruction will investigate whether a single project identifier can connect:

- Customer
- Quotation
- Products
- Procurement
- Execution
- Additional work
- Invoice
- Payment
- Warranty/rework

If this proves feasible, the project identifier can become the central key of the future information architecture.

This is a hypothesis to be validated through the 20-project reconstruction.

# 15. Information-Source Investigation

For each important piece of information, the investigation should identify:

What information?

→ Where does it currently exist?

→ What exact document/system contains it?

→ Who records it?

→ Who can access it?

→ Can it be connected to a project?

This source mapping will be performed during historical project reconstruction.

# 16. Design Implication

The future system must not assume that every employee should see every piece of information.

Instead, the future design should preserve appropriate information boundaries while allowing authorized management users to obtain an integrated project-level view.

The objective is therefore:

Integrated information without unrestricted information access.

The exact technical implementation will be decided only after the business and information requirements have been validated.
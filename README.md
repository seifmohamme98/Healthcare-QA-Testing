# CareNest Clinic Booking Platform - QA Testing

A comprehensive Manual Quality Assurance testing portfolio for the "CareNest" healthcare appointment booking platform, covering the full Software Testing Life Cycle (STLC) for the **Patient Details & Promo Code Engine** requirement (REQ-FUN-05), including requirement analysis, test case design, test execution, and bug reports.

---

## 📌 Project Overview

This repository documents a complete Manual QA cycle performed against the "CareNest" clinic booking platform, based on the official Software Requirements Specification (SRS v1.0.0). The work follows a structured 5-day testing cycle:

1. **Requirement Analysis & Distribution**
2. **Task Breakdown**
3. **Test Case Design**
4. **Test Case Peer Review**
5. **Test Case Execution & Bug Reporting**

---

## 🎯 Scope of Work

- **Requirement Analysis** of REQ-FUN-05: Patient Selection logic, Beneficiary field validation, Promo Code input & normalization, discount rules (SAVE10, FLAT50, BEST-QA), and business rules (single-use code, non-negative total).
- **Test Case Design**: 31 detailed test cases covering Equivalence Partitioning, Boundary Value Analysis, Decision Table Testing, and Business Rule Testing — aligned with the SRS's Requirement Traceability Matrix (RTM).
- **Test Execution**: Manual execution of high-priority test cases against the live staging environment, with Pass/Fail results logged per case.
- **Bug Reporting**: Defects identified during execution, documented with steps to reproduce, expected vs. actual results, and business impact.

---

## 📂 Repository Structure

```
├── Healthcare_Clinic_Booking_Platform_SRS_v1.0.0.pdf   # Original SRS (source of truth)
├── Requirements/
│   └── Requirement Analysis for REQ-FUN-05
├── Test_Cases/
│   ├── Full Test Case Design document (31 test cases)
│   └── Test Execution Report (results log)
└── Bug_Reports/
    └── Detailed defect reports found during execution
```

---

## 🐞 Bugs Found

| ID | Title | Priority |
|---|---|---|
| HLTHCR3-124 | Promo code field truncates input at 10 chars instead of 15 | Medium |
| HLTHCR3-125 | SAVE10 applies a flat 10 EGP discount instead of 10% | High |
| HLTHCR3-126 | BEST-QA discount behavior under investigation | High (pending) |

---

## 🛠 Tools Used

- **Jira** — Test case management & bug tracking
- **Manual Functional Testing** — executed against a live staging environment

---

## 👤 Author

**Seif Mohamed** — QA Engineer

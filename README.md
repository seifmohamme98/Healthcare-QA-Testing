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
- **Test Case Design**: 17 detailed test cases covering Equivalence Partitioning, Boundary Value Analysis, Decision Table Testing, and Business Rule Testing — aligned with the SRS's Requirement Traceability Matrix (RTM).
- **Test Execution**: Manual execution of high-priority test cases against the live staging environment, with Pass/Fail results logged per case.
- **Bug Reporting**: Defects identified during execution, documented with steps to reproduce, expected vs. actual results, and business impact.

---

## 📂 Repository Structure

```text
├── Healthcare_Clinic_Booking_Platform_SRS_v1.0.0.pdf   # Original SRS (source of truth)
├── Requirements/
│   └── Requirement Analysis for REQ-FUN-05
├── Test_Cases/
│   ├── Full Test Case Design document (17 test cases)
│   └── Test Execution Report (results log)
└── Bug_Reports/
    └── Detailed defect reports found during execution
```

# 🐞 Defect Reports (REQ-FUN-05)

This document contains the detailed bug reports logged during the manual execution of the Checkout & Booking Engine test suite, exported directly from Jira.

---

## 1. Bug: HLTHCR3-124
**Title:** Promo code input field fails to correctly accept and process the maximum allowed length of 15 characters
* **Status:** In Progress
* **Priority:** Medium
* **Environment:** Website

**Description & Steps:**
* Attempt to enter a 15-character valid-format promo code in the checkout field.

**Expected Result:**
The input field should accept all 15 characters seamlessly without truncation, and no validation error should trigger before the user finishes typing and clicks "Apply".

**Actual Result:**
The field caps the input prematurely, failing to accept the full 15 characters.

---

## 2. Bug: HLTHCR3-125
**Title:** `SAVE10` promo code applies a flat 10 EGP discount instead of a 10% percentage discount
* **Status:** In Progress
* **Priority:** High 
* **Severity:** Low
* **Environment:** Web

**Description & Steps:**
* Proceed to checkout with a consultation fee (e.g., 90 EGP).
* Enter `SAVE10` in the Promo Code field and apply.

**Expected Result:**
Discount should be 10% (e.g., 9 EGP discount on a 90 EGP fee) and Total should be calculated accordingly (81 EGP).

**Actual Result:**
The system deducts a flat 10 EGP regardless of the percentage logic.

---

## 3. Bug: HLTHCR3-126
**Title:** `BEST-QA` fails to properly apply 100% discount rules
* **Status:** In Progress
* **Priority:** Medium
* **Severity:** Medium
* **Environment:** Web

**Description & Steps:**
* Proceed to checkout and enter the `BEST-QA` promo code.
* Apply the code.

**Expected Result:**
Discount should be 100% (Total = 0 EGP) and display message: "Discount Applied! You are officially the best QA team".

**Actual Result:**
The system fails to zero out the total and incorrectly triggers a duplicate promo code error.

## 🛠 Tools Used

* **Jira Software** — Test case management, execution tracking, and detailed bug reporting.
* **Manual Functional Testing** — Executed against a live staging environment utilizing Black-box testing techniques (Boundary Value Analysis and Equivalence Partitioning).
* **Environment** — Web Application / Google Chrome.

---

## 👤 Author

**Seif Mohamed** — Software Quality Assurance Engineer  
🔗 [LinkedIn Profile](https://www.linkedin.com/in/seif-mawad)

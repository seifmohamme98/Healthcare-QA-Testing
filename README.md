# 🏥 CareNest Clinic Booking System - QA Manual Testing
**Author:** Seif Mawad

🔗 **Live Target Application:** CareNest Clinic Booking Engine  
📌 **Project Overview:** A comprehensive Manual Quality Assurance project for the **CareNest** healthcare appointment booking platform. This project demonstrates a rigorous application of Software Testing Life Cycle (STLC) principles, focusing strictly on Functional validation and Business Logic verification for the Checkout & Booking Engine.

---

## 🎯 Scope of Work

* **Functional & Business Logic Testing:** Validated core checkout workflows, patient beneficiary logic, and dynamic pricing calculations (`REQ-FUN-05`). 
* **Test Design Techniques:** Applied **Boundary Value Analysis (BVA)** and **Equivalence Partitioning (EP)** to test promo code constraints, input length limitations, and zero-floor balance handling.
* **Defect Management & Traceability:** Documented, prioritized, and tracked defects using **Jira**, ensuring full end-to-end traceability mapped directly to the original Software Requirements Specification.

---

## 🔍 Key Discoveries & Bug Reports

During the testing phase, critical business logic and input restriction defects were identified and logged:

| Bug ID | Defect | Severity | Category | Description |
| :--- | :--- | :---: | :---: | :--- |
| **FUN-01** | Boundary Restriction Failure | **High** | Functional (BVA) | Promo code field prematurely caps input at **10 characters**, overriding the documented **15-character** limit requirement (`HLTHCR3-107`). |
| **FUN-02** | Calculation Logic Error | **High** | Business Logic | The percentage discount code `SAVE10` incorrectly applies a flat **10 EGP** deduction instead of a **10%** calculation (`HLTHCR3-119`). |
| **FUN-03** | Total Waiver System Failure | **High** | Business Logic | The 100% discount code `BEST-QA` fails to drop the total to 0 EGP and falsely triggers a `"Code already applied"` session error (`HLTHCR3-122`). |

---

## 📊 Test Execution Summary

| Module / Epic | Total Executed | Passed | Failed | Execution Rate |
| :--- | :---: | :---: | :---: | :---: |
| **Patient Selection & Beneficiary Validation** | 3 | 3 | 0 | 100% |
| **Promo Code Validation & Constraints** | 5 | 3 | 2 | 100% |
| **Discount Calculation Logic** | 4 | 2 | 2 | 100% |
| **Total Test Suite (`REQ-FUN-05`)** | **12** | **8** | **4** | **100%** |

---

## 🛠️ Tools & Methodologies

* **QA Methodologies:** Black-box Testing, Test Case Design (BVA, EP), Defect Lifecycle Management, SDLC adherence.
* **Test Management & Tracking:** Jira Software (Test execution, Bug logging, State tracking).
* **Environment:** Web Application / Google Chrome.

---

## 📂 Repository Structure

```text
├── /Requirements
│   └── CareNest_SRS_REQ-FUN-05.pdf       # Original Software Requirements Specification
├── /Test_Cases
│   ├── Jira_TestCases_Export.csv         # Complete Jira export of all 12 executed scenarios
│   └── TestCases_Execution_Report.pdf    # Detailed mapping of test steps to expected vs actual results
├── /Bug_Reports
│   ├── Defect_Log_Jira.pdf               # Comprehensive Bug Reports with severity/priority tagging
│   └── Screen_Evidence/                  # UI screenshots and PoC evidence for logged defects
└── README.md                             # Project Documentation

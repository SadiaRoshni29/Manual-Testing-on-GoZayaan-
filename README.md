# GoZayaan.com — Software Quality Assurance (SQA) Testing Project

> A practical manual SQA testing project covering the major user-facing modules and workflows of GoZayaan.com.

## 📌 Project Overview

This project presents a structured **manual Software Quality Assurance testing exercise for GoZayaan.com**, an online travel booking platform.

The objective was to test major website functionality, execute and document test cases, record expected and actual results, identify failed scenarios, prepare bug reports, organize test scenarios by priority, calculate test metrics, and document the overall testing approach.

The project follows the major customer journey from **homepage → travel search → results → selection → booking → payment**, together with account management, visa services, promotions, support, and policy pages.

| Project Information | Details |
|---|---|
| **Application Tested** | GoZayaan.com |
| **Domain** | Online Travel / OTA Platform |
| **Testing Approach** | Manual Software Testing / SQA |
| **Total Test Cases** | 163 |
| **Passed** | 156 |
| **Failed** | 7 |
| **Pass Rate** | 95.71% |
| **Fail Rate** | 4.29% |

---

## 🎯 Project Objectives

- Verify that major GoZayaan functions work as expected.
- Validate important search, booking, payment, and account workflows.
- Test valid and invalid inputs.
- Check UI and navigation behavior.
- Evaluate usability and user-facing interactions.
- Identify and document failed test cases.
- Prepare reproducible bug reports.
- Group test cases into logical test scenarios.
- Assign scenario priorities from **P0 (Critical)** to **P3 (Low)**.
- Calculate execution and pass/fail metrics.
- Document testing scope, environment, risks, and deliverables.

---

# 🧩 Modules Covered

The project covers **10 major modules** and 163 test cases.

| Module | Test Cases | Main Areas |
|---|---:|---|
| 🏠 Home | 13 | Homepage, navigation, search panel, banners, footer |
| ✈️ Flights | 40 | Search, results, filtering, sorting, booking, passenger information |
| 🏨 Hotels | 29 | Search, results, filters, hotel details, rooms, booking |
| 🧳 Tours | 13 | Listings, filters, details, participants, booking |
| 🛂 Visa | 12 | Country selection, information, application, documents |
| 👤 Account | 37 | Registration, login, profile, booking history, logout, session management |
| 💳 Payment | 1 | Payment processing |
| 🎁 Offers & Promotions | 8 | Offers, promo codes, discounts, terms |
| 🎧 Support | 6 | Contact information, live chat, FAQ, support request |
| 📄 Policies | 4 | Terms, Privacy, Refund, EMI Policy |
| **Total** | **163** | **Complete testing scope** |

---

# 🔄 Major User Journey

```text
GoZayaan.com
     │
     ▼
   HOME
     │
     ├───────────────┬───────────────┬───────────────┐
     ▼               ▼               ▼
  FLIGHTS          HOTELS          TOURS
     │               │               │
  Search           Search          Browse
     │               │               │
  Results          Results         Details
     │               │               │
 Selection       Selection       Selection
     │               │               │
     └───────────────┼───────────────┘
                     ▼
                 BOOKING
                     │
                     ▼
                  PAYMENT
                     │
                     ▼
              BOOKING COMPLETE
                     │
                     ▼
             ACCOUNT / HISTORY
```

Supporting flows:

```text
Registration → Login → Profile → Booking History → Logout

Offers → Promo Code → Discount Validation

Visa → Country → Application → Documents → Submission

Support → Contact / FAQ / Live Chat → Support Request

Policies → Terms / Privacy / Refund / EMI
```

---

# 🧪 Testing Types

| Testing Type | Purpose |
|---|---|
| **Functional Testing** | Verifies that functions produce the expected results. |
| **Integration Testing** | Checks interaction between connected modules and workflows. |
| **Negative Testing** | Checks system behavior with invalid or unexpected inputs/actions. |
| **Usability Testing** | Evaluates ease of use, clarity, navigation, and user experience. |
| **Boundary Value Testing** | Checks values at or near valid input limits. |
| **Risk-Based Testing** | Gives greater attention to high-impact areas such as booking and payment. |
| **UI Testing** | Checks visible interface elements, layout, readability, and consistency. |
| **Navigation Testing** | Verifies menus, buttons, links, headers, and footer navigation. |
| **Validation Testing** | Checks required fields and invalid information. |
| **Security Testing** | Covers authentication, logout, session behavior, and account protection. |

### Testing Types Not Treated as Separate Execution Cycles

**Browser Compatibility Testing:** The recorded test cases mainly used a browser and did not provide a complete cross-browser/OS test matrix.

**Regression Testing:** The project records the executed test cycle; regression testing was not performed as a separate repeated cycle after defect fixes.

---

# 📋 Test Case Documentation

Each test case contains structured information including:

- Test Case ID / Serial Number
- Module
- Testing Type
- Feature
- Test Case Description
- Expected Result
- Actual Result
- Test Data
- Reproducing Steps
- Bug Screenshot
- Developer Comments
- Final Status
- Remarks

This provides traceability from **feature → test execution → result → defect information**.

---

# 📊 Test Execution Summary

| Result | Count | Percentage |
|---|---:|---:|
| ✅ Passed | 156 | 95.71% |
| ❌ Failed | 7 | 4.29% |
| No Run | 0 | 0% |
| Blocked | 0 | 0% |
| **Total** | **163** | **100%** |

### Execution Metrics

**Test Cases Executed**

```text
(163 / 163) × 100 = 100%
```

**Test Cases Passed**

```text
(156 / 163) × 100 = 95.71%
```

**Test Cases Failed**

```text
(7 / 163) × 100 = 4.29%
```

---

# 🐞 Failed Test Cases

Seven test cases were recorded as failed.

| Test Case | Module | Test Case | Main Issue |
|---:|---|---|---|
| **#77** | Flights | Payment navigation | Session timeout/network interruption can leave application and payment-provider transaction states inconsistent. |
| **#98** | Hotels | Room availability | External inventory/availability data may become stale, causing outdated information or delayed booking confirmation. |
| **#100** | Hotels | Hotel policies | Refund/cancellation status can be delayed or inconsistent between backend processing and user-facing booking status. |
| **#106** | Hotels | Payment navigation | Session timeout/network interruption can leave application and payment-provider transaction states inconsistent. |
| **#114** | Tours | Price calculation | Dynamic tax, fee, discount, or currency calculations may display a base amount instead of the final inclusive amount in affected listings/promotions. |
| **#150** | Payment | Mobile banking option | Session timeout/network interruption can leave application and payment-provider transaction states inconsistent. |
| **#168** | Account | Cancellation flow | Refund/cancellation status can be delayed or inconsistent between backend processing and user-facing booking status. |

These failed cases form the basis of the project's bug-reporting documentation.

---

# 🐛 Bug Reporting

The bug-reporting documentation records each identified issue with information such as:

- Bug ID
- Related Test Case
- Module
- Feature
- Bug Title
- Actual Bug / Description
- Expected Behavior
- Reproducing Steps
- Test Data
- Severity
- Priority
- Status
- Developer Comments
- Remarks

The purpose is to make each defect **clear, reproducible, and actionable**.

---

# 🚦 Test Scenario Priorities

Test scenarios are prioritized using **P0–P3**.

| Priority | Meaning | Description | Example |
|---|---|---|---|
| 🔴 **P0** | Critical / Highest | Business-critical functionality that must work. | Flight booking, hotel booking, payment, login |
| 🟠 **P1** | High | Important functionality with significant user impact. | Search/filtering, visa application, promotions |
| 🟡 **P2** | Medium | Moderate-impact functionality where a workaround may exist. | Profile management, sorting |
| 🟢 **P3** | Low | Lower-impact functionality that does not normally stop booking. | Policies, FAQ, footer/informational links |

**Priority order: P0 → P1 → P2 → P3**

> Priority describes **importance/urgency**, not whether a test case passed or failed.

---

# 🗂️ Test Scenarios

The 163 test cases are grouped into **27 logical test scenarios**, covering:

- Homepage
- Header Navigation
- Homepage Promotions
- Travel Search Widget
- Footer and Policy Navigation
- Sign-in and Account Validation
- Registration
- Flight Search
- Flight Results, Filtering and Sorting
- Flight Booking
- Hotel Search
- Hotel Results, Filtering and Sorting
- Hotel Details and Room Availability
- Hotel Booking
- Hotel Payment Navigation
- Tours
- Tour Booking
- Visa Service
- Visa Application
- Offers & Promotions
- Payment
- User Profile
- Booking Management
- Logout and Session Management
- Customer Support
- Policies

---

# 🌳 Test Case Mind Map

A visual mind map is included in the project to show the relationship between:

```text
                         GoZayaan.com
                              │
       ┌──────────┬───────────┼───────────┬───────────┐
       │          │           │           │           │
     Home      Flights      Hotels      Tours        Visa
       │          │           │           │           │
       └──────────┴───────────┴───────────┴───────────┘
                              │
              ┌───────────────┼────────────────┐
              │               │                │
           Account         Payment       Offers & Promotions
              │                                │
              └──────────────┬─────────────────┘
                             │
                    Support / Policies
```

The detailed mind map also shows individual testing steps and their **Pass/Fail status**.

---

# 🖥️ Test Environment

- **Application:** GoZayaan.com
- **Platform:** Web
- **Testing Approach:** Manual
- **Execution Date:** 13/09/2026
- **Browser Testing:** Recorded in the final test report
- **Test Data:** Valid and invalid data according to individual test cases

---

# ⚠️ Risks Considered

Important testing risks included:

- External travel inventory or availability becoming stale.
- Network interruption during booking or payment.
- Session timeout during a transaction.
- Inconsistency between payment-provider and application transaction states.
- Delayed refund/cancellation status.
- Incorrect dynamic price, fee, tax, discount, or currency calculations.
- Incorrect or incomplete booking-information validation.
- Availability changing between search and booking.

These risks are especially important because they can directly affect **booking completion, payment, pricing, and customer trust**.

---

# 📁 Suggested Repository Structure

```text
GoZayaan-SQA-Testing/
│
├── README.md
│
├── Test Cases/
│   └── GoZayaan_Test_Cases.xlsx
│
├── Bug Reports/
│   └── GoZayaan_Bug_Reports.xlsx
│
├── Test Plan/
│   └── GoZayaan_Test_Plan.docx
│
├── Test Scenarios/
│   └── GoZayaan_Test_Scenarios.xlsx
│
├── Test Metrics/
│   └── GoZayaan_Test_Metrics.xlsx
│
├── Mind Map/
│   └── GoZayaan_Test_Case_Mind_Map.png
│
└── Screenshots/
    └── Bug / Test Evidence
```

You can rename the files to match the exact files uploaded to the repository.

---

# 📝 Test Plan

The test plan documents the overall testing strategy and covers:

1. Introduction
2. Webpage Overview
3. Purpose
4. Testing Scope
5. Modules in Scope
6. Testing Types
7. Test Environment
8. Test Data
9. Test Execution
10. Entry Criteria
11. Exit Criteria
12. Defect Reporting
13. Risks and Mitigation
14. Test Deliverables
15. Conclusion

---

# 📈 Key Findings

- **163** test cases were executed.
- **156** test cases passed.
- **7** test cases failed.
- **100%** of the recorded test cases were executed.
- The overall pass rate was **95.71%**.
- The failures were concentrated around important areas such as **payment navigation, availability information, cancellation/refund status, price calculation, and account/booking flows**.
- No test cases were recorded as **No Run** or **Blocked**.

---

# 🏁 Conclusion

This project demonstrates a complete practical manual SQA workflow for GoZayaan.com.

The testing covered **10 major modules and 163 test cases**, supported by test scenarios, priority classification, test metrics, a detailed test plan, bug reports, and a visual test-case mind map.

The final result was **156 passed and 7 failed test cases**, giving a **95.71% pass rate**. The failed scenarios highlight areas that require further investigation, particularly **transaction consistency, external availability data, cancellation/refund status, and dynamic price calculation**.

Overall, the project demonstrates how a QA tester can move from **test planning and test-case design → execution → defect identification → bug reporting → metrics and final reporting**.

---

## 👩‍💻 Skills Demonstrated

- Manual Software Testing
- Software Quality Assurance
- Test Case Design
- Test Execution
- Functional Testing
- Integration Testing
- Negative Testing
- Usability Testing
- UI Testing
- Navigation Testing
- Validation Testing
- Security Testing
- Boundary Value Testing
- Risk-Based Testing
- Defect / Bug Reporting
- Test Scenario Design
- Test Prioritization
- Test Metrics
- QA Documentation
- Test Reporting

---

### ✈️ GoZayaan.com

**Explore More. Travel Further.**

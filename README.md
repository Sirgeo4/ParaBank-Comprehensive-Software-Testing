# 🏦 ParaBank Frontend Testing Graduation Project

<p align="center">
  <strong>Manual Testing • Static Code Review • UI Automation</strong><br>
  <em>A one-month, six-member software testing graduation project</em>
</p>

---

## 1. 📌 About The Project

**ParaBank Frontend Testing** is a team-based software testing project focused on evaluating the user interface and frontend-related source code of the official ParaBank demo banking application.

The project combines three complementary testing activities:

- **Manual Testing:** Validate page behavior, navigation, form validation, messages, and user workflows.
- **Static Code Review:** Inspect the actual JSP, JavaScript, CSS, and Java source files in the official ParaBank repository that implement or support each assigned page.
- **Automation Testing:** Automate stable, repeatable UI scenarios using Java, Selenium WebDriver, TestNG, and Maven.

The team consists of **6 members, including the Team Leader**, and the project duration is **4 weeks (one month)**.

> **Important:** Page ownership includes both testing the live website and reviewing the corresponding source code. Reviewing only the rendered page is not considered complete ownership.

## 2. 🎯 Project Goals

- Verify the main public and authenticated ParaBank user journeys.
- Identify functional, usability, validation, navigation, and UI consistency defects.
- Review the implementation files related to each assigned page in the official source repository.
- Connect observed UI behavior with the relevant JSP and Java implementation.
- Build one shared automation framework that all six members use.
- Produce traceable test cases, code-review notes, automation results, and bug reports.
- Keep the project limited to frontend/UI testing and frontend-related static code review.

## 3. 🔗 Project Links

| Resource | Link |
|---|---|
| Live Website | [https://parabank.parasoft.com/](https://parabank.parasoft.com/) |
| Official Source Code | [https://github.com/parasoft/parabank](https://github.com/parasoft/parabank) |
| Source JSP Directory | [WEB-INF/jsp/content](https://github.com/parasoft/parabank/tree/master/src/main/webapp/WEB-INF/jsp/content) |
| Team Repository | [Azure Coast reference repository](https://github.com/Sirgeo4/Azure-Coast) |

**Repository note:** The ParaBank source-code paths in this document refer to the official `master` repository layout inspected while preparing this plan. Re-check the branch before implementation if the upstream repository changes.

## 4. 🧪 Testing Scope

### In Scope

| Activity | Coverage |
|---|---|
| Manual UI Testing | Navigation, page rendering, forms, field validation, error/success messages, session-related UI behavior, and user workflows |
| Static Code Review | Assigned JSP files, embedded JavaScript, confirmed Java controllers, shared configuration, and shared frontend assets where identified |
| Automation Testing | Stable UI regression scenarios using Selenium WebDriver and TestNG |
| Cross-browser checks | Selected critical workflows in agreed browsers |
| Responsive/UI checks | Layout, alignment, visibility, scrolling, and basic viewport behavior |

### Out of Scope

- API Testing (REST/SOAP endpoint testing).
- Database Testing or direct database validation.
- Performance/load testing.
- Security penetration testing.
- Changing or fixing the official ParaBank application source code.

**Boundary clarification:** A UI test may observe a message or page state after a user action. It must not turn into a standalone API or database test. Static code review may read a controller to understand page behavior, but it does not include API/database test execution.

## 5. 🛠️ Technologies & Tools

| Technology / Tool | Purpose |
|---|---|
| Java | Automation programming language |
| Selenium WebDriver | Browser interaction and UI automation |
| TestNG | Test organization, assertions, grouping, and execution |
| Maven | Dependency and build management |
| Page Object Model (POM) | Maintainable separation of page locators/actions from tests |
| Git & GitHub | Version control, branches, pull requests, and collaboration |
| Browser Developer Tools | UI inspection, DOM inspection, console review, and responsive checks |
| Markdown | Test documentation and project reporting |

## 6. 🗂️ Project Structure

The team will maintain one shared automation framework. Members contribute their own page objects and test classes without creating separate frameworks.

```text
ParaBank-Testing/
│
├── README.md
├── pom.xml
├── testng.xml
│
├── src/
│   ├── main/
│   │   └── java/
│   │       └── com/parabank/
│   │           ├── base/
│   │           │   ├── BaseTest.java
│   │           │   └── BasePage.java
│   │           ├── pages/
│   │           │   ├── common/
│   │           │   ├── member1/
│   │           │   ├── member2/
│   │           │   ├── member3/
│   │           │   ├── member4/
│   │           │   ├── member5/
│   │           │   └── member6/
│   │           └── utils/
│   │               ├── DriverFactory.java
│   │               ├── ConfigReader.java
│   │               ├── WaitUtils.java
│   │               └── ScreenshotUtils.java
│   │
│   └── test/
│       ├── java/
│       │   └── com/parabank/tests/
│       │       ├── member1/
│       │       ├── member2/
│       │       ├── member3/
│       │       ├── member4/
│       │       ├── member5/
│       │       └── member6/
│       └── resources/
│           ├── config.properties
│           └── testdata/
│
├── test-output/
├── test-cases/
│   ├── manual/
│   ├── automation/
│   └── code-review/
│
├── bug-reports/
└── reports/
```

**Structure rules**

- `BaseTest` owns common browser setup and teardown.
- `BasePage` owns reusable page-level browser helpers.
- `DriverFactory` creates/configures WebDriver instances.
- `WaitUtils`, `ConfigReader`, and `ScreenshotUtils` are shared utilities.
- Page Objects contain locators and page actions; TestNG classes contain test scenarios and assertions.
- Each member owns only their assigned member package. Shared framework files are maintained collaboratively and reviewed by the Team Leader.
- The directory names are the proposed structure of this team's test project; they are not paths inside the ParaBank application repository.

## 7. 👥 Team Members & Responsibilities

| Member | Role | Main Responsibility |
|---|---|---|
| Member 1 | Team Leader | Own assigned public/authentication module, coordinate sprint progress, review pull requests, maintain project quality and integration |
| Member 2 | Team Member | Own assigned informational pages and their source-code review |
| Member 3 | Team Member | Own assigned navigation/contact/admin-inspection module and review source mappings |
| Member 4 | Team Member | Own account overview and account-opening workflows |
| Member 5 | Team Member | Own money-transfer and bill-payment UI workflows |
| Member 6 | Team Member | Own transaction, profile, loan, and logout workflows |

## 8. 📋 Detailed Task Distribution

### Source-mapping conventions

- **Verified JSP:** The filename appears in the official repository's `src/main/webapp/WEB-INF/jsp/content/` directory.
- **Verified Java class:** The class path is explicitly identified in the official source documentation/repository references.
- **Shared:** A common file/configuration supports multiple pages and is not exclusive to one member.
- **Mapping Pending:** The exact implementation file or controller was not confidently established. The assigned member must trace the route/view mapping in the repository before recording a final mapping. No filename is guessed.
- The JSP files may contain embedded JavaScript. Do not assume a separate `.js` file exists unless the repository confirms it.

| Member | Website Pages | Source Code Files | Manual Testing Tasks | Automation Testing Tasks |
|---|---|---|---|---|
| **Member 1 – Team Leader** | **Home**; **Customer Login**; **Register**; **Forgot Login Info** | **Verified JSPs:** `src/main/webapp/WEB-INF/jsp/content/index.jsp` (Home); `.../loginform.jsp` (Login); `.../register.jsp` (Register); `.../lookup.jsp` and `.../lookupConfirm.jsp` (Forgot Login Info flow). **Verified Java:** `src/main/java/com/parasoft/parabank/web/controller/LoginController.java` (login flow). **Mapping Pending:** registration and lookup controller/view mappings; exact shared CSS/JS assets. **Shared:** `src/main/webapp/WEB-INF/parabank-servlet.xml` (public view/controller mappings; not exclusive). | Check initial page rendering and navigation links; validate required/invalid/valid login inputs; verify login error and successful redirect; inspect registration required fields, field formats, validation feedback, and confirmation state; verify forgot-login form behavior and confirmation/error states; check keyboard navigation and visible labels; review the related JSP/Java logic and record code observations. As Team Leader, also review team test-case quality, code-review evidence, and incoming pull requests. | Create `HomePage`, `LoginPage`, `RegisterPage`, and `ForgotLoginPage` Page Objects; automate home navigation; automate empty/invalid login and successful login with approved test data; automate required-field and validation checks for registration; automate forgot-login form validation and confirmation UI; add assertions for messages, page headings, and redirects. Keep test data/configuration in shared resources. |
| **Member 2** | **Solutions**; **About Us**; **Services** | **Verified JSPs:** `src/main/webapp/WEB-INF/jsp/content/about.jsp`; `.../services.jsp`. **Mapping Pending:** Solutions page route/view and its exact source file; exact CSS/JS assets used by these pages. **Shared:** common navigation/layout and shared frontend assets (exact paths to be confirmed in repository). | Verify each page opens from the correct navigation link; inspect page titles, headings, text, links, images, and content layout; check broken/incorrect links, missing content, and visual inconsistencies; validate navigation back to Home and between informational pages; review confirmed JSP markup and any linked shared assets; document page-to-source traceability. | Create `AboutPage`, `ServicesPage`, and a `SolutionsPage` object only after its mapping is traced; automate navigation to each confirmed page; assert page title/heading and key visible sections; verify important internal links and browser navigation; add smoke tests for page load and shared navigation. |
| **Member 3** | **Products**; **Locations**; **Contact Us**; **Site Map**; **Admin Page** (UI inspection only) | **Verified JSPs:** `src/main/webapp/WEB-INF/jsp/content/contact.jsp`; `.../contactConfirm.jsp`; `.../sitemap.jsp`; `.../admin.jsp`. **Mapping Pending:** Products and Locations page files/routes; Admin controller and exact route; exact shared CSS/JS assets. **Shared:** `src/main/webapp/WEB-INF/parabank-servlet.xml` (route/view configuration; shared, not exclusive). | Verify contact form labels, required fields, invalid/valid input feedback, and confirmation page; inspect sitemap links and destinations; inspect Products and Locations UI after tracing their mappings; inspect Admin UI only for visible layout, labels, navigation, and page rendering—do not change configuration or perform administrative actions; document inaccessible or unclear mappings. | Create `ContactPage` and `SiteMapPage` objects plus Products/Locations objects after mapping confirmation; automate contact required-field validation and confirmation UI; verify sitemap links; add read-only admin page smoke inspection only if access is explicitly available and authorized; avoid modifying admin settings/data. |
| **Member 4** | **Accounts Overview**; **Open New Account** | **Verified JSPs:** `src/main/webapp/WEB-INF/jsp/content/overview.jsp`; `.../openaccount.jsp`; `.../openaccountConfirm.jsp`. **Related verified Java/config:** `src/main/resources/applicationContext-base.xml` configures the service proxy used by banking pages. **Shared integration:** `RestServiceProxyController` handles `services_proxy/bank/*` requests; exact controller source path should be confirmed against the current repository tree before assigning a code-review line reference. **Shared:** common secure-page mappings in `src/main/webapp/WEB-INF/parabank-servlet.xml`. | Verify authenticated access and unauthenticated redirect behavior; inspect account list, account identifiers, balances, empty/error states, and formatting; test account-type selection and submission; verify confirmation/result UI and navigation back to overview; review JSP JavaScript and relevant route/service-proxy wiring without executing API/database tests. | Create `AccountsOverviewPage` and `OpenAccountPage`; automate login prerequisite through shared test setup; assert account overview visibility and key table/list elements; automate account type selection and open-account submission with approved test data; assert confirmation state and navigation; add negative checks for missing selection or unavailable controls. |
| **Member 5** | **Transfer Funds**; **Bill Pay** | **Verified JSPs:** `src/main/webapp/WEB-INF/jsp/content/transfer.jsp`; `.../billpay.jsp`; `.../billpayConfirm.jsp`. **Verified Java:** `src/main/java/com/parasoft/parabank/web/controller/BillPayController.java`. **Shared:** `src/main/resources/applicationContext-base.xml` (service proxy configuration) and `src/main/webapp/WEB-INF/parabank-servlet.xml` (secure mappings). Transfer UI uses the shared service-proxy route; do not claim a dedicated transfer controller unless confirmed. | Verify account dropdown population and selection; check transfer amount required/invalid values, submission feedback, and confirmation UI; inspect bill-pay fields (payee name, phone, address, account number, verification, amount, source account); test missing/invalid values and mismatched account verification; verify success/error messages; review `billpay.jsp` validation and `BillPayController` validation handling. | Create `TransferFundsPage` and `BillPayPage`; automate transfer form validation and a controlled valid transfer using team-approved test data; automate bill-pay required fields, invalid amount, account-number mismatch, and valid confirmation flow; assert visible result messages; ensure tests do not depend on database queries or direct API calls. |
| **Member 6** | **Find Transactions**; **Transaction Details / Activity**; **Update Contact Info**; **Request Loan**; **Logout** | **Verified JSPs:** `src/main/webapp/WEB-INF/jsp/content/findtrans.jsp`; `.../activity.jsp`; `.../transaction.jsp`; `.../transactions.jsp`; `.../requestloan.jsp`; `.../updateprofile.jsp`. **Verified Java:** `src/main/java/com/parasoft/parabank/web/controller/RequestLoanController.java`; `.../UpdateCustomerController.java`; `.../LoginController.java` (authentication/session flow; logout route still needs confirmation). **Mapping Pending:** exact logout handler/view mapping and any separate transaction controller. **Shared:** `src/main/webapp/WEB-INF/parabank-servlet.xml` secure-page mappings. | Verify transaction search criteria and empty/no-match/result states; inspect activity list and transaction details navigation; test profile form validation and confirmation feedback; test loan amount/down-payment/account selection and approved/denied result UI; verify logout navigation and protected-page behavior after logout; review the related JSP/controller logic and record any mismatch between UI behavior and implementation. | Create `FindTransactionsPage`, `ActivityPage`, `TransactionDetailsPage`, `UpdateContactInfoPage`, and `RequestLoanPage`; automate transaction search validation and result navigation; automate profile required-field/format checks and update confirmation; automate loan form validation plus visible approval/denial states using controlled data; automate logout and verify a protected page redirects to login. |

### Shared source files – ownership policy

The following files are **shared review targets**, not exclusive ownership of one member:

| Shared File / Area | Why It Is Shared | Ownership Rule |
|---|---|---|
| `src/main/webapp/WEB-INF/parabank-servlet.xml` | Spring MVC view/controller and secure-page mappings | Team Leader coordinates; each member reviews only the mappings relevant to their pages |
| `src/main/resources/applicationContext-base.xml` | Shared service-proxy configuration referenced by banking UI | Review collaboratively when tracing relevant pages |
| `src/main/webapp/WEB-INF/jsp/` common layout/includes | May provide shared page structure | Exact include filenames must be confirmed before adding them to the mapping |
| Shared CSS and JavaScript assets | May affect multiple pages | Exact asset paths are **Mapping Pending** until verified from JSP references/repository tree |
| Shared automation `BaseTest`, `BasePage`, and utilities | Used by all member test classes | Collaborative framework ownership; no member claims exclusive ownership |

### Page-to-source mapping follow-up checklist

Before a member marks source review as complete:

1. Open the assigned page's verified JSP in the official repository.
2. Trace any `<%@ include %>`, tag files, JavaScript references, and CSS references used by that JSP.
3. Trace the page URL/view name in `parabank-servlet.xml` and identify the actual controller or view-controller mapping.
4. For AJAX-driven pages, identify the referenced route and shared proxy configuration, but keep API execution outside project scope.
5. Record the exact file path, relevant method/function, and a short code-review observation in the code-review log.
6. Replace `Mapping Pending` only after the exact mapping is confirmed from source.

## 9. ⚖️ Workload Balance

Page count alone is not a fair workload measure. The team should balance effort using the following dimensions:

| Member | Workload Profile | Balancing Approach |
|---|---|---|
| Member 1 | Medium page count + authentication forms + leadership/integration | Keep leadership duties time-boxed; delegate general framework maintenance and review PRs in batches |
| Member 2 | Low-to-medium complexity informational pages; one page mapping pending | Spend additional time tracing Solutions and validating shared navigation/content |
| Member 3 | Several public pages + contact form + read-only admin inspection | Prioritize contact form testing; keep Admin strictly UI inspection |
| Member 4 | Two authenticated workflows with account state and confirmation behavior | Allocate time to both source tracing and end-to-end UI scenarios |
| Member 5 | Two high-interaction financial forms with validation and confirmation states | More test design effort is expected despite the lower page count |
| Member 6 | Highest number of workflows, including transactions, profile, loan, and logout | Split test design into transaction, profile, and loan/session groups; use shared login setup and reuse common utilities |

**Balancing rule:** Every member must deliver (1) manual test cases, (2) a source-code review record, and (3) automation tests for their assigned module. If a member finishes early, they help review shared framework code or execute peer regression—not take ownership of another member's source files without coordination.

## 10. 🗓️ Project Timeline – 4 Weeks

| Week | Focus | Expected Deliverables |
|---|---|---|
| **Week 1 – Discovery & Planning** | Understand ParaBank flows; inspect repository structure; confirm page-to-JSP/controller mappings; define test scenarios; establish Maven/TestNG framework | Finalized mapping register; test plan; initial manual test cases; shared framework skeleton |
| **Week 2 – Manual Testing & Code Review** | Execute assigned manual tests; inspect JSP/JavaScript/CSS/Java files; log defects and code observations | Manual execution results; code-review notes; reproducible bug reports |
| **Week 3 – Automation Development** | Implement Page Objects and member TestNG classes; integrate shared utilities; run tests and fix flaky tests | Member automation suites; integrated TestNG suite; initial automation report |
| **Week 4 – Regression & Delivery** | Run full regression; peer review; verify bug fixes where available; finalize documentation and presentation | Final test summary; consolidated bug log; code-review summary; automation report; graduation presentation |

## 11. 🧾 Test Case Documentation

All test cases must use a consistent format and unique IDs.

| Field | Description |
|---|---|
| Test Case ID | Example: `PB-M1-LOGIN-001` |
| Module / Page | Assigned page or workflow |
| Test Scenario | What behavior is being verified |
| Preconditions | Required account/session/data state |
| Test Data | Input values used; do not store real personal data |
| Steps | Numbered, reproducible actions |
| Expected Result | Correct visible UI behavior |
| Actual Result | Observed result after execution |
| Status | Pass / Fail / Blocked / Not Run |
| Test Type | Manual / Automation / Regression |
| Source Files Reviewed | Exact repository paths and relevant method/function |
| Evidence | Screenshot or short recording reference |
| Defect ID | Linked bug report, if applicable |

**Suggested ID format:** `PB-M{member}-{MODULE}-{number}`

Examples: `PB-M1-LOGIN-001`, `PB-M4-ACCOUNT-002`, `PB-M5-BILLPAY-003`.

## 12. 🐞 Bug Report Template

Every defect must be reproducible and supported by evidence.

```markdown
# Bug ID: PB-BUG-001

## Title
[Short, specific defect title]

## Module / Page
[Assigned page]

## Environment
- Browser:
- Browser Version:
- OS:
- Test Date:

## Severity
Critical / High / Medium / Low

## Priority
P1 / P2 / P3 / P4

## Preconditions
[Required state before reproducing]

## Steps to Reproduce
1.
2.
3.

## Expected Result
[Expected visible behavior]

## Actual Result
[Observed behavior]

## Evidence
[Screenshot / recording path]

## Source Code Review
- Related file:
- Method / JavaScript function / JSP section:
- Observation:

## Status
New / Open / In Progress / Fixed / Retest / Closed
```

## 13. 🤝 GitHub Collaboration Rules

1. Keep one shared automation framework; do not create a separate framework per member.
2. Use feature branches with clear names, for example:
   - `feature/member1-login-tests`
   - `feature/member4-account-pages`
   - `feature/member5-billpay-tests`
3. Commit messages should describe one focused change:
   - `test: add login validation scenarios`
   - `page: add bill payment page object`
   - `docs: update source mapping for loan module`
4. Open a Pull Request (PR) for every completed module or meaningful change.
5. At least one teammate must review each PR; the Team Leader coordinates integration and reviews.
6. Do not commit browser binaries, IDE folders, generated reports, secrets, passwords, or personal test data.
7. Keep locators in Page Objects and assertions in TestNG test classes.
8. Use explicit waits; avoid fixed `Thread.sleep()` unless there is a documented reason.
9. Never modify the official ParaBank repository as part of this testing project. Work in the team's own repository.
10. Keep test evidence and bug reports linked to their test case IDs.

## 14. 🚀 Getting Started

### Prerequisites

- Java Development Kit (JDK) installed.
- Maven installed and available from the terminal.
- Git installed.
- Chrome or another agreed browser.
- IDE such as IntelliJ IDEA or Eclipse.

### Clone the Team Repository

```bash
git clone <TEAM_REPOSITORY_URL>
cd ParaBank-Testing
```

### Run the Test Suite

```bash
mvn clean test
```

To run a specific TestNG suite:

```bash
mvn clean test -DsuiteXmlFile=testng.xml
```

The exact Maven Surefire/TestNG configuration and browser-driver setup must be committed in `pom.xml` and the shared driver utilities before the first team-wide run.

### Test Environment

- Base URL: `https://parabank.parasoft.com/`
- Use only team-approved demo/test accounts and non-sensitive test data.
- Do not put real credentials in source control.
- Tests that create or modify demo data must be coordinated to avoid members interfering with each other's runs.

## 15. 📦 Final Deliverables

At the end of the four-week project, the team should submit:

- [ ] Professional project README.
- [ ] Project test plan and scope statement.
- [ ] Final page-to-source mapping register.
- [ ] Manual test cases for every assigned page.
- [ ] Manual execution results and evidence.
- [ ] Static code-review checklist and findings per member.
- [ ] Shared Java + Selenium + TestNG + Maven automation framework.
- [ ] Page Objects and member-specific TestNG test classes.
- [ ] Consolidated bug reports with severity, priority, and evidence.
- [ ] Final regression and automation execution reports.
- [ ] Workload and contribution summary.
- [ ] Final graduation presentation.

---

## 📚 Source References

- [Official ParaBank repository](https://github.com/parasoft/parabank)
- [Official ParaBank JSP content directory](https://github.com/parasoft/parabank/tree/master/src/main/webapp/WEB-INF/jsp/content)
- [Banking Operations UI source overview](https://deepwiki.com/parasoft/parabank/5.2-banking-operations-ui)
- [Loan Request Workflow source overview](https://deepwiki.com/parasoft/parabank/5.3-loan-request-workflow)
- [Authentication and Security source overview](https://deepwiki.com/parasoft/parabank/5.5-authentication-and-security)

**Source-mapping integrity note:** This README intentionally uses `Mapping Pending` wherever the exact page-to-file/controller relationship was not confirmed. Do not replace those entries with guessed filenames. Confirm them in the official repository before implementation.

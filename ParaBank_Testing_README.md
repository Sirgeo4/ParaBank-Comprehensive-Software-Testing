# ParaBank -- Software Testing Graduation Project

> **Project type:** Frontend / Web UI Testing\
> **Team size:** 6 members (including the Team Leader)\
> **Duration:** 4 weeks\
> **Automation stack:** Java + Selenium WebDriver + TestNG + Maven\
> **Application:** [ParaBank Demo](https://parabank.parasoft.com/)\
> **Official source code:** [parasoft/parabank --
> GitHub](https://github.com/parasoft/parabank)

------------------------------------------------------------------------

## 1. Project Overview

This project focuses on testing the ParaBank web application's user
interface and user-facing workflows. The team will combine manual
testing, UI automation, and frontend-oriented static review where the
relevant source files are available.

The six members are assigned balanced page groups. **Every member is
responsible for the complete testing lifecycle of their assigned
pages**, rather than being assigned to only one testing type.

### In-scope testing

-   Manual UI and functional testing.
-   Positive and negative test scenarios.
-   Form validation and error-message checks.
-   Navigation and link validation.
-   UI layout and basic responsive checks.
-   Selenium UI automation using Java, TestNG, and Maven.
-   Frontend source review / static checks for relevant HTML, CSS, and
    JavaScript files when available.
-   Regression testing and retesting.

### Out of scope

-   API testing.
-   Database testing.
-   Backend service testing.
-   Load, stress, or performance testing unless separately approved by
    the instructor.

> The official repository contains the ParaBank demo application and
> associated web services. This graduation project intentionally limits
> its testing scope to the frontend/UI. Do not treat API or database
> work as a required deliverable unless the instructor changes the
> scope.

------------------------------------------------------------------------

## 2. Application and Source Links

  ---------------------------------------------------------------------------------
  Resource                            Link
  ----------------------------------- ---------------------------------------------
  Live ParaBank application           https://parabank.parasoft.com/

  Official ParaBank source repository https://github.com/parasoft/parabank

  Repository README                   https://github.com/parasoft/parabank#readme
  ---------------------------------------------------------------------------------

The GitHub repository is the application source. This team's repository
should contain **testing artifacts only** (test cases, automation code,
reports, and documentation), not an unnecessary copy of the entire
ParaBank application source.

------------------------------------------------------------------------

## 3. Team Structure and Balanced Work Distribution

The workload is balanced by **page complexity and expected test
effort**, not by page count alone. Public information pages are simpler,
while authenticated banking workflows require more validation and test
scenarios.

  -----------------------------------------------------------------------
  Member                  Assigned pages / module Main focus
  ----------------------- ----------------------- -----------------------
  **Member 1 -- Team      Home, Customer Login,   Entry and
  Leader**                Register, Forgot Login  authentication UI
                          Info                    

  **Member 2**            Solutions, About Us,    Public information
                          Services, Products      pages

  **Member 3**            Locations, Contact Us,  Public navigation and
                          Site Map, Admin Page    page consistency
                          (UI inspection only)    

  **Member 4**            Accounts Overview, Open Account UI workflows
                          New Account             

  **Member 5**            Transfer Funds, Bill    Banking form workflows
                          Pay                     

  **Member 6**            Find Transactions,      Customer self-service
                          Update Contact Info,    workflows
                          Request Loan, Logout    
  -----------------------------------------------------------------------

### Fairness rules

1.  Every member performs **Manual Testing, Automation Testing, and
    Static Review** for their assigned module.
2.  Every member writes test scenarios and test cases before automating
    the relevant cases.
3.  Every member executes their manual tests, records evidence, reports
    defects, and performs retesting when a fix is available.
4.  All members contribute to the shared automation framework through
    their own page objects and test classes.
5.  The Team Leader also owns Member 1's assigned module. Leadership and
    coordination are additional duties, not a replacement for testing
    work.
6.  If a page is unavailable or behaves differently in the live demo,
    record it as **Blocked / Not Available** with evidence; do not
    invent expected behavior.
7.  Admin Page testing is limited to safe UI inspection and navigation.
    Do not change administrative settings or perform destructive
    actions.

------------------------------------------------------------------------

## 4. Responsibilities and Deliverables for Every Member

Each member must deliver the same categories of work for their assigned
pages:

  -----------------------------------------------------------------------
  Phase                   Required work           Deliverable
  ----------------------- ----------------------- -----------------------
  Requirement review      Understand page         Page notes /
                          purpose, fields,        requirements
                          buttons, navigation,    
                          and expected behavior   

  Static review           Inspect relevant        Static review checklist
                          available frontend      
                          markup, styles,         
                          scripts, labels, links, 
                          and obvious UI issues   

  Test design             Create positive,        Test scenarios and test
                          negative, boundary, and cases
                          navigation scenarios    

  Manual execution        Execute test cases and  Execution sheet and
                          record actual results   evidence

  Defect reporting        Document reproducible   Bug reports with
                          UI defects              screenshots

  Automation              Automate selected       Selenium + TestNG tests
                          stable, high-value UI   
                          cases                   

  Regression              Rerun affected cases    Retest results
                          after fixes             

  Reporting               Summarize coverage,     Module test summary
                          results, blockers, and  
                          defects                 
  -----------------------------------------------------------------------

### Suggested minimum contribution per member

These are planning targets, not a reason to create duplicate or
low-value tests:

-   At least **12 meaningful manual test cases** across the assigned
    module.
-   At least **5 stable UI automation test cases**, where automation is
    technically suitable.
-   One completed static review checklist for the relevant available
    frontend files.
-   Execution evidence for the manual test cases.
-   A module summary containing Pass, Fail, Blocked, and Not Run counts.

For very simple informational pages, test cases should focus on content
presence, navigation, links, layout, and responsive behavior. For
banking workflows, test cases should focus more on form validation,
required fields, input boundaries, messages, and navigation outcomes.

------------------------------------------------------------------------

## 5. Detailed Page Assignment

### Member 1 -- Home and Authentication

**Pages** - Home - Customer Login - Register - Forgot Login Info

**Suggested scenarios** - Home page loads and main navigation is
visible. - Login fields, labels, and Login button are displayed. - Empty
and invalid login submissions show appropriate feedback. - Register form
fields and required-field validation. - Registration with valid test
data, if registration is available. - Forgot Login Info form
validation. - Navigation between Login, Register, and Forgot Login
Info. - Keyboard focus and basic form usability.

### Member 2 -- Public Information Pages

**Pages** - Solutions - About Us - Services - Products

**Suggested scenarios** - Each page opens from its navigation link. -
Page title and expected content are visible. - Internal and external
links navigate to the expected destination. - Images and visible content
load correctly. - Header, footer, and navigation remain consistent. - No
obvious text overlap, clipping, or broken layout. - Basic responsive
checks at agreed viewport sizes.

### Member 3 -- Locations and Public Navigation

**Pages** - Locations - Contact Us - Site Map - Admin Page (UI
inspection only)

**Suggested scenarios** - Locations page content and links display
correctly. - Contact Us page content and any visible form controls are
checked. - Site Map links navigate to the corresponding pages. - Footer
links work consistently. - Admin Page can be opened and its visible UI
is documented. - No administrative changes or destructive actions are
performed. - Broken links, missing content, and layout issues are
recorded.

### Member 4 -- Account Management

**Pages** - Accounts Overview - Open New Account

**Suggested scenarios** - Account Overview page opens after login. -
Account list and visible account details are displayed. - Open New
Account form controls are displayed. - Account type selection works as
expected. - Required fields and invalid selections are handled. -
Success or error feedback is displayed after submission. - Navigation
between account pages works. - UI behavior is checked with valid test
accounts only.

### Member 5 -- Banking Operations

**Pages** - Transfer Funds - Bill Pay

**Suggested scenarios** - Transfer form fields and account selectors are
displayed. - Empty, invalid, and boundary input values are checked. -
Confirmation or validation messages are displayed. - Bill Pay form
fields and required inputs are checked. - Invalid payee or amount inputs
are handled. - Navigation and form reset behavior are checked where
available. - Use only designated test accounts and non-sensitive test
data.

### Member 6 -- Customer Self-Service

**Pages** - Find Transactions - Update Contact Info - Request Loan -
Logout

**Suggested scenarios** - Transaction search controls are displayed. -
Search by each available criterion is checked. - Empty and invalid
search inputs are handled. - Contact information fields display and
validate correctly. - Update form feedback is checked using test data. -
Loan request form controls and validation messages are checked. - Logout
returns the user to the expected logged-out state. - Accessing a
protected page after logout is checked through normal UI navigation.

------------------------------------------------------------------------

## 6. Shared Automation Framework

All members must use **one shared framework**. Do not create six
separate Selenium frameworks.

### Technology

-   Java
-   Selenium WebDriver
-   TestNG
-   Maven
-   Page Object Model (POM)
-   Explicit waits
-   TestNG assertions
-   Screenshots on failure
-   TestNG / Maven test reports

### Suggested repository layout

``` text
parabank-testing/
├── README.md
├── docs/
│   ├── test-plan.md
│   ├── test-strategy.md
│   ├── requirements-and-scope.md
│   └── team-assignment.md
├── test-artifacts/
│   ├── test-scenarios/
│   ├── manual-test-cases/
│   ├── execution-results/
│   ├── bug-reports/
│   └── evidence/
├── automation/
│   ├── pom.xml
│   ├── testng.xml
│   └── src/
│       ├── main/java/
│       │   ├── base/
│       │   ├── pages/
│       │   ├── utilities/
│       │   └── config/
│       └── test/java/
│           ├── member1/
│           ├── member2/
│           ├── member3/
│           ├── member4/
│           ├── member5/
│           └── member6/
├── static-review/
│   ├── checklists/
│   └── findings/
├── reports/
│   ├── manual/
│   ├── automation/
│   └── final-summary/
└── presentation/
```

### Collaboration rules

-   `main`: stable project version.
-   `develop`: integrated team work.
-   Each member creates a feature branch for their assigned module.
-   Submit changes through Pull Requests.
-   Review automation changes before merging.
-   Do not commit passwords, personal information, browser profiles, or
    private test data.
-   Keep test data clearly marked as dummy data.
-   Use stable, descriptive test names and link automation tests to
    manual Test Case IDs where possible.

------------------------------------------------------------------------

## 7. Four-Week Timeline

  -----------------------------------------------------------------------
  Week                    All members' activities Expected output
  ----------------------- ----------------------- -----------------------
  **Week 1 -- Analysis &  Inspect assigned pages, Scope, test cases,
  Design**                confirm scope, perform  static review
                          static review, write    checklists, framework
                          scenarios and test      skeleton
                          cases, prepare the      
                          shared framework        

  **Week 2 -- Manual      Execute manual tests,   Manual execution
  Execution**             capture evidence,       results, bug reports,
                          report defects, refine  evidence
                          automation candidates   

  **Week 3 --             Implement page objects  Automated UI suite and
  Automation**            and TestNG tests, run   initial reports
                          tests, review failures, 
                          integrate member        
                          branches                

  **Week 4 -- Regression  Retest fixes, run       Final test summary,
  & Delivery**            regression, review      reports, presentation,
                          coverage, complete      clean repository
                          reports and             
                          presentation            
  -----------------------------------------------------------------------

### Weekly checkpoints

-   **End of Week 1:** Team Leader reviews all page assignments and test
    cases.
-   **End of Week 2:** Team reviews execution results and prioritizes
    defects.
-   **End of Week 3:** Team integrates and runs the shared automation
    suite.
-   **End of Week 4:** Team validates final deliverables and prepares
    the demo.

------------------------------------------------------------------------

## 8. Test Case and Bug Report Standards

### Test Case fields

-   Test Case ID
-   Module / Page
-   Test Scenario
-   Preconditions
-   Test Steps
-   Test Data
-   Expected Result
-   Actual Result
-   Status: Pass / Fail / Blocked / Not Run
-   Priority
-   Evidence reference

### Bug Report fields

-   Bug ID
-   Bug Title
-   Affected Page
-   Environment / Browser
-   Preconditions
-   Steps to Reproduce
-   Expected Result
-   Actual Result
-   Severity
-   Priority
-   Screenshot / Evidence
-   Status

Do not report a defect without reproducible steps and evidence whenever
evidence can reasonably be captured.

------------------------------------------------------------------------

## 9. Project Completion Criteria

The project is ready for final delivery when:

-   All assigned pages have been reviewed.
-   Each member has submitted their manual test cases and execution
    results.
-   Each member has completed their static review checklist.
-   Automation tests are integrated into the shared framework.
-   Test execution results are available and clearly classified.
-   Defects and blockers are documented.
-   Regression results are recorded.
-   README and project documentation are up to date.
-   The final presentation demonstrates the team's work.

Report actual coverage and execution counts. Do not claim 100% coverage
unless it is measured and supported by the test artifacts.

------------------------------------------------------------------------

## 10. Important Notes

-   ParaBank is a demonstration banking application, not a real bank.
    Use dummy accounts and test data only.
-   The live demo may change or become temporarily unavailable. Record
    the date, browser, and environment for test runs.
-   Do not perform destructive or administrative actions on the public
    demo.
-   API and database testing are excluded from this project's current
    scope.
-   Static review is limited to relevant frontend files that can
    actually be inspected. Do not claim backend source analysis as
    frontend testing.
-   The official ParaBank source repository is separate from the team's
    testing repository.

------------------------------------------------------------------------

## 11. Team Members

Replace the placeholders with the actual team members' names and GitHub
usernames.

  Role                      Name          GitHub
  ------------------------- ------------- -------------
  Member 1 -- Team Leader   To be added   To be added
  Member 2                  To be added   To be added
  Member 3                  To be added   To be added
  Member 4                  To be added   To be added
  Member 5                  To be added   To be added
  Member 6                  To be added   To be added

------------------------------------------------------------------------

**Project:** ParaBank Frontend Testing\
**Duration:** One month\
**Team:** Six members\
**Automation:** Java + Selenium + TestNG

::: {dir="rtl" align="right"}
# 🏦 ParaBank Testing Project \| مشروع اختبار ParaBank

### 💻 Frontend & UI Software Testing

مشروع تخرج لاختبار واجهة تطبيق **ParaBank** باستخدام Manual Testing
وAutomation Testing، مع مراجعة Static للملفات المرتبطة بالواجهة والمتاحة
في الـ Source Code.

🎓 Digital Egypt Initiative \| Software Testing Graduation Project
:::

------------------------------------------------------------------------

## 🌐 Project Links

  Resource                Link
  ----------------------- ---------------------------------------------
  ParaBank Live Website   https://parabank.parasoft.com/
  Official Source Code    https://github.com/parasoft/parabank
  Source Code README      https://github.com/parasoft/parabank#readme

------------------------------------------------------------------------

## 📌 About The Project \| عن المشروع

::: {dir="rtl" align="right"}
ParaBank هو تطبيق بنكي تجريبي مقدم من Parasoft، ويُستخدم في مشروع التخرج
لتطبيق مفاهيم وممارسات الـ Software Testing على موقع ويب يحتوي على صفحات
عامة وخدمات بنكية تتطلب تسجيل الدخول.

هدف فريقنا هو اختبار واجهة الموقع والتأكد من أن الصفحات والوظائف الظاهرة
للمستخدم تعمل بالشكل المتوقع، مع توثيق الأخطاء وتحويل أهم السيناريوهات
إلى اختبارات آلية.

### 🎯 Project Goals

-   🧪 تطبيق Manual Testing على صفحات الموقع.
-   🤖 تنفيذ UI Automation باستخدام Selenium.
-   🔍 إجراء Static Review للملفات المرتبطة بالواجهة والمتاحة في الـ
    Source Code.
-   📝 كتابة Test Scenarios وTest Cases.
-   🐞 اكتشاف وتوثيق Bugs بطريقة منظمة.
-   🔄 تنفيذ Retesting وRegression Testing.
-   📊 إعداد تقارير توضح نتائج الاختبار ونسبة التغطية.
:::

------------------------------------------------------------------------

## 🧪 Testing Scope \| نطاق الاختبار

  Testing Type         Description
  -------------------- ------------------------------------------------
  Manual UI Testing    اختبار الصفحات والوظائف يدويًا
  Functional Testing   التحقق من سلوك الوظائف والنتائج المتوقعة
  Negative Testing     اختبار المدخلات غير الصحيحة والحقول الفارغة
  UI Testing           فحص العناصر والتنسيق والرسائل
  Navigation Testing   اختبار الروابط والتنقل بين الصفحات
  Static Review        مراجعة ملفات الواجهة المتاحة دون تشغيل التطبيق
  Automation Testing   أتمتة سيناريوهات UI باستخدام Selenium
  Regression Testing   إعادة اختبار الوظائف بعد التعديلات

> **Out of Scope:** API Testing وDatabase Testing وBackend Testing ليست
> ضمن نطاق هذا المشروع حاليًا، إلا إذا تم اعتماد تغيير رسمي من المهندس
> المشرف.

------------------------------------------------------------------------

## 🛠️ Technologies & Tools

  Technology / Tool         Usage
  ------------------------- --------------------------------------
  Java                      لغة كتابة Automation Scripts
  Selenium WebDriver        Browser UI Automation
  TestNG                    Test Execution & Assertions
  Maven                     Project & Dependency Management
  Git & GitHub              Version Control & Team Collaboration
  Chrome / Firefox          Browser Testing
  Excel / Google Sheets     Test Cases & Execution Tracking
  Browser DevTools          UI Inspection
  HTML / CSS / JavaScript   مراجعة ملفات الواجهة المتاحة

------------------------------------------------------------------------

## 📂 Project Structure \| هيكل المشروع

المشروع منظم بحيث تكون ملفات التوثيق والاختبارات اليدوية والـ Automation
منفصلة وواضحة.

``` text
ParaBank-Testing/
│
├── README.md
│
├── docs/
│   ├── Test-Plan.md
│   ├── Test-Strategy.md
│   ├── Project-Scope.md
│   └── Team-Assignment.md
│
├── manual-testing/
│   ├── Test-Scenarios/
│   ├── Test-Cases/
│   ├── Execution-Results/
│   ├── Bug-Reports/
│   └── Evidence/
│
├── automation/
│   ├── pom.xml
│   ├── testng.xml
│   └── src/
│       ├── main/
│       │   └── java/
│       │       ├── base/
│       │       ├── pages/
│       │       └── utilities/
│       │
│       └── test/
│           └── java/
│               ├── member1/
│               ├── member2/
│               ├── member3/
│               ├── member4/
│               ├── member5/
│               └── member6/
│
├── static-review/
│   ├── Checklists/
│   └── Findings/
│
├── reports/
│   ├── Manual/
│   ├── Automation/
│   └── Final-Report/
│
└── presentation/
    └── Final-Presentation.pptx
```

------------------------------------------------------------------------

## 🤝 Team Members & Responsibilities \| توزيع المهام

كل عضو مسؤول عن مجموعة صفحات محددة، ويقوم بتنفيذ مراحل الاختبار المختلفة
على الصفحات الخاصة به. تم توزيع العمل حسب حجم وتعقيد الوظائف، وليس عدد
الصفحات فقط.

### 👨‍💻 Work Distribution

  -----------------------------------------------------------------------
  Member                  Pages / Module          Responsibilities
  ----------------------- ----------------------- -----------------------
  **Member 1 -- Team      Home, Login, Register,  Manual, Automation,
  Leader**                Forgot Login Info       Static Review, Test
                                                  Documentation + Team
                                                  Coordination

  **Member 2**            Solutions, About Us     Manual, Automation,
                                                  Static Review, Test
                                                  Documentation

  **Member 3**            Services, Products,     Manual, Automation,
                          Locations, Site Map,    Static Review,
                          Contact Us, Admin Page  Navigation & Content
                          (UI inspection only)    Testing

  **Member 4**            Accounts Overview, Open Manual, Automation,
                          New Account             Static Review, Form &
                                                  Account UI Testing

  **Member 5**            Transfer Funds, Bill    Manual, Automation,
                          Pay                     Static Review, Form
                                                  Validation & Workflow
                                                  Testing

  **Member 6**            Find Transactions,      Manual, Automation,
                          Update Contact Info,    Static Review, Search &
                          Request Loan, Logout    Customer Workflow
                                                  Testing
  -----------------------------------------------------------------------

### 📋 Responsibilities of Every Member

كل عضو مسؤول عن تسليم الآتي للـ Module الخاص به:

1.  Requirement / Page Analysis.
2.  Test Scenarios.
3.  Manual Test Cases (Positive & Negative).
4.  Manual Test Execution Results.
5.  Screenshots & Test Evidence.
6.  Bug Reports عند اكتشاف أي مشكلة.
7.  Static Review Checklist للملفات المرتبطة بالواجهة والمتاحة.
8.  Selenium Automation Scripts باستخدام Java وTestNG.
9.  Automation Execution Results.
10. Retesting & Module Summary.

### ⚖️ Workload Balance

-   كل عضو يشارك في Manual Testing وAutomation وStatic Review.
-   الصفحات البسيطة يتم اختبارها من ناحية المحتوى والروابط والتنسيق
    والتنقل.
-   الصفحات البنكية يتم اختبارها من ناحية السيناريوهات والحقول والتحقق
    من المدخلات والرسائل.
-   لا يتم قياس المجهود بعدد الصفحات فقط؛ يتم مراعاة تعقيد كل صفحة.
-   قائد الفريق مسؤول أيضًا عن Module الخاص به، بالإضافة إلى التنسيق
    والمراجعة العامة.

------------------------------------------------------------------------

## 🗓️ Project Timeline \| الخطة الزمنية

مدة المشروع: **شهر واحد -- 4 أسابيع**.

  -----------------------------------------------------------------------
  Week                    Tasks                   Expected Deliverables
  ----------------------- ----------------------- -----------------------
  Week 1                  Page Analysis, Static   Test Cases + Static
                          Review, Test Scenarios  Review Checklists
                          & Test Cases            

  Week 2                  Manual Testing & Bug    Execution Results + Bug
                          Reporting               Reports

  Week 3                  Selenium Automation     Automation Scripts +
                          using Java & TestNG     Initial Reports

  Week 4                  Regression, Retesting & Final Reports +
                          Final Documentation     Presentation
  -----------------------------------------------------------------------

### Weekly Reviews

-   **Week 1:** مراجعة توزيع الصفحات والـ Test Cases.
-   **Week 2:** مراجعة نتائج الـ Manual Testing والـ Bugs.
-   **Week 3:** دمج الـ Automation Scripts وتشغيلها.
-   **Week 4:** مراجعة النتائج النهائية وتجهيز الـ Demo.

------------------------------------------------------------------------

## 🧾 Test Documentation

### Test Case Template

  Field             Description
  ----------------- ---------------------------------
  Test Case ID      Unique ID
  Module / Page     الصفحة محل الاختبار
  Test Scenario     وصف السيناريو
  Preconditions     المتطلبات المسبقة
  Test Steps        خطوات التنفيذ
  Test Data         بيانات الاختبار
  Expected Result   النتيجة المتوقعة
  Actual Result     النتيجة الفعلية
  Status            Pass / Fail / Blocked / Not Run
  Evidence          Screenshot أو مرجع الدليل

### Bug Report Template

-   Bug ID
-   Bug Title
-   Affected Page
-   Browser / Environment
-   Preconditions
-   Steps to Reproduce
-   Expected Result
-   Actual Result
-   Severity
-   Priority
-   Screenshot / Evidence
-   Status

------------------------------------------------------------------------

## 🔀 Team Collaboration Rules \| قواعد العمل الجماعي

علشان نضمن إن الشغل يمشي بشكل منظم ونتجنب تعارض التعديلات، كل أعضاء
الفريق ملتزمين بالقواعد التالية:

1.  **Page Ownership:** كل عضو مسؤول عن الصفحات المحددة له في جدول توزيع
    المهام.
2.  **Shared Framework:** جميع الأعضاء يستخدمون Automation Framework
    واحد مشترك.
3.  **No Unauthorized Changes:** ممنوع تعديل ملفات عضو آخر دون الرجوع
    إليه والاتفاق معه.
4.  **Git Workflow:** كل عضو يعمل على Branch خاص بمهمته قبل دمج
    التعديلات.
5.  **Pull Requests:** أي تعديل يتم دمجه بعد المراجعة.
6.  **Test Case IDs:** كل Test Case يجب أن يحمل ID واضحًا وفريدًا.
7.  **Bug Tracking:** كل Bug يتم توثيقه بخطوات إعادة إنتاج واضحة ودليل
    متاح.
8.  **Communication:** أي تغيير يؤثر على شغل عضو آخر يجب الاتفاق عليه
    مسبقًا.
9.  **Test Data:** استخدام بيانات تجريبية فقط وعدم رفع بيانات شخصية أو
    كلمات مرور إلى GitHub.
10. **Admin Page:** الفحص يقتصر على الواجهة والتنقل الآمن، دون تنفيذ
    تغييرات إدارية أو إجراءات مدمرة على الموقع العام.

------------------------------------------------------------------------

## 🚀 Getting Started \| بدء العمل

### 1. Clone the Testing Repository

``` bash
git clone YOUR_TESTING_REPOSITORY_URL
```

### 2. Move to the Project Directory

``` bash
cd ParaBank-Testing
```

### 3. Clone the Official ParaBank Source Code (For Source Review)

``` bash
git clone https://github.com/parasoft/parabank.git
```

> يمكن دراسة ملفات المصدر المتاحة لمراجعة الأجزاء المرتبطة بالواجهة.
> مستودع Parabank الرسمي منفصل عن مستودع فريق الاختبار.

### 4. Setup Automation Environment

تأكد من تثبيت:

-   Java JDK
-   Maven
-   Chrome أو Firefox
-   Selenium WebDriver dependencies
-   TestNG

### 5. Run Automation Tests

من مجلد `automation`:

``` bash
mvn clean test
```

> قد تحتاج إعدادات التشغيل وملف `testng.xml` إلى التعديل حسب إعدادات
> الفريق والـ Test Environment.

### 6. Open the Application

افتح الموقع التجريبي:

https://parabank.parasoft.com/

واستخدم بيانات اختبار مخصصة. لا تستخدم بيانات شخصية أو حسابات لا تملك
صلاحية اختبارها.

------------------------------------------------------------------------

## 📊 Final Deliverables \| التسليم النهائي

-   Project Test Plan.
-   Test Scenarios & Manual Test Cases.
-   Manual Execution Report.
-   Bug Reports & Evidence.
-   Static Review Findings.
-   Selenium Automation Framework.
-   TestNG Automation Reports.
-   Regression & Retesting Results.
-   Final Test Summary Report.
-   Final Project Presentation.

------------------------------------------------------------------------

## 👥 Our Team

**Digital Egypt Initiative -- Software Testing Graduation Project**

Built with teamwork, collaboration, and a shared commitment to software
quality.

### 🏦 ParaBank Testing Team

*Quality is never an accident; it is the result of organized testing and
teamwork.*

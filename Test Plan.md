Basic functionalities Test Plan for InterviewMe web application.
Prepared by: Mateusz Nowicki 09/09/2021

1. INTRODUCTION
The Test Plan has been created to explain the test approach to team members. It includes the objectives, scope, risks, resources and environment requirements.

1.1. OBJECTIVES
This Test Plan describes how to test basic functionalities for logged-in user on app.inverviewme.pl. It will be used as a manual during testing works for QA engineers, developers or project managers.

1.2. TEAM MEMEBERS
Mateusz Nowicki

2. SCOPE
2.1 Features to be tested:
Konto section and all features inside this section (https://app.interviewme.pl/dashboard/account)
Profil section and all features inside this section(https://app.interviewme.pl/dashboard/profile)
Ofert Pracy section and all features inside this section(https://app.interviewme.pl/dashboard/job-offers)

2.2 Features not to be tested (out-of-scope):
Log in and log out features.
Pulpit section (https://app.interviewme.pl/dashboard/main)
Plany section (https://app.interviewme.pl/dashboard/plans)
Kosz section (https://app.interviewme.pl/dashboard/trash)
Dokumenty section (https://app.interviewme.pl/dashboard/documents)

3. RISKS
There are no schedule or personnel risks. Because there are no specific requirements delivered to the QA engineer expected results in test cases may differ from actual expectations of the product owner. Thus a complexity of test cases may not be the best in terms of quality.

4. ENVIRONMENT
Tests will be performed on https://app.interviewme.pl/ website with testing credentials that are delivered.

5. TESTING STRATEGY
The following main testing types that will be performed:

Functional Testing
UI Testing
Testing types that will not be performed:

Compatibility Testing
Regression Testing
Security Testing
Load Testing
Stress Testing
Performance Testing
6. RESOURCES
Test cases - TestRail
Browser - Chrome 93.0.4577.63 (64-bit)
Screenshots - ShareX
Devices - Desktop / Windows 10 OS
7. BUGS REPORT
Bugs will be reported in JIRA. It will be helpful in determining causes of the errors and correcting them. Defects will be classified into four categories such as:

Critical/blocker
Major
Minor
Trivial Each bug report includes summary of the problem. location of the defect, steps to reproduce the error, frequency, severity and additional information if needed.
8. AUTOMATION TOOLS
Automation tools are not required for this project however QA engineer will select the most suitable test cases for future automation.

9. DELIVERABLES
Test Plan
Test cases
Bug reports

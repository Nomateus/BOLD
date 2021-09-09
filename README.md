# BOLD interview task
## Basic functionalities Test Plan for InterviewMe web application.
> Prepared by: Mateusz Nowicki
> 09/09/2021
### 1. INTRODUCTION
The Test Plan has been created to explain the test approach to team members. It includes the objectives, scope, risks, resources and environment requirements.

1.1. OBJECTIVES  
This Test Plan describes how to test basic functionalities for logged-in user on app.inverviewme.pl. It will be used as a manual during testing works for QA engineers, developers or project managers.  

1.2. TEAM MEMEBERS  
Mateusz Nowicki

### 2. SCOPE
2.1 Features to be tested:  
`Konto` section and all features inside this section (https://app.interviewme.pl/dashboard/account)  
`Profil` section and all features inside this section(https://app.interviewme.pl/dashboard/profile)  
`Ofert Pracy` section and all features inside this section(https://app.interviewme.pl/dashboard/job-offers)

2.2 Features not to be tested (out-of-scope):  
`Log in` and `log out` features.  
`Pulpit` section (https://app.interviewme.pl/dashboard/main)  
`Plany` section (https://app.interviewme.pl/dashboard/plans)  
`Kosz` section (https://app.interviewme.pl/dashboard/trash)  
`Dokumenty` section (https://app.interviewme.pl/dashboard/documents)  

### 3. RISKS

There are no schedule or personnel risks. Because there are no specific requirements delivered to the QA engineer expected results in test cases may differ from actual expectations of the product owner. Thus a complexity of test cases may not be the best in terms of quality.


### 4. ENVIRONMENT
Tests will be performed on https://app.interviewme.pl/ website with testing credentials that are delivered. 

### 5. TESTING STRATEGY
The following main testing types that will be performed:
* Functional Testing
* UI Testing  

Testing types that will not be performed:
* Compatibility Testing
* Regression Testing
* Security Testing
* Load Testing
* Stress Testing
* Performance Testing

### 6. RESOURCES
* Test cases - TestRail
* Browser - Chrome 93.0.4577.63 (64-bit)
* Screenshots - ShareX
* Devices - Desktop / Windows 10 OS 
### 7. BUGS REPORT  
Bugs will be reported in JIRA. It will be helpful in determining causes of the errors and correcting them. Defects will be classified into four categories such as: 
* Critical/blocker
* Major
* Minor
* Trivial 
Each bug report includes summary of the problem. location of the defect, steps to reproduce the error, frequency, severity and additional information if needed.  

### 8. AUTOMATION TOOLS
Automation tools are not required for this project however QA engineer will select the most suitable test cases for future automation.
### 9. DELIVERABLES
* Test Plan 
* Test cases 
* Bug reports


# TEST CASES

**ID**: TC.01  
**TITLE**: Verify that user can navigate to `Konto` section.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the home page https://app.interviewme.pl/dashboard/main  
**STEPS TO REPRODUCE**: 1. Users clicks `Konto` button on the left side menu.  
**EXPECTED RESULT**: User lands on https://app.interviewme.pl/dashboard/account page.  
**ACTUAL RESULT**: Users is navigated to https://app.interviewme.pl/dashboard/account page.  
**STATUS PASS/FAIL**: PASS    

**ID**: TC.02  
**TITLE**: Verify that user can click on `Pomoc` button in the top right corner.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users clicks `Pomoc` button in the top right corner of the page.
**EXPECTED RESULT**: User lands on https://pomoc2.interviewme.pl/pl/support/home.  
**ACTUAL RESULT**: Users is navigated to https://pomoc2.interviewme.pl/pl/support/home page.  
**STATUS PASS/FAIL**: PASS  

**ID**: TC.03  
**TITLE**: Verify that user can successfully send opinion using `Opinia` button that can be expanded.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users clicks `Opinia` button on the right side of the page.  
2. User chooses `Okropnie` answer by choosing first button from the left side.  
3. User types `Test` as an answer.  
4. User hovers over an icon in the bottom left side of the text box which should show `Zaznacz element na stronie` tooltip and clicks on the icon.
5. User marks `interviewme` logo in the top left corner of the page.  
6. User clicks `Wyślij` button.   
**EXPECTED RESULT**: `Dziękujemy za podzielenie się z nami swoją opinią!` tooltip is displayed.   
**ACTUAL RESULT**: `Dziękujemy za podzielenie się z nami swoją opinią!` tooltip is displayed.    
**STATUS PASS/FAIL**: PASS  

**ID**: TC.04  
**TITLE**: Verify that user can successfully close the `Opinia` feature after opening it.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users clicks `Opinia` button on the right side of the page.  
2. User clicks on `X` button in the top right corner of the `Opinia` feature to close the tab.    
**EXPECTED RESULT**: `Opinia` feature is successfully closed.  
**ACTUAL RESULT**: `Opinia` feature is successfully closed.   
**STATUS PASS/FAIL**: PASS  

(we could do the same test case for closing the `Zaznacz element na stronie` feature but I will skip it since this is not a basic functionality)


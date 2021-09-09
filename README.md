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

(I could do the same test case for closing the `Zaznacz element na stronie` feature but I will skip it since this is not a basic functionality)  

**ID**: TC.05  
**TITLE**: Verify that user can successfully change e-mail using `Zmień adres e-mail` button.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users clicks `Zmień adres e-mail` button on the center menu.  
2. User types `mateusztest@bold.com` as new e-mail in the text box.  
3. User clicks on red `Zmień adres e-mail` button.  
**EXPECTED RESULT**: `Świetnie! Zmieniłeś swój adres e-mail na mateusztest@bold.com` message is displayed.  
**ACTUAL RESULT**: `Świetnie! Zmieniłeś swój adres e-mail na mateusztest@bold.com` message is displayed.   
**STATUS PASS/FAIL**: PASS  

**ID**: TC.06  
**TITLE**: Verify that user can successfully close `Podaj nowy adres email` popup.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users clicks `Zmień adres e-mail` button on the center menu.  
2. User clicks `Anuluj` button undert the text box.  
3. User is navigated to the https://app.interviewme.pl/dashboard/account page.  
**EXPECTED RESULT**: `Konto` page is displayed and `Podaj nowy adres email` popup is closed.    
**ACTUAL RESULT**: `Konto` page is displayed and `Podaj nowy adres email` popup is closed.       
**STATUS PASS/FAIL**: PASS

**ID**: TC.07  
**TITLE**: Verify that user can't input invalid email format.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users clicks `Zmień adres e-mail` button on the center menu.  
2. User puts `testtest.pl` in the e-mail text box.      
**EXPECTED RESULT**: `Niepoprawny adres email` message is shown at the bottom and user can't use `Zmień adres e-mail button` successfully.  
**ACTUAL RESULT**: `Niepoprawny adres email` message is shown at the bottom and user can't use `Zmień adres e-mail` button successfully.    
**STATUS PASS/FAIL**: PASS  

**ID**: TC.08  
**TITLE**: Verify that user can reset the password.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users clicks `Zmień hasło` button on the center menu.  
2. User clicks `Zapomniałeś hasła?` button.  
3. User puts `mateusztest@bold.com` and clicks `Wyślij link do resetowania hasła` button.    
**EXPECTED RESULT**: Popup message titled `Wiadomość e-mail została wysłana` appears with basic information about actions taken and a tip.  
**ACTUAL RESULT**: Popup message titled `Wiadomość e-mail została wysłana` appears with basic information and tip.      
**STATUS PASS/FAIL**: PASS  

**ID**: TC.09  
**TITLE**: Verify that user can change the password.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users clicks `Zmień hasło` button on the center menu.  
2. User puts `Password1` in the `Nowe hasło` text box.  
3. User clicks `Zmień hasło` button.    
**EXPECTED RESULT**: Popup message titled `Twoje hasło zostało zmienione` appears with basic information about actions taken and a tip.  
**ACTUAL RESULT**: Popup message titled `Twoje hasło zostało zmienione` appears with basic information and tip.      
**STATUS PASS/FAIL**: PASS  

**ID**: TC.10  
**TITLE**: Verify that user meets the new password requirements when changing the password.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users clicks `Zmień hasło` button on the center menu.  
2. User puts `X` in the `Nowe hasło` text box.    
3. Text box is highlighted in red color and `Co najmniej 7 znaków` text appears.    
4. User deletes previous value and puts `QWERTYU`.    
5. Text box is highlighted in red color and `Pole musi zawierać przynajmniej jedną cyfrę` text appears.    
6. User deletes previous value and puts `QWERTYU1`.   
7. User click `Zmień hasło` button.         
**EXPECTED RESULT**: Popup message titled `Twoje hasło zostało zmienione` appears with basic information about actions taken and a tip.  
**ACTUAL RESULT**: Popup message titled `Twoje hasło zostało zmienione` appears with basic information and tip.      
**STATUS PASS/FAIL**: PASS  

**ID**: TC.11  
**TITLE**: Verify that user can successfully change and save `Komunikacja e-mail` settings.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users selects the first checkbox in `Komunikacja e-mail` section.  
2. User selects and unselects the second checbox in `Komunikacja e-mail` section.  
3. User clicks `Zapisz` button under checkboxes.
4. User refreshes the page using F5 keyboard button.  
**EXPECTED RESULT**: Loading spinner shows up and settings are saved. After user refreshed the page settings are still saved just like user selected during the tests.  
**ACTUAL RESULT**: New settings are saved.        
**STATUS PASS/FAIL**: PASS  

**ID**: TC.12 
**TITLE**: Verify that user can open `Regulamin` page.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users clicks `Regulamin` button.  
**EXPECTED RESULT**: User is redirected to https://interviewme.pl/regulamin page.  
**ACTUAL RESULT**: User is redirected to https://interviewme.pl/regulamin page.    
**STATUS PASS/FAIL**: PASS  

**ID**: TC.13 
**TITLE**: Verify that user can open `Polityka prywatności` page.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users clicks `Polityka prywatności` button.  
**EXPECTED RESULT**: User is redirected to https://app.interviewme.pl/dashboard/account/privacy-policy page.  
**ACTUAL RESULT**: User is redirected to https://app.interviewme.pl/dashboard/account/privacy-policy page.    
**STATUS PASS/FAIL**: PASS  

**ID**: TC.14 
**TITLE**: Verify that user can open `Pełna wersja polityki prywatności` inside `Polityka prywatności` page.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users clicks `Polityka prywatności` button.    
2. User scrolls down to the bottom of the page and clicks `Pełna wersja polityki prywatności` link.  
**EXPECTED RESULT**: User is redirected to https://interviewme.pl/polityka-prywatnosci page.  
**ACTUAL RESULT**: User is redirected to https://interviewme.pl/polityka-prywatnosci page.    
**STATUS PASS/FAIL**: PASS  

**ID**: TC.15 
**TITLE**: Verify that user can delete the account using specific link inside `Polityka prywatności` page.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users clicks `Polityka prywatności` button.      
2. User scrolls down until user sees blue link `usuwając konto z serwisu` and clicks it.      
3. Users selects two checkboxes and clicks `Usuń konto` button.    
**EXPECTED RESULT**: (I didn't clickecd on `Usuń konto` because if this actually works I won't be able to use this account and continue to write test cases.)   
**ACTUAL RESULT**:  (I didn't clickecd on `Usuń konto` because if this actually works I won't be able to use this account and continue to write test cases.)     
**STATUS PASS/FAIL**: ?   

**ID**: TC.16 
**TITLE**: Verify that user can unselect the `Zapoznałem/am się i akceptuję Regulamin i Politykę prywatności`.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users unselects the `Zapoznałem/am się i akceptuję Regulamin i Politykę prywatności` checkbox.        
**EXPECTED RESULT**: Checkbox is unselected.       
**ACTUAL RESULT**: User is presented with a new popup that let him delete the account.        
**STATUS PASS/FAIL**: FAIL   

**ID**: TC.17 
**TITLE**: Verify that user can download his personal data using `Pobierz moje dane` button.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. Users clicks the `Pobierz moje dane` button at the bottom of the page.          
**EXPECTED RESULT**: Popup message titled `Eksport Twoich danych jest już w toku` with loading spinner is displayed and data is sent to the user's email address.         
**ACTUAL RESULT**: Popup message titled `Eksport Twoich danych jest już w toku` with loading spinner is displayed.          
**STATUS PASS/FAIL**: FAIL   

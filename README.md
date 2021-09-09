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
**STEPS TO REPRODUCE**: 1. User clicks `Konto` button on the left side menu.  
**EXPECTED RESULT**: User lands on https://app.interviewme.pl/dashboard/account page.  
**ACTUAL RESULT**: User is navigated to https://app.interviewme.pl/dashboard/account page.  
**STATUS PASS/FAIL**: PASS    

**ID**: TC.02  
**TITLE**: Verify that user can click on `Pomoc` button in the top right corner.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. User clicks `Pomoc` button in the top right corner of the page.
**EXPECTED RESULT**: User lands on https://pomoc2.interviewme.pl/pl/support/home.  
**ACTUAL RESULT**: User is navigated to https://pomoc2.interviewme.pl/pl/support/home page.  
**STATUS PASS/FAIL**: PASS  

**ID**: TC.03  
**TITLE**: Verify that user can successfully send opinion using `Opinia` button that can be expanded.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. User clicks `Opinia` button on the right side of the page.  
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
**STEPS TO REPRODUCE**: 1. User clicks `Opinia` button on the right side of the page.  
2. User clicks on `X` button in the top right corner of the `Opinia` feature to close the tab.    
**EXPECTED RESULT**: `Opinia` feature is successfully closed.  
**ACTUAL RESULT**: `Opinia` feature is successfully closed.   
**STATUS PASS/FAIL**: PASS  

(I could do the same test case for closing the `Zaznacz element na stronie` feature but I will skip it since this is not a basic functionality)  

**ID**: TC.05  
**TITLE**: Verify that user can successfully change e-mail using `Zmień adres e-mail` button.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. User clicks `Zmień adres e-mail` button on the center menu.  
2. User types `mateusztest@bold.com` as new e-mail in the text box.  
3. User clicks on red `Zmień adres e-mail` button.  
**EXPECTED RESULT**: `Świetnie! Zmieniłeś swój adres e-mail na mateusztest@bold.com` message is displayed.  
**ACTUAL RESULT**: `Świetnie! Zmieniłeś swój adres e-mail na mateusztest@bold.com` message is displayed.   
**STATUS PASS/FAIL**: PASS  

**ID**: TC.06  
**TITLE**: Verify that user can successfully close `Podaj nowy adres email` popup.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. User clicks `Zmień adres e-mail` button on the center menu.  
2. User clicks `Anuluj` button undert the text box.  
3. User is navigated to the https://app.interviewme.pl/dashboard/account page.  
**EXPECTED RESULT**: `Konto` page is displayed and `Podaj nowy adres email` popup is closed.    
**ACTUAL RESULT**: `Konto` page is displayed and `Podaj nowy adres email` popup is closed.       
**STATUS PASS/FAIL**: PASS

**ID**: TC.07  
**TITLE**: Verify that user can't input invalid email format.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. User clicks `Zmień adres e-mail` button on the center menu.  
2. User puts `testtest.pl` in the e-mail text box.      
**EXPECTED RESULT**: `Niepoprawny adres email` message is shown at the bottom and user can't use `Zmień adres e-mail button` successfully.  
**ACTUAL RESULT**: `Niepoprawny adres email` message is shown at the bottom and user can't use `Zmień adres e-mail` button successfully.    
**STATUS PASS/FAIL**: PASS  

**ID**: TC.08  
**TITLE**: Verify that user can reset the password.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. User clicks `Zmień hasło` button on the center menu.  
2. User clicks `Zapomniałeś hasła?` button.  
3. User puts `mateusztest@bold.com` and clicks `Wyślij link do resetowania hasła` button.    
**EXPECTED RESULT**: Popup message titled `Wiadomość e-mail została wysłana` appears with basic information about actions taken and a tip.  
**ACTUAL RESULT**: Popup message titled `Wiadomość e-mail została wysłana` appears with basic information and tip.      
**STATUS PASS/FAIL**: PASS  

**ID**: TC.09  
**TITLE**: Verify that user can change the password.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. User clicks `Zmień hasło` button on the center menu.  
2. User puts `Password1` in the `Nowe hasło` text box.  
3. User clicks `Zmień hasło` button.    
**EXPECTED RESULT**: Popup message titled `Twoje hasło zostało zmienione` appears with basic information about actions taken and a tip.  
**ACTUAL RESULT**: Popup message titled `Twoje hasło zostało zmienione` appears with basic information and tip.      
**STATUS PASS/FAIL**: PASS  

**ID**: TC.10  
**TITLE**: Verify that user meets the new password requirements when changing the password.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. User clicks `Zmień hasło` button on the center menu.  
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
**STEPS TO REPRODUCE**: 1. User selects the first checkbox in `Komunikacja e-mail` section.  
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
**STEPS TO REPRODUCE**: 1. User clicks `Regulamin` button.  
**EXPECTED RESULT**: User is redirected to https://interviewme.pl/regulamin page.  
**ACTUAL RESULT**: User is redirected to https://interviewme.pl/regulamin page.    
**STATUS PASS/FAIL**: PASS  

**ID**: TC.13 
**TITLE**: Verify that user can open `Polityka prywatności` page.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. User clicks `Polityka prywatności` button.  
**EXPECTED RESULT**: User is redirected to https://app.interviewme.pl/dashboard/account/privacy-policy page.  
**ACTUAL RESULT**: User is redirected to https://app.interviewme.pl/dashboard/account/privacy-policy page.    
**STATUS PASS/FAIL**: PASS  

**ID**: TC.14 
**TITLE**: Verify that user can open `Pełna wersja polityki prywatności` inside `Polityka prywatności` page.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. User clicks `Polityka prywatności` button.    
2. User scrolls down to the bottom of the page and clicks `Pełna wersja polityki prywatności` link.  
**EXPECTED RESULT**: User is redirected to https://interviewme.pl/polityka-prywatnosci page.  
**ACTUAL RESULT**: User is redirected to https://interviewme.pl/polityka-prywatnosci page.    
**STATUS PASS/FAIL**: PASS  

**ID**: TC.15 
**TITLE**: Verify that user can delete the account using specific link inside `Polityka prywatności` page.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. User clicks `Polityka prywatności` button.      
2. User scrolls down until user sees blue link `usuwając konto z serwisu` and clicks it.      
3. User selects two checkboxes and clicks `Usuń konto` button.    
**EXPECTED RESULT**: (I didn't clickecd on `Usuń konto` because if this actually works I won't be able to use this account and continue to write test cases.)   
**ACTUAL RESULT**:  (I didn't clickecd on `Usuń konto` because if this actually works I won't be able to use this account and continue to write test cases.)     
**STATUS PASS/FAIL**: ?   

**ID**: TC.16 
**TITLE**: Verify that user can unselect the `Zapoznałem/am się i akceptuję Regulamin i Politykę prywatności`.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. User unselects the `Zapoznałem/am się i akceptuję Regulamin i Politykę prywatności` checkbox.        
**EXPECTED RESULT**: Checkbox is unselected.       
**ACTUAL RESULT**: User is presented with a new popup that let him delete the account.          
**STATUS PASS/FAIL**: FAIL   

**ID**: TC.17 
**TITLE**: Verify that user can download his personal data using `Pobierz moje dane` button.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the https://app.interviewme.pl/dashboard/account page.  
**STEPS TO REPRODUCE**: 1. User clicks the `Pobierz moje dane` button at the bottom of the page.          
**EXPECTED RESULT**: Popup message titled `Eksport Twoich danych jest już w toku` with loading spinner is displayed and data is sent to the user's email address.         
**ACTUAL RESULT**: Popup message titled `Eksport Twoich danych jest już w toku` with loading spinner is displayed but nothing happens after few minutes. Data is not sent successfully.                
**STATUS PASS/FAIL**: FAIL  

**ID**: TC.18  
**TITLE**: Verify that user can navigate to `Profil` section.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the home page https://app.interviewme.pl/dashboard/main  
**STEPS TO REPRODUCE**: 1. User clicks `Profil` button on the left side menu.  
**EXPECTED RESULT**: User lands on https://app.interviewme.pl/dashboard/profile page.  
**ACTUAL RESULT**: User is navigated to https://app.interviewme.pl/dashboard/profile page.    
**STATUS PASS/FAIL**: PASS    

**ID**: TC.19  
**TITLE**: Verify that user can edit and save the `Dane osobowe` section.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the home page https://app.interviewme.pl/dashboard/main  
**STEPS TO REPRODUCE**: 1. User clicks `Edytuj dane osobowe` button.  
2. User puts `Mateusz` value in `Imię` section, `Nowicki` value in `Nazwisko` section.  
3. User chooses `Mężczyzna` value from the dropdown list in `Płeć` section.  
4. User clicks `Zapisz` button at the bottom of the page.
**EXPECTED RESULT**: New data is saved and popup with `Twoje dane zostały pomyślnie zapisane` is displayed.  
**ACTUAL RESULT**: `Problem z wysłaniem formularza` error is displayed. Data is not saved and user needs to leave.  
**STATUS PASS/FAIL**: FAIL    

**ID**: TC.20  
**TITLE**: Verify that user can edit and save the `Doświadczenie zawodowe` section.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the home page https://app.interviewme.pl/dashboard/main  
**STEPS TO REPRODUCE**: 1. User clicks `Edytuj doświadczenie zawodowe` button at the bottom of the page.  
2. User puts `QA` value in `Aktualny zawód` section, `Senior` value in `Aktualny poziom zawodowy` section.    
3. User deletes the previously saved value in `Wykształcenie` section.    
4. User clicks `Zapisz` button at the bottom of the page.  
**EXPECTED RESULT**: New data is saved and displayed under `Doświadczenie zawodowe` section.    
**ACTUAL RESULT**: Screen with newly saved data is displayed with correct data.    
**STATUS PASS/FAIL**: PASS   

**ID**: TC.21  
**TITLE**: Verify that user can navigate to `Oferty pracy` section.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the home page https://app.interviewme.pl/dashboard/main  
**STEPS TO REPRODUCE**: 1. User clicks `Oferty pracy` button on the left side menu.  
**EXPECTED RESULT**: User lands on https://app.interviewme.pl/dashboard/job-offers page.  
**ACTUAL RESULT**: User is navigated to https://app.interviewme.pl/dashboard/job-offers page.    
**STATUS PASS/FAIL**: PASS   

**ID**: TC.21  
**TITLE**: Verify that user can navigate to `Oferty pracy` section.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the home page https://app.interviewme.pl/dashboard/main  
**STEPS TO REPRODUCE**: 1. User clicks `Oferty pracy` button on the left side menu.  
**EXPECTED RESULT**: User lands on https://app.interviewme.pl/dashboard/job-offers page.  
**ACTUAL RESULT**: User is navigated to https://app.interviewme.pl/dashboard/job-offers page.    
**STATUS PASS/FAIL**: PASS   

**ID**: TC.22  
**TITLE**: Verify that clicking `Search` button without any additional input changes nothing.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the home page https://app.interviewme.pl/dashboard/main  
**STEPS TO REPRODUCE**: 1. User clicks `Search` button in the top right corner.    
**EXPECTED RESULT**: Page refreshes without showing any specific results.   
**ACTUAL RESULT**: No changes on the `Oferty pracy` page.    
**STATUS PASS/FAIL**: PASS   

**ID**: TC.23 
**TITLE**: Verify that user can search for a specific `Stanowisko`.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the home page https://app.interviewme.pl/dashboard/main  
**STEPS TO REPRODUCE**: 1. User inputs `tapeciarz` value in `Stanowisko` field.    
2. User clicks `Szukaj` button.  
**EXPECTED RESULT**: Page shows only results that includes value `Tapeciarz`.  
**ACTUAL RESULT**: Just one specific result is shown on the page.  
**STATUS PASS/FAIL**: PASS   

**ID**: TC.23 
**TITLE**: Verify that user can search for a specific `Lokalizacja`.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the home page https://app.interviewme.pl/dashboard/main  
**STEPS TO REPRODUCE**: 1. User inputs `Sopot` value in `Lokalizacja` field.  
2. User clicks `Szukaj` button.  
**EXPECTED RESULT**: Page shows only results that includes value `Sopot`.    
**ACTUAL RESULT**: Only results with `Sopot` as `Lokalizacja` are shown on the page.  
**STATUS PASS/FAIL**: PASS   

**ID**: TC.23 
**TITLE**: Verify that user can open any offer.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the home page https://app.interviewme.pl/dashboard/main  
**STEPS TO REPRODUCE**: 1. User clicks `Oferty pracy` button on the left side menu.    
2. User clicks any visible offer on the `Oferty pracy` page.  
**EXPECTED RESULT**: User is successfully redirected to external page with an offer.        
**ACTUAL RESULT**: Successfully redirected to an external page with an offer.    
**STATUS PASS/FAIL**: PASS   

**ID**: TC.24 
**TITLE**: Verify that user can search for any offer using `Enter` key instead of `Search` button.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the home page https://app.interviewme.pl/dashboard/main  
**STEPS TO REPRODUCE**: 1. User clicks `Oferty pracy` button on the left side menu.    
2. User inputs `Developer` in `Stanowisko` field.  
3. User clicks `Enter` button on keyboard.    
**EXPECTED RESULT**: Result pages with `Developer` value in `Stanowisko` are successfully displayed.          
**ACTUAL RESULT**: Results are shown correctly with `Developer` value in `Stanowisko` are successfully displayed.     
**STATUS PASS/FAIL**: PASS    

**ID**: TC.24 
**TITLE**: Verify that inputting incorrect value will not display any offers.  
**PRE-CONDITIONS**: User is logged in with following credentials: `vincent-sqa+rekrutacja@bold.com` / `parmezan6`  
User is on the home page https://app.interviewme.pl/dashboard/main  
**STEPS TO REPRODUCE**: 1. User clicks `Oferty pracy` button on the left side menu.      
2. User inputs `XYZ` in `Stanowisko` field.    
3. User clicks `Szukaj` button in top right corner.      
**EXPECTED RESULT**: `Brak ofert - zmień kryteria wyszukiania` message is shown with no results.            
**ACTUAL RESULT**: No results are shown and correct message is shown.       
**STATUS PASS/FAIL**: PASS    

I could really add many more test cases but I will end now since I feel you will know how I work by now. Alhough I have to say that writing test cases in some other tools is easier than in Github so pelase keep that in mind during review.    

When it comes to selecting test cases that could be automated we should aim to automate only these types of test cases that:   
* will be repeated often   
* that are changed by developers very seldom  
* that are time consuming (it saves as a lot of time)    
* there is low risk  

By any means I'm not an expert in automation tests but I would automate following test cases:  
* TC.05  
* TC.07  
* TC.08  
* TC.09  
* TC.10  
* TC.17   

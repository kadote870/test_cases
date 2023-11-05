# Task for develop new functionallity

## When a user signs up for the newsletter, receives a one-time 5% discount code to use in web store.

1. User registers for the newsletter
2. After registration, system automatically sent to users email adress message with 5% discount
3. Discount code is assigned to particular user
4. Discount code is one-time only
5. Discount code covers value of entire order in cart (5%)
6. Discount code deactivated after payment is processed by web shop system
7. Generated discount code is stored in data base and include information:
   * id
   * discount code
   * generated date
   * user
   * used (yes/no)
   * used date
   * order number
8. In web shop admin panel, admin can on/off "newsletter discount" mechanism manually, or automatically after a certain
   period of time
9. When "newsletter discount" mechanism OFF, still can use disount code

# Bug reports

| Parameter          | Content                                                                                                                                                                               |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|	
| Title              | User is able to login into webapp using old password                                                                                                                                  |
| Priority           | 	(set by Product Owner)                                                                                                                                                               |
| Severity	          | Critical                                                                                                                                                                              |
| Browser	           | Google Chrome ; Firefox ; Microsoft Edge ; Safari                                                                                                                                     |
| Environment        | 	http://www.example-url-adress-test-env.com/login-page                                                                                                                                |
| Branch	            | test-branch-software                                                                                                                                                                  |
| Issue location     | 	http://www.example-url-adress-test-env.com/login-page                                                                                                                                |
| PRECONDITIONS	     | 1.	Standard user account<br/><p>1.1 email: example@email.com<br/>1.2 old password: Old#Password123<br/>1.3 new password: New#Password123*<br/><p>2.User already changed password once |
| STEPS TO REPRODUCE | 1.	Go to login page http://www.example-url-adress-test-env.com/login-page <br/>2. Login in to web app using old password                                                              |
| ACTUAL RESULTS     | User is able login into webapp using old password                                                                                                                                     |
| EXPECTED RESULTS   | 1. User is  NOT able login into webapp using old password<br/>2. „Incorrect username or password” message is displayed                                                                |
| COMMENTS           | none                                                                                                                                                                                  |      	1.	

| Parameter          | Content                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|	
| Title              | At web shop cart section user is able to increase quantity more than real product stock                                                                                                                                                                                                                                                                                                                                                                                         |
| Priority           | 	(set by Product Owner)                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Severity	          | Critical                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Browser	           | Google Chrome ; Firefox ; Microsoft Edge ; Safari                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Environment        | 	http://www.web-shop-test-env.com                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Branch	            | product-page-new-feature                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Issue location     | 	http://www.example-url-adress-test-env.com/login-page                                                                                                                                                                                                                                                                                                                                                                                                                          |
| PRECONDITIONS	     | 1.	Example-product-001 quantity = 2                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| STEPS TO REPRODUCE | 1. Login in to buyer account<br/>2. Go to product page http://www.web-shop-test-env.com/example-product-001<br/>3. Add item in to cart – effect: cart qty = 1<br/>4. Add item in to cart second time – effect: cart qty = 2<br/>5. Add item in to cart third time – effect: system display message "No products in stock" ; cart qty = 2<br/>6. Display cart page to proceed to checkout and payment<br/>7. At cart page increase example-product-001 quantity using „+” button | 
| ACTUAL RESULTS     | 1. message  "No products in stock" was NOT displayed<br/>2. example-product-001 quantity was increased to 3<br/> 3. total order amount was increased                                                                                                                                                                                                                                                                                                                            |
| EXPECTED RESULTS   | 1. message  "No products in stock"  was displayed<br/>2. example-product-001 quantity = 2                                                                                                                                                                                                                                                                                                                                                                                       |
| COMMENTS           | none                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |      	1.	

# Web app login test cases

| Parameter       | Content                                                                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID              | 1                                                                                                                                                                                                                                |
| Name            | Login page have correct design (according to UX docummentation)                                                                                                                                                                  |
| Preconditions   | 1. Web browsers Google Chrome ; Firefox ; Microsoft Edge ; Safari                                                                                                                                                                |
| Steps           | 1. Using web browsers mentionend in precondition check login page design                                                                                                                                                         |
| Expected Result | 1. Login page have correct design (according to UX docummentation)<br>2. All elements are displayed correctly<br>3. All desciriptions are correct<br>4. All tooltips are displaying correctly, and included correct informations |

| Parameter       | Content                                                                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID              | 2                                                                                                                                                                                                                                |
| Name            | Login page layout is responsive depending on the window size (RWD)                                                                                                                                                               |
| Preconditions   | 1. Chrome DevTools or Blisk web browser                                                                                                                                                                                          |
| Steps           | 1. Open webapp login page<br>2. Change window resolution<br>3. Using Chrome DevTools or Blisk web browser check how GUI looks on other devices (tablets, smartphonest etc. etc.) (according to BI report – most popular devices) |
| Expected Result | 1. All GUI elements looks correctly<br>2. When user resize window (or display it on other device) all GUI elements looks correctly, change size or place (according to UX documentation)                                         |

| Parameter       | Content                                                                                                                                                                                                                                                                                                    |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID              | 3                                                                                                                                                                                                                                                                                                          |
| Name            | User can navigate on login page using keyboard button „Tab”, and accept login details using „Enter” button                                                                                                                                                                                                 |
| Preconditions   | 1. Standard user credentials                                                                                                                                                                                                                                                                               |
| Steps           | 1. Go to login input field<br><br>2. Provide users email<br>3. press „TAB” button on keyboard – coursor are changed place to password input field<br>4. Provide users password<br>5. press tab – Login button are market<br>6. press „ENTER” button on keyboard<br>7. User is logged in to web application |
| Expected Result | 1. All steps performed correctly                                                                                                                                                                                                                                                                           |

| Parameter       | Content                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| ID              | 4                                                                                                                                       |
| Name            | The appearance of the mouse cursor depends on where it is placed (buttons, input fields etc.)                                           |
| Preconditions   | none                                                                                                                                    |
| Steps           | 1. Move mouse coursor to: password input field<br>2. Move mouse coursor to: email input field<br>3. Move mouse coursor to: Login button |
| Expected Result | 1. Standard coursor is displayed correctly<br>2. „Hand” coursor is displayed correctly<br>3. I-beam pointer is displayed correctly      |

| Parameter       | Content                                                            |
|-----------------|--------------------------------------------------------------------|
| ID              | 5                                                                  |
| Name            | User can login with success                                        |
| Preconditions   | 1. Standard user credentials                                       |
| Steps           | 1. Provide user credentials - email and password<br>2. Click login |
| Expected Result | 1. User is logged in to webapp                                     |

| Parameter       | Content                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID              | 6                                                                                                                                                                                                                                                                                       |
| Name            | User can not login - „Incorrect username or password”                                                                                                                                                                                                                                   |
| Preconditions   | 1. Standard user credentials                                                                                                                                                                                                                                                            |
| Steps           | 1. Provide user credentials – email (WITH TYPO) and correct password<br/>2. User can not login – message „Incorrect username or password”<br/>3. Provide user credentials – correct email and password (WITH TYPO)<br/>4. User can not login – message „Incorrect username or password” |
| Expected Result | 1. All steps performed correctly                                                                                                                                                                                                                                                        |

| Parameter       | Content                                                                                                                                                                                                                                                                |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID              | 7                                                                                                                                                                                                                                                                      |
| Name            | When user provide random text in to login input field, message "Please enter a valid email address" is displayed                                                                                                                                                       |
| Preconditions   | 1. None                                                                                                                                                                                                                                                                |
| Steps           | 1. in to login input field provide text<br/><p> 1.1 random@emailcom <br/>1.2. randomemail.com><p><br/>2. "Please enter a valid email address" is displayed<br/>3. in to login input field provide correct email adres: random@email.com<br/>4. no message is displayed |
| Expected Result | 1. All steps performed correctly                                                                                                                                                                                                                                       |

| Parameter       | Content                                                                                                                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID              | 8                                                                                                                                                                                                                                                                                  |
| Name            | User can not login - „Empty field”                                                                                                                                                                                                                                                 |
| Preconditions   | 1. Standard user credentials                                                                                                                                                                                                                                                       |
| Steps           | 1. Provide user credentials – incorrect email and correct password<br>2. User can not login – message „Incorrect username or password”<br>3. Provide user credentials – correct email and password (WITH TYPO)<br>4. User can not login – message „Incorrect username or password” |
| Expected Result | 1. All steps performed correctly                                                                                                                                                                                                                                                   |



| Parameter       | Content                                                                                                |
|-----------------|--------------------------------------------------------------------------------------------------------|
| ID              | 9                                                                                                      |
| Name            | If user cannot login into web app (incorrect email or password) "Reset password" button are displayed. |
| Preconditions   | 1. Standard user credentials<br/>2. Test-case id 8 performed correctly                                 |
| Steps           | 1. Test-case id 8 steps performed correctly                                                            |
| Expected Result | 1. When user provide wrong credential, "Reset password" button are displayed                           |

| Parameter       | Content                                                                                                                                  |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| ID              | 10                                                                                                                                       |
| Name            | If the application support both login solutions user-login/password and email/password - user can login in to web app using both method. |
| Preconditions   | 1. Standard user credentials (user-login , email, password)                                                                              |
| Steps           | 1. As a user login into web app using email and password<br>2. Log off<br>3. As a user login into web app using user-login and password  |
| Expected Result | 1. Wser can login in to web app using both method - user-login/password and email/password                                               |


| Parameter       | Content                                                                                                                              |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| ID              | 11                                                                                                                                   |
| Name            | If the application support one account with two different email address, user can login into account using both email address.       |
| Preconditions   | 1. Standard user credentials (email1 , email2, password)                                                                             |
| Steps           | 1. As a user login into web app using email1 and password<br>2. Log off<br>3. As a user login into web app using email2 and password |
| Expected Result | 1. User can login into web app using two different email address.                                                                    |

| Parameter       | Content                                                |
|-----------------|--------------------------------------------------------|
| ID              | 12                                                     |
| Name            | After login user is redirected to main page of web app |
| Preconditions   | 1. Standard user credentials                           |
| Steps 1.        | As a user login into webapp                            |
| Expected Result | 1. user is redirected to main page of web app          |


| Parameter       | Content                                                      |
|-----------------|--------------------------------------------------------------|
| ID              | 13                                                           |
| Name            | When user unlogg from account is redirected to login page    |
| Preconditions   | 1. Standard user credentials                                 |
| Steps           | 1. As a user login into webapp<br>2. unlogg user             |
| Expected Result | 1. When user unlogg from account is redirected to login page |

   | Parameter       | Content                                                                                                                  |
   |-----------------|--------------------------------------------------------------------------------------------------------------------------|
   | ID              | 14                                                                                                                       |
   | Name            | When logged user enter URL address of the login page is automatically redirected to the home page of the web application |
   | Preconditions   | 1. User is already logged into web app                                                                                   |
   | Steps           | 1. Go to login page                                                                                                      |
   | Expected Result | 1. Login page automatically redirect to main page                                                                        |

   | Parameter       | Content                                                                                                  |
   |-----------------|----------------------------------------------------------------------------------------------------------|
   | ID              | 15                                                                                                       |
   | Name            | When logged user refresh site is not unlogged                                                            |
   | Preconditions   | 1. User is already logged into web app                                                                   |
   | Steps           | 1. Press „refresh” button in web browser<br>2. Press „F5” on keyboard<br>3. Press „SHIFT+F5” on keyboard |
   | Expected Result | 1. When logged user refresh site is not unlogged                                                         |

   | Parameter       | Content                                                                                     |
   |-----------------|---------------------------------------------------------------------------------------------|
   | ID              | 16                                                                                          |
   | Name            | When logged user click web browser button "Forward", user is not unlogged                   |
   | Preconditions   | 1. Standard user credentials                                                                |
   | Steps           | 1. Login into web app using correct credentials<br>2. Press „Forward” button in web browser |
   | Expected Result | 1. User is not unlogged                                                                     |

   | Parameter       | Content                                                                       |
   |-----------------|-------------------------------------------------------------------------------|
   | ID              | 17                                                                            |
   | Name            | When user close all windows with web app is not unlogged                      |
   | Preconditions   | 1. User is already logged into web app                                        |
   | Steps           | 1. Close all windows of web application<br>2. Open login page                 |
   | Expected Result | 1. User is not unlogged<br>2. User is redirected from login page to main page |

   | Parameter       | Content                                                                                                                                                                                                                                                                                                              |
   |-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | ID              | 18                                                                                                                                                                                                                                                                                                                   |
   | Name            | When user shut down web browser, user is not unlogged                                                                                                                                                                                                                                                                |
   | Preconditions   | 1. Standard user credentials<br>2. During shutdown process web browser is NOT automatically erase cookies                                                                                                                                                                                                            |
   | Steps           | 1. Login into web app using correct credentials.<br>2. Perform any action (ex. change view from main page to subpage)<br>3. Shutdown web browser<br>4. Start web browser                                                                                                                                             |
   | Expected Result | 1. If web browser after start automatically open closed tabs, user can perform any action (ex. change view from main page to subpage) and is NOT redirected to login page<br>2. If web browser after start automatically NOT open closed tabs, and user open login page is automatically is redirected to main page. |

   | Parameter       | Content                                                                                                                                                                                                   |
   |-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | ID              | 19                                                                                                                                                                                                        |
   | Name            | If user unlogg from web app, cannot perform any action on other open web app tabs                                                                                                                         |
   | Preconditions   | 1. Standard user credentials                                                                                                                                                                              |
   | Steps           | 1. Login into web app using correct credentials<br>2. Open any sub page in new tab<br>3. unlogg user (user is redirect to login page)<br>4. go to second tab with opened web app<br>5. perform any action |
   | Expected Result | 1. When user try to perform any action is automatically redirected to login page                                                                                                                          |

   | Parameter       | Content                                                                                                                                                                                                                                             |
   |-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | ID              | 20                                                                                                                                                                                                                                                  |
   | Name            | After erase cookies, when user perform any action on the web app is automatically redirect to login page                                                                                                                                            |
   | Preconditions   | 1. Standard user credentials<br>2. web browser extension to modify cookies<br> Steps 1. Login into web app using correct credentials (user is redirect to main page)<br>2. web browser extension erase web app cookies<br>3. try perform any action |
   | Expected Result | 1. After erase cookies, when user try to perform any action is redirect to login page                                                                                                                                                               |

   | Parameter       | Content                                                                                                                                                 |
   |-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
   | ID              | 21                                                                                                                                                      |
   | Name            | After modify cookies, when user perform any action on the web app is automatically redirect to login page                                               |
   | Preconditions   | 1. Standard user credentials<br>2. web browser extension to modify cookies<br>                                                                          |
   | Steps 1.        | Login into web app using correct credentials (user is redirect to main page)2. web browser extension erase web app cookies<br>3. try perform any action |
   | Expected Result | 1. After modify cookies, when user try to perform any action is redirect to login page                                                                  |

   | Parameter       | Content                                                                                            |
   |-----------------|----------------------------------------------------------------------------------------------------|
   | ID              | 22                                                                                                 |
   | Name            | User can login in to web app using web browsers: Google Chrome ; Firefox ; Microsoft Edge ; Safari |
   | Preconditions   | 1. Standard user credentials                                                                       |
   | Steps           | 1. As a user login in to web app using browsers: Google Chrome ; Firefox ; Microsoft Edge ; Safari |
   | Expected Result | 1. User can login into web app using browsers: Google Chrome ; Firefox ; Microsoft Edge ; Safari   |

   | Parameter       | Content                                                                    |
   |-----------------|----------------------------------------------------------------------------|
   | ID              | 23                                                                         |
   | Name            | Password hiding and revealing function works correctly                     |
   | Preconditions   | 1. none                                                                    |
   | Steps           | 1. At login page provide password<br> 2. press „show/hide password” button |
   | Expected Result | 1. User can display password                                               |

   | Parameter       | Content                                                                    |
   |-----------------|----------------------------------------------------------------------------|
   | ID              | 24                                                                         |
   | Name            | When password is hide user can not copy it.                                |
   | Preconditions   | 1. none                                                                    |
   | Steps           | 1. At login page provide password                                          |
   | Expected Result | 1. User can not copy password and paste in to somewhere else (ex. notepad) |

   | Parameter       | Content                                    |
   |-----------------|--------------------------------------------|
   | ID              | 25                                         |
   | Name            | Button "create account" works correctly    |
   | Preconditions   | 1. None                                    |
   | Steps           | 1. As a user press "create account" button |
   | Expected Result | 1. User is redirect to register page       |

   | Parameter       | Content                                                                                                                        |
   |-----------------|--------------------------------------------------------------------------------------------------------------------------------|
   | ID              | 26                                                                                                                             |
   | Name            | When user provided incorrect password during login process, system automatically send email to user about failed login attempt |
   | Preconditions   | 1. Standard user credentials                                                                                                   |
   | Steps           | 1. Login into web app using credentials with typo in password<br>2. Check user private email                                   |
   | Expected Result | 1. User recieved email message about failed login attempt                                                                      |

   | Parameter       | Content                                                                                                     |
   |-----------------|-------------------------------------------------------------------------------------------------------------|
   | ID              | 27                                                                                                          |
   | Name            | When user perform failed login attempt X times, system block login page (by ip address) for X minutes/hours |
   | Preconditions   | 1. None                                                                                                     |
   | Steps           | 1. Try to login using wrong cedentials X times                                                              |
   | Expected Result | 1. System block login page (by ip address) for X minutes/hours                                              |

   | Parameter       | Content                                                                                                                                                                                                       |
   |-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | ID              | 28                                                                                                                                                                                                            |
   | Name            | When user not accepted registration token and try to login, "resend token" button is displayed                                                                                                                |
   | Preconditions   | 1. Standard user credentials<br>2. User not accepted registration token during registration process<br>                                                                                                       |
   | Steps           | 1. Try to login into web app                                                                                                                                                                                  |
   | Expected Result | 1. When user try to login into web app "resend token" button is displayed<br>2. "resend token" button works correctly<br>3. first registration token is inactive<br>4. new registration token works correctly |

   | Parameter       | Content                                                                                              |
   |-----------------|------------------------------------------------------------------------------------------------------|
   | ID              | 29                                                                                                   |
   | Name            | User can not login in to web app using old password                                                  |
   | Preconditions   | 1. Standard user credentials<br>2. User changed password                                             |
   | Steps           | 1. Try to login in to web app using old password<br>2. Try to login in to web app using new password |
   | Expected Result | 1. User can not login in to web app using old password                                               |

   | Parameter       | Content                                                                                                                         |
   |-----------------|---------------------------------------------------------------------------------------------------------------------------------|
   | ID              | 30                                                                                                                              |
   | Name            | After login in to web app session is automaticly expired after X minutes/hours                                                  |
   | Preconditions   | 1. Standard user credentials                                                                                                    |
   | Steps           | 1. login into web app<br>2. wait X minutes/hours<br>3. try to perform any action                                                |
   | Expected Result | 1. After X minutes/hours user is automatically logged-out<br>2. when user try to perform any action is redirected to login page |

   | Parameter       | Content                                                                                                                                       |
   |-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
   | ID              | 31                                                                                                                                            |
   | Name            | When user account is banned user can NOT login in to web app and specific information are displayed.                                          |
   | Preconditions   | 1. Standard user credentials<br>2. User have banned account                                                                                   |
   | Steps           | 1. login into web app                                                                                                                         |
   | Expected Result | 1. User can not login in to web application<br>2. information about locked account is diplayed<br>3. „contact with admin” button is displayed |

   | Parameter       | Content                                                                                                                                                                                                   |
   |-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | ID              | 32                                                                                                                                                                                                        |
   | Name            | After X days form last password change, system display message about password change proposal message                                                                                                     |
   | Preconditions   | 1. Standard user credentials<br>2. Tester have access to web app users data base                                                                                                                          |
   | Steps           | 1. login into DB<br>Find user<br>3. Change date last password teset to X days backward<br>4. As a user try Login in to web app<br>                                                                        |
   | Expected Result | 1. System display password change proposal message<br>2. „Change password” button works and redirect correctly<br>3. „Remind in x days” button works correctly – user is redirect to main viev of web app |
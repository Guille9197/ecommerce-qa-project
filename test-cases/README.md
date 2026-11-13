# Test Cases

## Registration

### TC-REG-001 — Register a new user with valid data

**Priority:** High

**Preconditions:**
- User is not registered.
- User has a valid email address.

**Test Steps:**

1. Open the nopCommerce Demo Store.
2. Click **Register**.
3. Select the required gender option.
4. Enter a valid first name.
5. Enter a valid last name.
6. Enter a unique email address.
7. Enter a valid password.
8. Confirm the password.
9. Click **Register**.

**Actual Result:**

The user account was successfully created and the message "Your registration completed" was displayed.

**Status:**

PASS

**Execution Date:**

August 23, 2026

**Evidence:**
[TC-REG-001 Registration Success](./evidence/TC-REG-001-registration-success.png)

---

### TC-REG-002 — Register with empty email

**Priority:** High

**Preconditions:**
- User is not registered.
- Registration page is accessible.

**Test Steps:**

1. Open the nopCommerce Demo Store.
2. Click **Register**.
3. Select the required gender option.
4. Enter a valid first name.
5. Enter a valid last name.
6. Leave the email field empty.
7. Enter a valid password.
8. Confirm the password.
9. Click **Register**.

**Expected Result:**

Registration should not be completed and an appropriate validation message should be displayed for the email field.

**Actual Result:**

The registration was not completed and the validation message "Email is required." was displayed below the Email field.

**Status:**

PASS

**Execution Date:**

August 23, 2026

**Evidence:**

[TC-REG-002 Registration - Empty Email](./evidence/TC-REG-002-registration-empty-email.png)

---

### TC-REG-003 — Register with invalid email format

**Priority:** High

**Preconditions:**
- User is not registered.
- Registration page is accessible.

**Test Steps:**

1. Open the nopCommerce Demo Store.
2. Click **Register**.
3. Select the required gender option.
4. Enter a valid first name.
5. Enter a valid last name.
6. Enter an invalid email address, for example `qa@invalid`.
7. Enter a valid password.
8. Confirm the password.
9. Click **Register**.

**Expected Result:**

Registration should not be completed and an appropriate validation message should be displayed indicating that the email format is invalid.

**Actual Result:**

The registration was not completed and the validation message "Wrong email" was displayed below the Email field.

**Status:**

PASS

**Execution Date:**

August 25, 2026

**Evidence:**

[TC-REG-003 Registration - Invalid Email](./evidence/TC-REG-003-registration-invalid-email.png)

---

### TC-REG-004 — Register with an existing email address

**Priority:** High

**Preconditions:**
- An account with the test email address is already registered.
- Registration page is accessible.

**Test Steps:**

1. Open the nopCommerce Demo Store.
2. Click **Register**.
3. Select the required gender option.
4. Enter a valid first name.
5. Enter a valid last name.
6. Enter an email address that is already registered.
7. Enter a valid password.
8. Confirm the password.
9. Click **Register**.

**Expected Result:**
The system should not allow registration using an email address that is already registered. An appropriate error message should be displayed.

**Actual Result:**
The system allowed the registration and displayed the message "Your registration completed".

**Status:** Failed

**Evidence:** [TC-REG-004 Duplicate Email Registration](evidence/TC-REG-004-duplicate-email-registration-fail.png)

---

## TC-REG-005 — Register with empty password

**Priority:** High

### Preconditions:
- User is not registered.
- Registration page is accessible.

### Test Steps:
1. Open the nopCommerce Demo Store.
2. Click **Register**.
3. Select the required gender option.
4. Enter a valid first name.
5. Enter a valid last name.
6. Enter a unique valid email address.
7. Leave the **Password** field empty.
8. Enter a value in the **Confirm password** field.
9. Click **Register**.

### Expected Result:
The system should not allow the registration and should display a validation message indicating that the password is required.

### Actual Result:
The system did not allow the registration, but displayed the message "The password and confirmation password do not match" instead of indicating that the password field is required.

### Status:
**Failed**

### Evidence:
[TC-REG-005 Empty Password](evidence/TC-REG-005-empty-password-fail.png)

## TC-REG-006 — Register with mismatched password confirmation

**Priority:** High

### Preconditions:
- User is not registered.
- Registration page is accessible.

### Test Steps:
1. Open the nopCommerce Demo Store.
2. Click **Register**.
3. Select the required gender option.
4. Enter a valid first name.
5. Enter a valid last name.
6. Enter a unique valid email address.
7. Enter a valid password in the **Password** field.
8. Enter a different password in the **Confirm password** field.
9. Click **Register**.

### Expected Result:
The system should not allow the registration and should display a validation message indicating that the password and confirmation password do not match.

### Actual Result:
The system did not allow the registration and displayed the message "The password and confirmation password do not match."

### Status:
**Passed**

### Evidence:
[TC-REG-006 Password Confirmation Mismatch](evidence/TC-REG-006-password-confirmation-mismatch.png)

### TC-REG-007 — Register with empty password confirmation

**Priority:** High

**Preconditions:**
- User is not registered.
- Registration page is accessible.

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Click Register.
3. Select the required gender option.
4. Enter a valid first name.
5. Enter a valid last name.
6. Enter a unique email address.
7. Enter a valid password.
8. Leave the Confirm password field empty.
9. Click Register.

**Expected Result:**

The system should not allow registration and should display a validation message indicating that the password confirmation field is required.

**Actual Result:**

The registration was not completed, and the system displayed a validation message indicating that the Confirm password field is required.

**Status:**

PASS

**Execution Date:**

November 2, 2026

**Evidence:**

[TC-REG-007 Registration - Empty Password Confirmation](evidence/TC-REG-007%20Registration%20-%20Empty%20Password%20Confirmation.png)

### TC-REG-008 — Register with empty first name

**Priority:** High

**Preconditions:**
- User is not registered.
- Registration page is accessible.

**Test Steps:**

1. Open the nopCommerce Demo Store.
2. Click Register.
3. Select the required gender option.
4. Leave the First name field empty.
5. Enter a valid last name.
6. Enter a unique email address.
7. Enter a valid password.
8. Confirm the password.
9. Click Register.

**Expected Result:**

The system should not allow registration and should display a validation message indicating that the First name field is required.

**Actual Result:**

The system prevented registration and displayed a validation message indicating that the First name field is required. No account was created.

**Status:**

PASS

**Execution Date:**

November 4, 2026

**Evidence:**

[TC-REG-008 Empty First Name](evidence/TC-REG-008_Register_Empty_First_Name.png)

### TC-REG-009 — Register with empty last name

**Priority:** High

**Preconditions:**

- User is not registered.
- Registration page is accessible.

**Test Steps:**

1. Open the nopCommerce Demo Store.
2. Click Register.
3. Select the required gender option.
4. Enter a valid first name.
5. Leave the Last name field empty.
6. Enter a unique email address.
7. Enter a valid password.
8. Confirm the password.
9. Click Register.

**Expected Result:**

The system should not allow registration and should display a validation message indicating that the Last name field is required.

**Actual Result:**

The system prevented registration and displayed a validation message indicating that the Last name field is required. No account was created.

**Status:**

PASS

**Execution Date:**

November 4, 2026

**Evidence:**

[TC-REG-009 Empty Last Name](evidence/TC-REG-009_Register_Empty_Last_Name.png)

### TC-REG-010 — Register with Invalid Password Confirmation

**Module:** 
Registration  
**Priority:** 
High  
**Preconditions:**
- The user is not registered.
- The Registration page is accessible.

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Click on **Register**.
3. Select the required gender option.
4. Enter a valid first name.
5. Enter a valid last name.
6. Enter a unique email address.
7. Enter a valid password.
8. Enter a different password in the **Confirm password** field.
9. Click **Register**.

**Expected Result:**
The system should reject the registration and display a validation message indicating that the password and confirmation password do not match.

**Actual Result:**
The system rejected the registration and displayed a validation message indicating that the password and confirmation password do not match.

**Status:** 
PASS

**Execution Date:** 
November 4, 2026

**Evidence:** 
[TC-REG-010 Invalid Password Confirmation](evidence/TC-REG-010_Register_Invalid_Password_Confirmation.png)

### TC-LOGIN-001 — Login with Valid Credentials

**Module:** Login & Authentication

**Priority:** High

**Preconditions:**
- A registered user account exists.
- The user is logged out.
- The Login page is accessible.

**Test Data:**

| Field | Test Value |
|---|---|
| Email | Registered test account email |
| Password | Correct password associated with the account |
| Account Status | Registered |
| User Type | Registered Customer |

**Environment Details:**

| Property | Value |
|---|---|
| Application | nopCommerce Demo Store |
| Environment | Public Demo |
| Platform | Web |
| Browser | Google Chrome |
| Operating System | Windows |
| Test Type | Manual |
| Test URL | https://demo.nopcommerce.com/ |

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Click on **Log in**.
3. Enter a registered email address.
4. Enter the correct password.
5. Click the **Log in** button.

**Expected Result:**

The system should authenticate the user successfully and redirect them to the appropriate page. The user's account information should be accessible, and the login option should be replaced by account-related options.

**Actual Result:**

The system successfully authenticated the user using valid credentials. The user was redirected to the store, and account-related options became available.

**Status:** PASS

**Execution Date:** November 5, 2026

**Evidence:** 

[TC-REG-001 Registration Success](evidence/TC-REG-001-registration-success.png)

[TC-REG-001 Registration Completed](evidence/TC-REG-001_Registration_Completed.png)

### TC-LOGIN-002 — Login with Invalid Password

**Module:** Login & Authentication

**Priority:** High

**Preconditions:**
- A registered user account exists.
- The user is logged out.
- The Login page is accessible.

**Test Data:**

| Field | Test Value |
|---|---|
| Email | Registered test account email |
| Password | Incorrect password |
| Account Status | Registered |
| User Type | Registered Customer |

**Environment Details:**

| Property | Value |
|---|---|
| Application | nopCommerce Demo Store |
| Environment | Public Demo |
| Platform | Web |
| Browser | Google Chrome |
| Operating System | Windows |
| Test Type | Manual |
| Test URL | https://demo.nopcommerce.com/ |

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Click on **Log in**.
3. Enter a registered email address.
4. Enter an incorrect password.
5. Click the **Log in** button.

**Expected Result:**

The system should reject the login attempt and display an appropriate error message indicating that the credentials are incorrect. The user should remain unauthenticated.

**Actual Result:**

The system rejected the login attempt and displayed an error message indicating that the login was unsuccessful due to invalid credentials. The user remained unauthenticated.

**Status:** PASS

**Execution Date:** November 5, 2026

**Evidence:** 

[TC-LOGIN-002 Login Unsuccessful - Invalid Password](evidence/TC-LOGIN-002_Login_Unsuccessful_Invalid_Password.png)

### TC-LOGIN-003 — Login with Empty Password

**Module:** Login & Authentication

**Priority:** High

**Preconditions:**
- A registered user account exists.
- The user is logged out.
- The Login page is accessible.

**Test Data:**

| Field | Test Value |
|---|---|
| Email | Registered test account email |
| Password | Empty |
| Account Status | Registered |
| User Type | Registered Customer |

**Environment Details:**

| Property | Value |
|---|---|
| Application | nopCommerce Demo Store |
| Environment | Public Demo |
| Platform | Web |
| Browser | Google Chrome |
| Operating System | Windows |
| Test Type | Manual |
| Test URL | https://demo.nopcommerce.com/ |

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Click on **Log in**.
3. Enter a registered email address.
4. Leave the **Password** field empty.
5. Click the **Log in** button.

**Expected Result:**

The system should reject the login attempt and display an appropriate validation message indicating that the password is required. The user should remain unauthenticated.

**Actual Result:**

The system rejected the login attempt when the password field was left empty. A validation message was displayed, and the user remained unauthenticated.

**Status:** PASS

**Execution Date:** November 5, 2026

**Evidence:** 

[TC-LOGIN-003 Login with Empty Password](evidence/TC-LOGIN-003_Login_Empty_Password.png)

### TC-LOGIN-004 — Access Customer Account After Login

**Module:** Login & Authentication

**Priority:** High

**Preconditions:**
- A registered user account exists.
- The user is logged out.
- The Login page is accessible.

**Test Data:**

| Field | Test Value |
|---|---|
| Email | Registered test account email |
| Password | Correct account password |
| Account Status | Registered |
| User Type | Registered Customer |

**Environment Details:**

| Property | Value |
|---|---|
| Application | nopCommerce Demo Store |
| Environment | Public Demo |
| Platform | Web |
| Browser | Google Chrome |
| Operating System | Windows |
| Test Type | Manual |
| Test URL | https://demo.nopcommerce.com/ |

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Click on **Log in**.
3. Enter valid account credentials.
4. Click the **Log in** button.
5. Verify that the user is successfully authenticated.
6. Click on **My account**.

**Expected Result:**

The system should allow the authenticated user to access the My Account page and display the customer account information and available account sections.

**Actual Result:**

The system successfully authenticated the user and allowed access to the My Account page. The customer account information and available account sections were displayed.

**Status:** PASS

**Execution Date:** November 5, 2026

**Evidence:** 

[TC-LOGIN-004 Access Customer Account](evidence/TC-LOGIN-004_Access_Customer_Account.png)

### TC-LOGIN-005 — Logout from Customer Account

**Module:** Login & Authentication

**Priority:** High

**Preconditions:**
- A registered user account exists.
- The user is successfully logged in.
- The My Account page is accessible.

**Test Data:**

| Field | Test Value |
|---|---|
| User Account | Registered customer account |
| Initial Session Status | Logged In |
| Action | Log out |

**Environment Details:**

| Property | Value |
|---|---|
| Application | nopCommerce Demo Store |
| Environment | Public Demo |
| Platform | Web |
| Browser | Google Chrome |
| Operating System | Windows |
| Test Type | Manual |
| Test URL | https://demo.nopcommerce.com/ |

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Log in using valid customer credentials.
3. Verify that the user is successfully logged in.
4. Locate and click the **Log out** option.
5. Verify that the user is redirected to the appropriate page.
6. Check that the **Log in** and **Register** options are displayed in the navigation bar.

**Expected Result:**

The system should successfully terminate the user's session, redirect the user to the appropriate page, and display the logged-out navigation options.

**Actual Result:**

The system successfully terminated the user's session. The user was redirected to the appropriate page, and the **Log in** and **Register** options were displayed in the navigation bar.

**Status:** PASS

**Execution Date:** November 6, 2026

**Evidence:** 

[TC-LOGIN-005 Logout Customer Account](evidence/TC-LOGIN-005_Logout_Customer_Account.png)

### TC-LOGIN-006 — Verify Account Access After Logout

**Module:** Login & Authentication

**Priority:** High

**Preconditions:**
- A registered user account exists.
- The user has successfully logged in and then logged out.
- The My Account page was previously accessed during the authenticated session.

**Test Data:**

| Field | Test Value |
|---|---|
| User Account | Registered customer account |
| Initial Session Status | Logged Out |
| Target Page | My Account |

**Environment Details:**

| Property | Value |
|---|---|
| Application | nopCommerce Demo Store |
| Environment | Public Demo |
| Platform | Web |
| Browser | Google Chrome |
| Operating System | Windows |
| Test Type | Manual |
| Test URL | https://demo.nopcommerce.com/ |

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Log in using valid customer credentials.
3. Navigate to **My Account**.
4. Log out using the **Log out** option.
5. Use the browser's Back button to return to the previously visited My Account page.
6. Refresh the page if necessary.
7. Verify whether the account information remains accessible.

**Expected Result:**

The system should prevent access to protected customer account information after logout. The user should be redirected to the login page or another appropriate page requiring authentication.

**Actual Result:**

After logging out, the system prevented access to the protected customer account information. The user could not access the authenticated account page without logging in again.

**Status:** PASS

**Execution Date:** November 6, 2026

**Evidence:** 

[TC-LOGIN-006 Account Access After Logout](evidence/TC-LOGIN-006_Account_Access_After_Logout.png)

### TC-LOGIN-007 — Verify Session Persistence After Page Refresh

**Module:** Login & Authentication

**Priority:** Medium

**Preconditions:**
- A registered user account exists.
- The user is successfully logged in.
- The My Account page is accessible.

**Test Data:**

| Field | Test Value |
|---|---|
| User Account | Registered customer account |
| Initial Session Status | Logged In |
| Action | Refresh browser page |

**Environment Details:**

| Property | Value |
|---|---|
| Application | nopCommerce Demo Store |
| Environment | Public Demo |
| Platform | Web |
| Browser | Google Chrome |
| Operating System | Windows |
| Test Type | Manual |
| Test URL | https://demo.nopcommerce.com/ |

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Log in using valid customer credentials.
3. Navigate to **My Account**.
4. Verify that the account page is accessible.
5. Refresh the browser page using F5 or the browser refresh button.
6. Verify that the user remains logged in.
7. Verify that the My Account page and customer information remain accessible.

**Expected Result:**

The system should preserve the authenticated session after the page refresh. The user should remain logged in and retain access to the My Account page without entering credentials again.

**Actual Result:**

The system successfully maintained the authenticated session after the page refresh. The user remained logged in and retained access to the My Account page without having to enter credentials again.

**Status:** PASS

**Execution Date:** November 6, 2026

**Evidence:** 

[TC-LOGIN-007 Session Persistence After Refresh](evidence/TC-LOGIN-007_Session_Persistence_After_Refresh.png)

### TC-SEARCH-001 — Search Products Using a Valid Keyword

**Module:** Product Search & Filtering

**Priority:** High

**Preconditions:**
- The nopCommerce Demo Store is accessible.
- The product catalog contains products matching the search keyword.

**Test Data:**

| Field | Test Value |
|---|---|
| Search Keyword | computer |
| Search Type | Valid Keyword |

**Environment Details:**

| Property | Value |
|---|---|
| Application | nopCommerce Demo Store |
| Environment | Public Demo |
| Platform | Web |
| Browser | Google Chrome |
| Operating System | Windows |
| Test Type | Manual |
| Test URL | https://demo.nopcommerce.com/ |

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Locate the search field in the header.
3. Enter the keyword `computer`.
4. Click the Search button.
5. Review the displayed search results.
6. Verify that the results contain products relevant to the entered keyword.

**Expected Result:**

The system should display relevant products matching the search keyword. The search results page should load successfully and show the matching products.

**Actual Result:**

The system successfully displayed search results relevant to the keyword `computer`. The search results page loaded correctly and presented matching products.

**Status:** PASS

**Execution Date:** November 10, 2026

**Evidence:** 

[TC-SEARCH-001 Search Products Using a Valid Keyword](evidence/TC-SEARCH-001_Search_Products_Valid_Keyword.png)

### TC-SEARCH-002 — Search Products Using a Nonexistent Keyword

**Module:** Product Search & Filtering

**Priority:** Medium

**Preconditions:**
- The nopCommerce Demo Store is accessible.
- The product catalog is available.
- The selected keyword does not match any existing product.

**Test Data:**

| Field | Test Value |
|---|---|
| Search Keyword | xyznonexistent123 |
| Search Type | Nonexistent Keyword |

**Environment Details:**

| Property | Value |
|---|---|
| Application | nopCommerce Demo Store |
| Environment | Public Demo |
| Platform | Web |
| Browser | Google Chrome |
| Operating System | Windows |
| Test Type | Manual |
| Test URL | https://demo.nopcommerce.com/ |

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Locate the search field in the header.
3. Enter the keyword `xyznonexistent123`.
4. Click the Search button.
5. Review the displayed search results.
6. Verify that no products are returned for the nonexistent keyword.
7. Check whether the system displays an appropriate no-results message.

**Expected Result:**

The system should display no matching products and provide an appropriate message indicating that no products were found. The search page should load without errors.

**Actual Result:**

The system successfully processed the search request. No matching products were displayed for the nonexistent keyword, and the search page handled the request without errors.

**Status:** PASS

**Execution Date:** November 10, 2026

**Evidence:** 

[TC-SEARCH-002 Search Products Using a Nonexistent Keyword](evidence/TC-SEARCH-002_Search_Products_Nonexistent_Keyword.png)

### TC-SEARCH-003 — Search with an Empty Search Field

**Module:** Product Search & Filtering

**Priority:** Medium

**Preconditions:**
- The nopCommerce Demo Store is accessible.
- The product catalog is available.

**Test Data:**

| Field | Test Value |
|---|---|
| Search Keyword | Empty |
| Search Type | Empty Search |

**Environment Details:**

| Property | Value |
|---|---|
| Application | nopCommerce Demo Store |
| Environment | Public Demo |
| Platform | Web |
| Browser | Google Chrome |
| Operating System | Windows |
| Test Type | Manual |
| Test URL | https://demo.nopcommerce.com/ |

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Locate the search field in the header.
3. Leave the search field empty.
4. Click the Search button.
5. Observe the system response.
6. Verify whether the system displays search results, validation feedback, or an appropriate response.

**Expected Result:**

The system should handle an empty search request appropriately without causing an application error or unexpected behavior.

**Actual Result:**

The system prevented the empty search request from being processed and displayed the validation message: "Search term minimum length is 3 characters." The application handled the input correctly without displaying an application error.

**Status:** PASS

**Execution Date:** November 10, 2026

**Evidence:** 

[TC-SEARCH-003 Search with an Empty Search Field](evidence/TC-SEARCH-003_Search_Empty_Field.png)

### TC-SEARCH-004 — Search Using a Partial Product Name

**Module:** Product Search & Filtering

**Priority:** Medium

**Preconditions:**
- The nopCommerce Demo Store is accessible.
- The product catalog contains products with names matching the selected partial keyword.

**Test Data:**

| Field | Test Value |
|---|---|
| Search Keyword | `comp` |
| Search Type | Partial Product Name |
| Minimum Search Length | 3 characters |

**Environment Details:**

| Property | Value |
|---|---|
| Application | nopCommerce Demo Store |
| Environment | Public Demo |
| Platform | Web |
| Browser | Google Chrome |
| Operating System | Windows |
| Test Type | Manual |
| Test URL | https://demo.nopcommerce.com/ |

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Locate the search field in the header.
3. Enter the partial keyword `comp`.
4. Click the Search button.
5. Review the displayed search results.
6. Verify whether products containing or matching the partial keyword are displayed.

**Expected Result:**

The system should return relevant products matching the partial keyword, even when the complete product name is not provided.

**Actual Result:**

Not Executed.

**Status:** Not Executed

**Execution Date:** Pending

**Evidence:** 

[TC-SEARCH-004 Search Using a Partial Product Name](evidence/TC-SEARCH-004_Search_Partial_Product_Name.png)

### TC-SEARCH-005 — Verify Search Results Relevance

**Module:** Product Search & Filtering

**Priority:** High

**Preconditions:**
- The nopCommerce Demo Store is accessible.
- The product catalog contains products related to the search keyword.
- The search functionality is available.

**Test Data:**

| Field | Test Value |
|---|---|
| Search Keyword | computer |
| Search Type | Results Relevance |
| Expected Results | Products relevant to the keyword |

**Environment Details:**

| Property | Value |
|---|---|
| Application | nopCommerce Demo Store |
| Environment | Public Demo |
| Platform | Web |
| Browser | Google Chrome |
| Operating System | Windows |
| Test Type | Manual |
| Test URL | https://demo.nopcommerce.com/ |

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Locate the search field in the header.
3. Enter the keyword `computer`.
4. Click the Search button.
5. Review all displayed search results.
6. Inspect the product names and descriptions.
7. Verify that the displayed products are relevant to the search keyword.
8. Check whether unrelated products are included in the results.

**Expected Result:**

The system should display products relevant to the entered search keyword. Unrelated products should not appear in the search results.

**Actual Result:**

The system successfully displayed products relevant to the search keyword `computer`. The search results matched the intended search criteria.

**Status:** PASS

**Execution Date:** November 12, 2026

**Evidence:** 

[TC-SEARCH-005 Search Results Relevance](evidence/TC-SEARCH-005_Search_Results_Relevance.png)

### TC-SEARCH-006 — Navigate Through Search Results

**Module:** Product Search & Filtering

**Priority:** Medium

**Preconditions:**
- The nopCommerce Demo Store is accessible.
- The product catalog contains enough matching products to generate multiple result pages.
- The search functionality is available.

**Test Data:**

| Field | Test Value |
|---|---|
| Search Keyword | computer |
| Search Type | Search Results Pagination |
| Expected Results | Multiple pages of search results |

**Environment Details:**

| Property | Value |
|---|---|
| Application | nopCommerce Demo Store |
| Environment | Public Demo |
| Platform | Web |
| Browser | Google Chrome |
| Operating System | Windows |
| Test Type | Manual |
| Test URL | https://demo.nopcommerce.com/ |

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Locate the search field in the header.
3. Enter the keyword `computer`.
4. Click the Search button.
5. Review the displayed search results.
6. Check whether pagination controls are available.
7. Navigate to the next page.
8. Verify that a different set of search results is displayed.
9. Navigate back to the previous page.
10. Verify that the previous search results are displayed correctly.

**Expected Result:**

The system should allow users to navigate between available search result pages. The displayed products should update correctly when changing pages, without errors or unexpected behavior.

**Actual Result:**

The system successfully allowed navigation between search result pages. The displayed products updated correctly when moving to the next page, and the previous page was accessible again without errors.

**Status:** PASS

**Execution Date:** November 12, 2026

**Evidence:**
- [TC-SEARCH-006 First Page](evidence/TC-SEARCH-006_Search_Results_First_Page.png)
- [TC-SEARCH-006 Next Page](evidence/TC-SEARCH-006_Search_Results_Next_Page.png)
- [TC-SEARCH-006 Previous Page](evidence/TC-SEARCH-006_Search_Results_Previous_Page.png)

- ### TC-PROD-001 — Verify Product Details Page

**Module:** Product Details

**Priority:** High

**Preconditions:**
- The nopCommerce Demo Store is accessible.
- The product catalog contains available products.
- The user can access product listings.

**Test Data:**

| Field | Test Value |
|---|---|
| Product Name | Build your own computer |
| Product Category | Computers |
| Navigation Method | Product Listing |

**Environment Details:**

| Property | Value |
|---|---|
| Application | nopCommerce Demo Store |
| Environment | Public Demo |
| Platform | Web |
| Browser | Google Chrome |
| Operating System | Windows |
| Test Type | Manual |
| Test URL | https://demo.nopcommerce.com/ |

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Navigate to the Computers category.
3. Locate the product **Build your own computer**.
4. Click the product name or image.
5. Verify that the product details page loads successfully.
6. Verify that the page displays the main product information and purchasing options.

**Expected Result:**

The system should successfully navigate to the selected product details page. The page should display the product information and available purchasing options without errors.

**Actual Result:**

The system successfully navigated to the **Build your own computer** product details page. The page loaded correctly and displayed the product information and available purchasing options.

**Status:** PASS

**Execution Date:** November 12, 2026

**Evidence:** 

[TC-PROD-001 Verify Product Details Page](evidence/TC-PROD-001_Product_Details_Page.png)

### TC-PROD-002 — Verify Product Name and Description

**Module:** Product Details

**Priority:** High

**Preconditions:**
- The nopCommerce Demo Store is accessible.
- The product "Build your own computer" exists in the product catalog.
- The product details page is accessible.

**Test Data:**

| Field | Test Value |
|---|---|
| Product Name | Build your own computer |
| Product Category | Computers |
| Information to Validate | Product Name and Description |

**Environment Details:**

| Property | Value |
|---|---|
| Application | nopCommerce Demo Store |
| Environment | Public Demo |
| Platform | Web |
| Browser | Google Chrome |
| Operating System | Windows |
| Test Type | Manual |
| Test URL | https://demo.nopcommerce.com/ |

**Test Steps:**
1. Open the nopCommerce Demo Store.
2. Navigate to the Computers category.
3. Open the "Build your own computer" product.
4. Locate the product name displayed on the details page.
5. Verify that the product name matches the selected product.
6. Locate the product description.
7. Verify that the description is displayed correctly and is readable.

**Expected Result:**

The product details page should display the correct product name and its corresponding description. Both elements should be visible, readable, and properly presented.

**Actual Result:**

The product details page successfully displayed the correct product name, "Build your own computer", and its corresponding description. Both elements were visible and readable.

**Status:** PASS

**Execution Date:** November 12, 2026

**Evidence:** 

[TC-PROD-002 Product Name and Description](evidence/TC-PROD-002_Product_Name_Description.png)

# TC-PROD-003 — Verify Product Price

**Module:** Product Details  
**Priority:** High  
**Test Type:** Manual Functional Testing

### Preconditions
- The user can access the nopCommerce Demo Store.
- The product details page is available.

### Test Data
- **Product:** Build your own computer
- **URL:** https://demo.nopcommerce.com/

### Environment Details
- **Platform:** Web
- **Browser:** Google Chrome
- **Operating System:** Windows
- **Environment:** Public Demo Store

### Test Steps
1. Navigate to the nopCommerce Demo Store.
2. Open the **Computers** category.
3. Navigate to the **Desktops** subcategory.
4. Select **Build your own computer**.
5. Locate the product price displayed on the product details page.
6. Verify that the price is visible and formatted correctly.

### Expected Result
- The product price is displayed on the product details page.
- The price is clearly visible and uses the expected currency format.
- The displayed price is consistent with the selected product and its configuration.

### Actual Result
The product price was successfully displayed on the product details page and was clearly visible in the expected currency format.

### Status
PASS

### Execution Date
November 12, 2026

### Evidence

[TC-PROD-003 Verify Product Price](evidence/TC-PROD-003_Verify_Product_Price.png)

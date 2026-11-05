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

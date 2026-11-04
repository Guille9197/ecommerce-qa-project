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

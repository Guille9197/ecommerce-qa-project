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

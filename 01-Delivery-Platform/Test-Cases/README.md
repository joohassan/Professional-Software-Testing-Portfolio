# Test Scenarios

## Registration & Verification

| Scenario ID | Scenario | Type |
|---|---|---|
| REG-SC-001 | Verify customer can register with valid required data | Positive |
| REG-SC-002 | Verify registration with missing required fields | Negative |
| REG-SC-003 | Verify validation of invalid phone number | Negative |
| REG-SC-004 | Verify validation of invalid email address | Negative |
| REG-SC-005 | Verify password and confirm password validation | Negative |
| REG-SC-006 | Verify user can upload required identity documents | Positive |
| REG-SC-007 | Verify invalid or unsupported identity document upload | Negative |
| REG-SC-008 | Verify selfie upload during registration | Positive |
| REG-SC-009 | Verify OTP verification with valid OTP | Positive |
| REG-SC-010 | Verify OTP verification with invalid OTP | Negative |
| REG-SC-011 | Verify registration using phone verification | Positive |
| REG-SC-012 | Verify registration using email verification | Positive |
| REG-SC-013 | Verify already registered phone number cannot be registered again | Negative |
| REG-SC-014 | Verify already registered email cannot be registered again | Negative |

## Login

| Scenario ID | Scenario | Type |
|---|---|---|
| LOGIN-SC-001 | Verify login with valid credentials | Positive |
| LOGIN-SC-002 | Verify login with invalid credentials | Negative |
| LOGIN-SC-003 | Verify login with empty required fields | Negative |
| LOGIN-SC-004 | Verify unregistered user cannot log in | Negative |
| LOGIN-SC-005 | Verify forgot password functionality | Positive |
| LOGIN-SC-006 | Verify password reset with valid verification | Positive |
| LOGIN-SC-007 | Verify invalid verification during password reset | Negative |

## Ride Request

| Scenario ID | Scenario | Type |
|---|---|---|
| RIDE-SC-001 | Verify customer can request a ride | Positive |
| RIDE-SC-002 | Verify pickup location is required | Negative |
| RIDE-SC-003 | Verify destination is required | Negative |
| RIDE-SC-004 | Verify available drivers can receive ride requests | Positive |
| RIDE-SC-005 | Verify customer can track ride progress | Positive |
| RIDE-SC-006 | Verify ride status changes correctly during the trip | Positive |
| RIDE-SC-007 | Verify customer receives ride completion information | Positive |

## Payment

| Scenario ID | Scenario | Type |
|---|---|---|
| PAY-SC-001 | Verify successful payment | Positive |
| PAY-SC-002 | Verify payment failure handling | Negative |
| PAY-SC-003 | Verify payment information is reflected in ride summary | Positive |
| PAY-SC-004 | Verify customer can view payment-related information | Positive |

## Rating

| Scenario ID | Scenario | Type |
|---|---|---|
| RATE-SC-001 | Verify customer can rate a completed ride | Positive |
| RATE-SC-002 | Verify rating cannot be submitted before ride completion | Negative |
| RATE-SC-003 | Verify valid rating value is accepted | Positive |

## Admin Dashboard

| Scenario ID | Scenario | Type |
|---|---|---|
| ADMIN-SC-001 | Verify admin can access dashboard | Positive |
| ADMIN-SC-002 | Verify admin can manage users | Positive |
| ADMIN-SC-003 | Verify admin can manage drivers | Positive |
| ADMIN-SC-004 | Verify admin can view trips | Positive |
| ADMIN-SC-005 | Verify admin can view payment information | Positive |
| ADMIN-SC-006 | Verify admin can access reports | Positive |
| ADMIN-SC-007 | Verify unauthorized user cannot access admin functions | Negative |


---

# Detailed Test Cases

## Registration

### TC-REG-001 — Successful Customer Registration

**Scenario ID:** REG-SC-001

**Title:** Verify customer can register with valid required data

**Priority:** High

**Type:** Functional Testing

**Preconditions:**
- User is on the Registration page.
- User is not already registered in the system.

**Test Data:**
- Valid Full Name
- Valid Phone Number
- Valid Email Address
- Valid Password
- Matching Confirm Password
- Valid Selfie
- Valid ID Document
- Valid Verification Method

**Test Steps:**
1. Open the Registration page.
2. Enter a valid Full Name.
3. Enter a valid Phone Number.
4. Enter a valid Email Address.
5. Enter a valid Password.
6. Enter the same password in Confirm Password.
7. Upload a valid Selfie.
8. Upload a valid ID Document.
9. Select a valid Verification Method.
10. Submit the registration form.
11. Complete the verification process.

**Expected Result:**
- The system accepts the provided valid information.
- The registration request is submitted successfully.
- The user is directed to the required verification process.
- After successful verification, the account is created successfully.

**Actual Result:** Not Executed

**Status:** Not Run

### TC-REG-002 — Registration with Missing Required Fields

**Scenario ID:** REG-SC-002

**Title:** Verify registration fails when required fields are missing

**Priority:** High

**Type:** Negative Testing

**Preconditions:**
- User is on the Registration page.

**Test Data:**
- Leave one or more required fields empty.
- Enter valid data in the remaining fields.

**Test Steps:**
1. Open the Registration page.
2. Leave one or more required fields empty.
3. Enter valid data in the remaining fields.
4. Click the Register/Submit button.

**Expected Result:**
- The system should not create the account.
- Validation messages should be displayed for the missing required fields.
- The user should be able to correct the missing information.
- No incomplete registration should be submitted.

**Actual Result:** Not Executed

**Status:** Not Run

### TC-REG-003 — Invalid Phone Number

**Scenario ID:** REG-SC-003

**Title:** Verify registration fails when an invalid phone number is entered

**Priority:** High

**Type:** Negative Testing

**Preconditions:**
- User is on the Registration page.

**Test Data:**
- Invalid phone number format.

**Test Steps:**
1. Open the Registration page.
2. Enter valid data in all required fields.
3. Enter an invalid phone number.
4. Click the Register/Submit button.

**Expected Result:**
- The system should reject the invalid phone number.
- A clear validation message should be displayed.
- The registration request should not be completed until a valid phone number is provided.

**Actual Result:** Not Executed

**Status:** Not Run

### TC-REG-004 — Invalid Email Address

**Scenario ID:** REG-SC-004

**Title:** Verify registration fails when an invalid email address is entered

**Priority:** High

**Type:** Negative Testing

**Preconditions:**
- User is on the Registration page.

**Test Data:**
- Invalid email address format.
- Example: `user@`

**Test Steps:**
1. Open the Registration page.
2. Enter valid data in all other required fields.
3. Enter an invalid email address.
4. Click the Register button.

**Expected Result:**
- The system should reject the invalid email address.
- A clear validation message should be displayed.
- The registration should not be completed until a valid email address is provided.

**Actual Result:** Not Executed

**Status:** Not Run

### TC-REG-005 — Password and Confirm Password Validation

**Scenario ID:** REG-SC-005

**Title:** Verify registration validation when Password and Confirm Password do not match

**Priority:** High

**Type:** Negative Testing

**Preconditions:**
- User is on the Registration page.

**Test Data:**
- Valid password.
- Different Confirm Password.

**Test Steps:**
1. Open the Registration page.
2. Enter valid data in all required fields.
3. Enter a valid password.
4. Enter a different value in Confirm Password.
5. Click the Register button.

**Expected Result:**
- The system should detect that Password and Confirm Password do not match.
- A clear validation message should be displayed.
- The registration should not be completed until both values match.

**Actual Result:** Not Executed

**Status:** Not Run

### TC-REG-005 — Password and Confirm Password Validation

**Scenario ID:** REG-SC-005

**Title:** Verify registration fails when password and confirm password do not match

**Priority:** High

**Type:** Negative Testing

**Preconditions:**
- User is on the Registration page.

**Test Data:**
- Valid password.
- Different Confirm Password.

**Test Steps:**
1. Open the Registration page.
2. Enter valid data in all required fields.
3. Enter a valid password.
4. Enter a different value in Confirm Password.
5. Click the Register button.

**Expected Result:**
- The system should detect that the passwords do not match.
- A clear validation message should be displayed.
- The registration should not be completed until both passwords match.

**Actual Result:** Not Executed

**Status:** Not Run

### TC-REG-006 — Identity Document Upload

**Scenario ID:** REG-SC-006

**Title:** Verify user can upload the required identity document during registration

**Priority:** High

**Type:** Functional Testing

**Preconditions:**
- User is on the Registration page.
- User has a valid identity document available.

**Test Data:**
- Valid identity document.

**Test Steps:**
1. Open the Registration page.
2. Enter valid registration information.
3. Navigate to the identity document upload section.
4. Select a valid identity document.
5. Upload the document.
6. Complete the remaining required registration information.
7. Submit the registration form.

**Expected Result:**
- The system accepts the uploaded identity document.
- The uploaded document is displayed successfully.
- No upload error is displayed.
- The registration process can continue to the next step.

**Actual Result:** Not Executed

**Status:** Not Run

### TC-REG-007 — Invalid Identity Document Upload

**Scenario ID:** REG-SC-007

**Title:** Verify the system rejects an invalid identity document

**Priority:** High

**Type:** Negative Testing

**Preconditions:**
- User is on the Registration page.
- User has an invalid or unsupported identity document.

**Test Data:**
- Invalid identity document.
- Unsupported file format or invalid document.

**Test Steps:**
1. Open the Registration page.
2. Enter valid registration information.
3. Navigate to the identity document upload section.
4. Select an invalid or unsupported document.
5. Attempt to upload the document.

**Expected Result:**
- The system should reject the invalid document.
- A clear validation or upload error should be displayed.
- The invalid document should not be accepted as a valid identity document.
- The user should be able to upload a valid document.

**Actual Result:** Not Executed

**Status:** Not Run

### TC-REG-008 — Selfie Upload

**Scenario ID:** REG-SC-008

**Title:** Verify user can upload a valid selfie during registration

**Priority:** High

**Type:** Functional Testing

**Preconditions:**
- User is on the Registration page.
- User has a valid selfie image available.

**Test Data:**
- Valid selfie image.

**Test Steps:**
1. Open the Registration page.
2. Enter valid registration information.
3. Navigate to the selfie upload section.
4. Select a valid selfie image.
5. Upload the image.
6. Complete the remaining required registration information.
7. Submit the registration form.

**Expected Result:**
- The system accepts the valid selfie.
- The uploaded selfie is displayed successfully.
- No upload error is displayed.
- The registration process can continue to the next step.

**Actual Result:** Not Executed

**Status:** Not Run


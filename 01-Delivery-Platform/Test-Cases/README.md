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

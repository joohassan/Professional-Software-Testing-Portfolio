# Delivery Platform - API Testing

## API Testing Scope

API testing will cover the main backend operations of the Delivery Platform, including:

- Authentication
- Registration
- OTP Verification
- Login
- Password Recovery
- Ride Requests
- Driver Assignment
- Ride Status
- Payments
- Ratings
- Notifications
- Customer Profile
- Driver Profile
- Packages and Subscriptions
- Offers and Promo Codes
- Admin Operations

---

## 1. Authentication APIs

### API-AUTH-001 — Customer Registration

**Method:** POST

**Endpoint:** `/api/register`

**Purpose:** Create a new customer account.

**Validation:**
- Required fields should be validated.
- Email format should be validated.
- Phone number should be validated.
- Password should be validated.
- Duplicate email/phone should be rejected.

**Expected Response:**
- Successful registration returns a success response.
- Invalid data returns an appropriate validation error.

---

### API-AUTH-002 — OTP Verification

**Method:** POST

**Endpoint:** `/api/verify-otp`

**Purpose:** Verify the user's registration.

**Validation:**
- Valid OTP should be accepted.
- Invalid OTP should be rejected.
- Expired OTP should be rejected.
- Missing OTP should return a validation error.

---

### API-AUTH-003 — Login

**Method:** POST

**Endpoint:** `/api/login`

**Purpose:** Authenticate the user.

**Validation:**
- Valid credentials should authenticate successfully.
- Invalid credentials should be rejected.
- Required fields should be validated.
- Authentication token should be returned after successful login.

---

## 2. Ride APIs

### API-RIDE-001 — Request Ride

**Method:** POST

**Endpoint:** `/api/rides`

**Purpose:** Create a new ride request.

**Validation:**
- Pickup location is required.
- Destination is required.
- Payment method should be validated.
- Ride request should be created successfully with valid data.

---

### API-RIDE-002 — Get Ride Details

**Method:** GET

**Endpoint:** `/api/rides/{rideId}`

**Purpose:** Retrieve ride information.

**Validation:**
- Valid ride ID should return ride details.
- Invalid ride ID should return an appropriate error.
- Unauthorized users should not access another user's ride.

---

### API-RIDE-003 — Update Ride Status

**Method:** PUT

**Endpoint:** `/api/rides/{rideId}/status`

**Purpose:** Update the current ride status.

**Validation:**
- Valid status transitions should be accepted.
- Invalid status transitions should be rejected.
- Unauthorized requests should be rejected.

---

## 3. Driver APIs

### API-DRIVER-001 — Get Available Drivers

**Method:** GET

**Endpoint:** `/api/drivers/available`

**Purpose:** Retrieve available drivers for ride assignment.

**Validation:**
- Available drivers should be returned.
- Unavailable drivers should not be returned.
- Driver availability should reflect the current status.

---

### API-DRIVER-002 — Driver Accept Ride

**Method:** POST

**Endpoint:** `/api/rides/{rideId}/accept`

**Purpose:** Allow an available driver to accept a ride.

**Validation:**
- Available driver should be able to accept the ride.
- Unavailable driver should not accept a new ride.
- Already assigned ride should not be accepted by another driver.

---

## 4. Payment APIs

### API-PAY-001 — Create Payment

**Method:** POST

**Endpoint:** `/api/payments`

**Purpose:** Process payment for a completed ride.

**Validation:**
- Valid payment data should be accepted.
- Invalid payment data should be rejected.
- Payment amount should match the ride amount.
- Payment status should be returned.

---

### API-PAY-002 — Get Payment Details

**Method:** GET

**Endpoint:** `/api/payments/{paymentId}`

**Purpose:** Retrieve payment information.

**Validation:**
- Valid payment ID should return payment details.
- Invalid payment ID should return an appropriate error.
- Unauthorized users should not access another user's payment information.

---

## 5. Offers & Promo Codes

### API-OFFER-001 — Validate Promo Code

**Method:** POST

**Endpoint:** `/api/promo/validate`

**Purpose:** Validate a promo code before applying a discount.

**Validation:**
- Valid promo code should be accepted.
- Invalid promo code should be rejected.
- Expired promo code should be rejected.
- Discount information should be returned.

---

## 6. Rating APIs

### API-RATING-001 — Submit Rating

**Method:** POST

**Endpoint:** `/api/ratings`

**Purpose:** Submit a rating after a completed ride.

**Validation:**
- Valid rating should be accepted.
- Rating should only be submitted for an eligible ride.
- Invalid rating value should be rejected.

---

## 7. Profile APIs

### API-PROFILE-001 — Get Customer Profile

**Method:** GET

**Endpoint:** `/api/profile`

**Purpose:** Retrieve customer profile information.

**Validation:**
- Authenticated user should receive their profile.
- Unauthenticated request should be rejected.

---

### API-PROFILE-002 — Update Customer Profile

**Method:** PUT

**Endpoint:** `/api/profile`

**Purpose:** Update customer profile information.

**Validation:**
- Valid profile data should be accepted.
- Invalid data should return validation errors.
- Updated information should be returned correctly.

---

## 8. Notification APIs

### API-NOTIF-001 — Get Notifications

**Method:** GET

**Endpoint:** `/api/notifications`

**Purpose:** Retrieve user notifications.

**Validation:**
- Authenticated user should receive their notifications.
- User should not receive another user's notifications.

---

## 9. Subscription APIs

### API-SUB-001 — Get Available Packages

**Method:** GET

**Endpoint:** `/api/packages`

**Purpose:** Retrieve available driver packages.

**Validation:**
- Available packages should be returned.
- Package information should be complete.

---

### API-SUB-002 — Subscribe to Package

**Method:** POST

**Endpoint:** `/api/subscriptions`

**Purpose:** Subscribe a driver to a package.

**Validation:**
- Valid package should be accepted.
- Invalid package should be rejected.
- Payment status should be validated.
- Subscription status should be returned.

---

## 10. Admin APIs

### API-ADMIN-001 — Get Dashboard Data

**Method:** GET

**Endpoint:** `/api/admin/dashboard`

**Purpose:** Retrieve dashboard information.

**Validation:**
- Authorized admin should access dashboard data.
- Non-admin users should be rejected.
- Dashboard data should be returned successfully.

---

### API-ADMIN-002 — Get Financial Reports

**Method:** GET

**Endpoint:** `/api/admin/reports/financial`

**Purpose:** Retrieve financial report information.

**Validation:**
- Authorized admin should access reports.
- Non-admin users should be rejected.
- Report data should be returned successfully.

---

# API Response Validation

For every API, verify:

- HTTP Status Code
- Response Time
- Response Body
- JSON Structure
- Required Fields
- Data Types
- Error Messages
- Authentication
- Authorization
- Invalid Input Handling
- Missing Input Handling

---

# Tools

API testing will be performed using:

- Postman
- REST APIs
- JSON
- HTTP Methods
- HTTP Status Codes
- Postman Collections
- Environment Variables

---

# Test Status

| Status | Meaning |
|---|---|
| Not Run | Test has not been executed |
| Pass | Actual result matches expected result |
| Fail | Actual result does not match expected result |
| Blocked | Test cannot be executed بسبب dependency or environment issue |

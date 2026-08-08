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

## 1. Customer Registration & Verification

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-REG-001 | Register with valid required customer information | Positive | High |
| TC-REG-002 | Register with missing required fields | Negative | High |
| TC-REG-003 | Register with invalid phone number | Negative | High |
| TC-REG-004 | Register with invalid email address | Negative | High |
| TC-REG-005 | Register with mismatched password and confirm password | Negative | High |
| TC-REG-006 | Upload valid identity document | Positive | High |
| TC-REG-007 | Upload invalid or unsupported identity document | Negative | High |
| TC-REG-008 | Upload valid selfie image | Positive | High |
| TC-REG-009 | Verify registration using valid verification code | Positive | High |
| TC-REG-010 | Verify registration using invalid verification code | Negative | High |
| TC-REG-011 | Verify registration using email verification | Positive | High |
| TC-REG-012 | Verify registration using phone verification | Positive | High |
| TC-REG-013 | Register using an already registered phone number | Negative | High |
| TC-REG-014 | Register using an already registered email address | Negative | High |

---

## 2. Customer Login

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-LOGIN-001 | Login using valid email and password | Positive | High |
| TC-LOGIN-002 | Login using invalid email and password | Negative | High |
| TC-LOGIN-003 | Login with empty required fields | Negative | High |
| TC-LOGIN-004 | Login using an unregistered account | Negative | High |
| TC-LOGIN-005 | Login using registered phone number when phone verification is selected | Positive | High |
| TC-LOGIN-006 | Navigate to Forgot Password from Login | Positive | Medium |
| TC-LOGIN-007 | Navigate to Registration from Login | Positive | Medium |

---

## 3. Forgot Password

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-FP-001 | Request password reset using registered email | Positive | High |
| TC-FP-002 | Request password reset using registered phone number | Positive | High |
| TC-FP-003 | Request password reset using unregistered email | Negative | High |
| TC-FP-004 | Request password reset with empty email or phone field | Negative | Medium |
| TC-FP-005 | Verify reset link or recovery message is sent | Positive | High |

---

## 4. Home Page

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-HOME-001 | Verify customer home page is displayed after successful login | Positive | High |
| TC-HOME-002 | Verify customer profile picture is displayed | Positive | Medium |
| TC-HOME-003 | Verify Request a Ride button is displayed | Positive | High |
| TC-HOME-004 | Verify last three rides are displayed in Recent Rides | Positive | Medium |
| TC-HOME-005 | Verify current offers are displayed | Positive | Medium |
| TC-HOME-006 | Navigate to Ride History | Positive | Medium |
| TC-HOME-007 | Logout from Home Page | Positive | High |

---

## 5. Offers & Promo Codes

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-OFFER-001 | Verify available offers are displayed | Positive | Medium |
| TC-OFFER-002 | Apply a valid promo code | Positive | High |
| TC-OFFER-003 | Apply an invalid promo code | Negative | High |
| TC-OFFER-004 | Apply an expired promo code | Negative | High |
| TC-OFFER-005 | Verify discount is reflected after applying promo code | Positive | High |
| TC-OFFER-006 | Verify offer details can be viewed | Positive | Medium |

---

## 6. Notifications

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-NOTIF-001 | Verify ride request confirmation notification | Positive | High |
| TC-NOTIF-002 | Verify driver arrival notification | Positive | High |
| TC-NOTIF-003 | Verify ride completion notification | Positive | High |
| TC-NOTIF-004 | Verify new offer notification | Positive | Medium |
| TC-NOTIF-005 | Open notification details | Positive | Medium |
| TC-NOTIF-006 | Navigate to the related action from notification | Positive | Medium |

---

## 7. Ride Request

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-RIDE-001 | Request a one-way ride with valid locations | Positive | High |
| TC-RIDE-002 | Request a multi-destination ride | Positive | High |
| TC-RIDE-003 | Verify current location is detected using GPS | Positive | High |
| TC-RIDE-004 | Manually adjust location when GPS is unavailable | Positive | High |
| TC-RIDE-005 | Verify estimated cost is displayed | Positive | High |
| TC-RIDE-006 | Verify expected duration is displayed | Positive | Medium |
| TC-RIDE-007 | Select male driver preference | Positive | Medium |
| TC-RIDE-008 | Select female driver preference | Positive | Medium |
| TC-RIDE-009 | Apply promo code during ride request | Positive | High |
| TC-RIDE-010 | Select cash payment method | Positive | High |
| TC-RIDE-011 | Select online payment method | Positive | High |
| TC-RIDE-012 | Submit a valid ride request | Positive | Critical |

---

## 8. Find Driver

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-DRIVER-001 | Verify system searches for nearest available driver | Positive | Critical |
| TC-DRIVER-002 | Verify driver name is displayed | Positive | High |
| TC-DRIVER-003 | Verify driver photo is displayed | Positive | Medium |
| TC-DRIVER-004 | Verify car type is displayed | Positive | High |
| TC-DRIVER-005 | Verify license plate is displayed | Positive | High |
| TC-DRIVER-006 | Verify driver rating is displayed | Positive | Medium |
| TC-DRIVER-007 | Verify estimated driver arrival time is displayed | Positive | High |
| TC-DRIVER-008 | Contact driver using text communication | Positive | Medium |
| TC-DRIVER-009 | Contact driver using voice communication | Positive | Medium |
| TC-DRIVER-010 | Verify Start Ride button appears when driver arrives | Positive | Critical |

---

## 9. Ride Progress

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-PROGRESS-001 | Verify ride progress is displayed | Positive | Critical |
| TC-PROGRESS-002 | Verify ride cost is displayed | Positive | High |
| TC-PROGRESS-003 | Verify remaining ride time is displayed | Positive | Medium |
| TC-PROGRESS-004 | End ride early with a valid reason | Positive | High |
| TC-PROGRESS-005 | End ride early because of emergency | Positive | High |
| TC-PROGRESS-006 | Contact support during active ride | Positive | High |

---

## 10. Payment

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-PAY-001 | Pay using cash payment method | Positive | Critical |
| TC-PAY-002 | Pay using online payment method | Positive | Critical |
| TC-PAY-003 | Verify applied promo discount is displayed | Positive | High |
| TC-PAY-004 | Verify final price is displayed correctly | Positive | Critical |
| TC-PAY-005 | Complete payment using Pay Now | Positive | Critical |

---

## 11. Ride Summary & Rating

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-SUM-001 | Verify destination is displayed in ride summary | Positive | High |
| TC-SUM-002 | Verify final cost is displayed | Positive | High |
| TC-SUM-003 | Verify total ride time is displayed | Positive | Medium |
| TC-SUM-004 | Verify selected payment method is displayed | Positive | High |
| TC-SUM-005 | Submit a 1-star rating | Positive | Medium |
| TC-SUM-006 | Submit a 5-star rating | Positive | Medium |
| TC-SUM-007 | Submit review comment | Positive | Medium |
| TC-SUM-008 | Submit review using Submit Review button | Positive | High |

---

## 12. Customer Profile

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-PROFILE-001 | Verify customer full name is displayed | Positive | Medium |
| TC-PROFILE-002 | Verify customer email is displayed | Positive | Medium |
| TC-PROFILE-003 | Verify customer phone number is displayed | Positive | Medium |
| TC-PROFILE-004 | Verify profile picture is displayed | Positive | Medium |
| TC-PROFILE-005 | Edit customer personal information | Positive | High |
| TC-PROFILE-006 | Update profile picture | Positive | Medium |
| TC-PROFILE-007 | Delete customer account | Positive | Critical |

---

## 13. Customer Settings

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-SET-001 | Change application language to Arabic | Positive | Medium |
| TC-SET-002 | Change application language to English | Positive | Medium |
| TC-SET-003 | Enable ride notifications | Positive | Medium |
| TC-SET-004 | Disable ride notifications | Positive | Medium |
| TC-SET-005 | Enable payment notifications | Positive | Medium |
| TC-SET-006 | Enable offer notifications | Positive | Medium |
| TC-SET-007 | Configure privacy options | Positive | High |
| TC-SET-008 | Change application theme to Light | Positive | Low |
| TC-SET-009 | Change application theme to Dark | Positive | Low |
| TC-SET-010 | Change text size | Positive | Low |
| TC-SET-011 | Save settings changes | Positive | High |

---

## 14. Help & Support

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-SUPPORT-001 | Verify FAQ list is displayed | Positive | Medium |
| TC-SUPPORT-002 | Search for an FAQ | Positive | Medium |
| TC-SUPPORT-003 | Expand and view FAQ details | Positive | Medium |
| TC-SUPPORT-004 | Open Contact Support | Positive | High |
| TC-SUPPORT-005 | Verify support chat is opened | Positive | High |
| TC-SUPPORT-006 | Open Privacy Policy | Positive | Medium |
| TC-SUPPORT-007 | Open Terms of Service | Positive | Medium |

---

# 15. Driver Registration

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-DREG-001 | Select Driver account type | Positive | High |
| TC-DREG-002 | Enter valid personal information | Positive | High |
| TC-DREG-003 | Upload valid driver profile picture | Positive | Medium |
| TC-DREG-004 | Upload required driver documents | Positive | Critical |
| TC-DREG-005 | Enter valid vehicle information | Positive | High |
| TC-DREG-006 | Submit valid driver registration | Positive | Critical |
| TC-DREG-007 | Verify driver registration using valid OTP | Positive | Critical |
| TC-DREG-008 | Verify driver account activation | Positive | Critical |
| TC-DREG-009 | Register with missing personal information | Negative | High |
| TC-DREG-010 | Register with missing required documents | Negative | High |
| TC-DREG-011 | Register with invalid OTP | Negative | High |

---

# 16. Driver Login

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-DLOGIN-001 | Login using valid email credentials | Positive | Critical |
| TC-DLOGIN-002 | Login using valid phone credentials | Positive | Critical |
| TC-DLOGIN-003 | Login using invalid credentials | Negative | High |
| TC-DLOGIN-004 | Login with inactive driver account | Negative | Critical |
| TC-DLOGIN-005 | Login with empty required fields | Negative | Medium |

---

# 17. Driver Home

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-DHOME-001 | Verify Driver Home Screen is displayed | Positive | High |
| TC-DHOME-002 | Verify driver profile section | Positive | Medium |
| TC-DHOME-003 | Change driver availability status | Positive | Critical |
| TC-DHOME-004 | Receive ride request notification | Positive | Critical |
| TC-DHOME-005 | Verify active ride information | Positive | Critical |
| TC-DHOME-006 | View available offers and discounts | Positive | Medium |
| TC-DHOME-007 | Verify driver menu options | Positive | Medium |

---

# 18. Driver Ride Assignment

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-ASSIGN-001 | Receive ride assignment notification | Positive | Critical |
| TC-ASSIGN-002 | Verify ride details in assignment notification | Positive | Critical |
| TC-ASSIGN-003 | Verify assigned client information | Positive | High |

---

# 19. Driver Pre-Trip

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-PRETRIP-001 | Verify client information before trip | Positive | High |
| TC-PRETRIP-002 | Chat with client | Positive | Medium |
| TC-PRETRIP-003 | Open Google Maps navigation | Positive | High |
| TC-PRETRIP-004 | End trip before reaching client | Positive | High |

---

# 20. Driver In-Trip

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-INTRIP-001 | Verify client information during trip | Positive | High |
| TC-INTRIP-002 | Verify route map is displayed | Positive | Critical |
| TC-INTRIP-003 | End trip midway | Positive | High |
| TC-INTRIP-004 | Contact support during trip | Positive | High |
| TC-INTRIP-005 | Use emergency button | Positive | Critical |
| TC-INTRIP-006 | End trip successfully | Positive | Critical |

---

# 21. Driver End Trip

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-ENDTRIP-001 | Verify trip summary after ending trip | Positive | High |
| TC-ENDTRIP-002 | Verify rating section after trip completion | Positive | Medium |

---

# 22. Driver Packages & Subscriptions

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-SUB-001 | View available packages | Positive | High |
| TC-SUB-002 | View package details | Positive | High |
| TC-SUB-003 | Apply valid promo code to package | Positive | High |
| TC-SUB-004 | Apply invalid promo code to package | Negative | High |
| TC-SUB-005 | Subscribe to available package | Positive | Critical |
| TC-SUB-006 | Complete subscription payment | Positive | Critical |
| TC-SUB-007 | Confirm subscription | Positive | Critical |
| TC-SUB-008 | Subscribe without promo code | Positive | High |
| TC-SUB-009 | Manage active subscription | Positive | High |
| TC-SUB-010 | View active subscriptions | Positive | High |
| TC-SUB-011 | View driver subscription payment information | Positive | High |
| TC-SUB-012 | View driver earnings | Positive | High |

---

# 23. Driver Menu

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-DMENU-001 | Filter trips using available trip filters | Positive | Medium |
| TC-DMENU-002 | Open Offers & Discounts | Positive | Medium |
| TC-DMENU-003 | Open Driver Settings | Positive | Medium |
| TC-DMENU-004 | Open Driver Profile | Positive | Medium |

---

# 24. Admin Dashboard

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-ADMIN-001 | Verify Admin Dashboard Overview is displayed | Positive | Critical |
| TC-ADMIN-002 | Verify Revenue Overview is displayed | Positive | High |
| TC-ADMIN-003 | Verify Driver Availability information | Positive | High |
| TC-ADMIN-004 | Verify Pending Trip Requests | Positive | Critical |
| TC-ADMIN-005 | Verify Alerts and Notifications | Positive | High |
| TC-ADMIN-006 | Open Driver Management | Positive | Critical |
| TC-ADMIN-007 | Open User Management | Positive | Critical |
| TC-ADMIN-008 | Open Payment Management | Positive | Critical |
| TC-ADMIN-009 | Open Trip Management | Positive | Critical |
| TC-ADMIN-010 | Open Offers & Discounts Management | Positive | High |
| TC-ADMIN-011 | Open Support & Help Desk | Positive | High |
| TC-ADMIN-012 | Open System Settings | Positive | High |
| TC-ADMIN-013 | Open Financial Reports | Positive | Critical |

---

# 25. Admin Driver Management

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-ADM-DRV-001 | View driver management section | Positive | High |
| TC-ADM-DRV-002 | View driver availability | Positive | High |
| TC-ADM-DRV-003 | View driver information | Positive | High |
| TC-ADM-DRV-004 | Monitor pending driver-related requests | Positive | High |

---

# 26. Admin User Management

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-ADM-USR-001 | View user management section | Positive | High |
| TC-ADM-USR-002 | View user information | Positive | High |
| TC-ADM-USR-003 | Monitor user-related operations | Positive | High |

---

# 27. Admin Payment Management

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-ADM-PAY-001 | View payment management section | Positive | Critical |
| TC-ADM-PAY-002 | View driver subscription payments | Positive | High |
| TC-ADM-PAY-003 | View payment information | Positive | High |

---

# 28. Admin Trip Management

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-ADM-TRIP-001 | View trip management section | Positive | Critical |
| TC-ADM-TRIP-002 | View pending trip requests | Positive | Critical |
| TC-ADM-TRIP-003 | Monitor trip information | Positive | High |

---

# 29. Admin Offers & Promo Code Management

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-ADM-OFFER-001 | View offers management | Positive | High |
| TC-ADM-OFFER-002 | View promo code management | Positive | High |
| TC-ADM-OFFER-003 | Verify available offer information | Positive | Medium |

---

# 30. Admin Support & Help Desk

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-ADM-SUP-001 | Open Support & Help Desk | Positive | High |
| TC-ADM-SUP-002 | View support-related information | Positive | High |

---

# 31. Admin System Settings

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-ADM-SET-001 | Open System Settings | Positive | High |
| TC-ADM-SET-002 | Verify system configuration information | Positive | High |

---

# 32. Admin Financial Reports

| ID | Test Case | Type | Priority |
|---|---|---|---|
| TC-ADM-FIN-001 | Open Financial Reports | Positive | Critical |
| TC-ADM-FIN-002 | Verify Revenue information is available | Positive | Critical |
| TC-ADM-FIN-003 | Verify Driver Earnings information is available | Positive | High |

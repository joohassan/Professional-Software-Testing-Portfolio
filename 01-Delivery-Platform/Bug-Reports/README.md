# Delivery Platform - Bug Reports

## Bug Report Template

### Bug ID
BUG-XXX

### Title
[Short and clear bug title]

### Module
[Registration / Login / Ride Request / Payment / Driver / Admin / etc.]

### Severity
[Critical / High / Medium / Low]

### Priority
[High / Medium / Low]

### Environment
- Platform:
- Browser / Device:
- OS:
- App Version:

### Preconditions
- [Required conditions before reproducing the bug]

### Test Data
- [Data used during testing]

### Steps to Reproduce
1. 
2. 
3. 
4. 

### Expected Result
[What should happen according to the requirement]

### Actual Result
[What actually happened]

### Reproducibility
[Always / Sometimes / Once]

### Status
[New / Open / In Progress / Fixed / Retest / Closed / Reopened]

### Attachments
- Screenshot:
- Video:
- Logs:

---

## Example Bug Report

### Bug ID
BUG-001

### Title
Registration form accepts an invalid email address

### Module
Customer Registration

### Severity
High

### Priority
High

### Environment
- Platform: Web / Mobile
- Browser / Device: Not Specified
- OS: Not Specified
- App Version: Not Specified

### Preconditions
- User is on the Registration page.

### Test Data
- Invalid email: `user@`

### Steps to Reproduce
1. Open the Registration page.
2. Enter valid data in the other required fields.
3. Enter `user@` in the Email field.
4. Click Register.

### Expected Result
The system should reject the invalid email address and display a validation message.

### Actual Result
The system accepts the invalid email address.

### Reproducibility
Always

### Status
New

### Attachments
- Screenshot: Not Available
- Video: Not Available
- Logs: Not Available

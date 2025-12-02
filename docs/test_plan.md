#  Test Cases

---

## 1. User Signup (JWT + bcrypt)
**Precondition:** None  
**Steps:**  
- Submit signup form with valid information  
- Verify email  
**Expected Result:**  
- User account created  
- Password hashed  
- Email verification required  
**Priority:** High

---

## 2. Login Authentication
**Precondition:** Verified user exists  
**Steps:**  
- Login with correct credentials  
**Expected Result:**  
- JWT returned with user ID and role  
**Priority:** High

---

## 3. RBAC – Unauthorized Access Block
**Precondition:** Patient logged in  
**Steps:**  
- Patient tries accessing admin-only route  
**Expected Result:**  
- API returns 403 Forbidden  
**Priority:** High

---

## 4. Add Doctor (Admin Only)
**Precondition:** Admin authenticated  
**Steps:**  
- Admin submits doctor details  
**Expected Result:**  
- Doctor profile created  
**Priority:** High

---

## 5. Doctor Deactivation
**Precondition:** Doctor has future appointments  
**Steps:**  
- Admin deactivates doctor  
**Expected Result:**  
- New bookings blocked  
- Future appointment patients notified  
**Priority:** High

---

## 6. Add Clinic
**Precondition:** Admin authenticated  
**Steps:**  
- Admin adds a clinic  
**Expected Result:**  
- Clinic visible in search and assignment  
**Priority:** High

---

## 7. Search Doctor & View Slots
**Precondition:** Doctors, clinics, and slots exist  
**Steps:**  
- Patient searches for doctor  
- Patient views available slots  
**Expected Result:**  
- Active doctors & clinics shown  
- Available slots displayed  
**Priority:** High

---

## 8. Create Slot Lock
**Precondition:** Slot available  
**Steps:**  
- Patient selects a slot  
**Expected Result:**  
- Slot locked  
- Other users cannot select same slot  
**Priority:** High

---

## 9. Confirm Booking
**Precondition:** Slot lock exists  
**Steps:**  
- Patient confirms booking  
**Expected Result:**  
- Appointment created  
- Slot marked as booked  
- Lock removed  
- Notifications sent  
**Priority:** High

---

## 10. Prevent Double Booking
**Precondition:** Two users attempt same slot  
**Steps:**  
- Both try to book simultaneously  
**Expected Result:**  
- One booking succeeds  
- Other receives conflict (409)  
**Priority:** High

---

## 11. Cancel Appointment (Patient)
**Precondition:** Active appointment exists  
**Steps:**  
- Patient cancels appointment  
**Expected Result:**  
- Status becomes Cancelled  
- Slot becomes available  
- Doctor notified  
**Priority:** High

---

## 12. Doctor Day-wise Appointment View
**Precondition:** Doctor has scheduled appointments  
**Steps:**  
- Doctor checks schedule for a specific date  
**Expected Result:**  
- All appointments listed  
**Priority:** High

---

## 13. Token Expired Access
**Precondition:** Expired JWT  
**Steps:**  
- Call protected API with expired token  
**Expected Result:**  
- System returns 401 Unauthorized  
**Priority:** High

---



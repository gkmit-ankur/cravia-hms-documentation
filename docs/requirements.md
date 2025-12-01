#  Functional & Non-Functional Requirements

## Functional Requirements

| **ID** | **Functionality** | **Description** | 
|--------|------------------|----------------|
| FR-1 | Authentication | JWT-based signup/login for Admin, Doctor, and Patient |
| FR-2 | Doctor Management| Admin manages doctor accounts, availability, and status |
| FR-3 | clinic Management| Fetch and display detail of clinic data  |
| FR-4 | Appointments Management | Patients book/manage appointments; doctors view/manage schedules |
| FR-5 | Health Education & Articles | Stores health related articles like good nurtition |


## **FR-1: Authentication**
- Secure signup/login using JWT  
- Password encryption (bcrypt)  
- Email verification  
- Role based Access control 
- Token validation for protected routes 


## **FR-2: Doctor Management (Admin Role)**
- Add new doctor profiles  
- Update doctor information  
- Assign doctors to clinics  
- Deactivate/reactivate doctors  
- Search doctors by specialty, name, or status.  


## **FR-3: Clinic Management (Admin Role)**
- Add clinics with name, address, timings  
- Update clinic details  
- Disable/enable clinics  

## **FR-4: Appointment Management**

### Patients
- Search doctors  
- Book clinic-based time-slot appointments  
- Cancel or reschedule appointments  
- View:
     - Upcoming appointments  
     - Doctor-wise appointments  
     - Clinic-wise appointments  

### Doctors
- View day-wise appointment list   
- Cancel appointments with reason  

### System Handling
- Appointment statuses:
    - Pending  
    - Confirmed  
    - Completed  
    - Cancelled  
- Real-time slot locking to avoid double booking  
- Notifications for status updates 


## **FR-5: Health Education & Articles**
### Doctors
- Publish articles on nutrition, disease prevention, mental health, etc.  
- Edit and delete previously posted articles  

### Patient
- Browse and read health education articles  
- Search articles by category 

---

## Non-Functional Requirements

- **Performance**:The system should provide fast response times.  
- **Security**:All data should be secure to protect user privacy and system integrity.  

___

## **Workflows & Sequence Summaries**

## Booking Sequence
1. Patient -> Search -> select doctor -> select slot -> Confirm booking
2. System -> Lock slot -> Create appointment record -> Notify doctor & patient
3. Doctor -> Sees appointment on daily list

## Cancellation by Patient
1. Patient -> Cancel request
2. System  -> mark appointment cancelled -> free slot -> notify doctor

## Doctor Deactivation 
1. Admin -> Deactivate doctor
2. System -> Block new bookings for doctor
3. System -> Check future appointments -> notify patients + admin -> follow chosen business rule

___

## **Future Scope**. 
- Prescription Management: Allow doctors to upload prescriptions digitally.  
- Payment Gateway: Add secure online payment for appointments.     

---
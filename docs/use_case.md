# Bussiness Use case.    

The Cravia healthcare provides a centralized platform for handling all operations related to health like cure,awareness and booking appointment with the doctors. 

- **Doctor Management**    
This maintains all the information of the doctor,including their qualifications,specializations, experience, and availability. 
  
- **Appointment Booking System**.  
Paintent can book appointments through the platform by selecting the doctor based on the diseases you are suffering.  

  

# Functional Use Case

This section describes the key use cases of the **Healthcare Management System**, outlining the actors, goals and main flows for each major function.

---
### UC-01: Patient — Register & Login
**Actor:** Patient  
**Goal:** Create account and access patient features.  
**Flow:** Signup → Email verification → Login (JWT issued).

### UC-02: Patient — Search & View Doctors
**Actor:** Patient  
**Goal:** Find a doctor by name, clinic.  
**Flow:** Search → View doctor profile → See clinic  & available slots.

### UC-03: Patient — Book Appointment
**Actor:** Patient  
**Goal:** Book a slot with a doctor at a clinic.  
**Flow:** Select doctor → Select clinic → Select available slot → Confirm booking → Notifications sent.

### UC-04: Patient — Cancel / Reschedule Appointment
**Actor:** Patient  
**Goal:** Cancel or change a booked appointment.  
**Flow:** Choose appointment → Cancel/Reschedule → System enforces cancellation policy → Update status & notify doctor.

### UC-05: Doctor — View Day-wise Appointments
**Actor:** Doctor  
**Goal:** See all appointments for a date.  
**Flow:** Open schedule → Select date → System lists appointments (time, patient, notes).

### UC-06: Doctor — Cancel Appointment
**Actor:** Doctor  
**Goal:** Cancel an appointment (e.g., emergency).  
**Flow:** Select appointment → Cancel with reason → System notifies patient.

### UC-07: Admin — Add Clinic
**Actor:** Admin  
**Goal:** Make a clinic available in the system.  
**Flow:** Create clinic record → Clinic visible for doctor assignment and patient search.

### UC-08: Admin — Add / Deactivate Doctor
**Actor:** Admin  
**Goal:** Add new doctors and manage their active status.  
**Flow:** Create doctor profile → Assign clinic(s) → Optionally deactivate → System blocks new bookings if deactivated.


---


##  Conclusion

Cravia Healthcare represents the future of digital healthcare — merging accessibility, education, and personalized medical services in one platform.  
By connecting patients and doctors directly, it encourages **better health management**, **early diagnosis**, and **greater health awareness**.

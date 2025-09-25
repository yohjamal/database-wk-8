# database-wk-8
# 🏥 Clinic Booking System Database

## 📌 Project Overview
This project implements a **relational database schema** for a **Clinic Booking System**.  
The system is designed to manage patients, doctors, appointments, and prescribed medications in a structured and efficient way.

It demonstrates the use of:
- Well-structured tables
- Primary and foreign key constraints
- One-to-Many and Many-to-Many relationships
- SQL best practices for data integrity

---

## 📂 Database Schema

### 1. **Patients**
Stores patient details.  
- Primary Key: `patient_id`  
- Unique constraints: `phone`, `email`

### 2. **Doctors**
Stores doctor details.  
- Primary Key: `doctor_id`  
- Unique constraints: `phone`, `email`

### 3. **Appointments**
Links patients and doctors, stores booking details.  
- Primary Key: `appointment_id`  
- Foreign Keys: `patient_id` → Patients, `doctor_id` → Doctors  
- Relationship: One Patient → Many Appointments, One Doctor → Many Appointments  

### 4. **Medications**
List of medications prescribed to patients.  
- Primary Key: `medication_id`  
- Unique constraint: `medication_name`

### 5. **PatientMedications**
Resolves Many-to-Many between Patients and Medications.  
- Composite Primary Key: (`patient_id`, `medication_id`)  
- Foreign Keys: `patient_id` → Patients, `medication_id` → Medications  

---

## ⚙️ How to Use

1. **Clone the repository** or download the `.sql` file.
2. Open MySQL Workbench or any SQL client.
3. Run the script:
   ```sql
   SOURCE clinic_booking.sql;


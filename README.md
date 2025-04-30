# Hospital Management System Database

A comprehensive SQL database system designed to manage hospital operations including patient records, appointments, admissions, medical tests, and billing.

## Features

- **Patient Management**: Track patient details, contacts, and medical history.
- **Staff Management**: Manage employee records, qualifications, and department assignments.
- **Appointment Scheduling**: Handle appointments with disease tracking and prescriptions.
- **Admission System**: Manage room allocations and patient admissions.
- **Medical Tests**: Record test results and associate them with patients.
- **Billing System**: Generate invoices with cost tracking.
- **Role-Based Access Control**: Secure roles with specific permissions (Doctor, Nurse, Receptionist, etc.).

## Database Schema Details

### Tables

#### **PATIENT**
- `PATIENT_ID` (PK)
- `PATIENT_NAME`, `PATIENT_AGE`, `GENDER`

#### **EMPLOYEE**
- `EMPLOYEE_ID` (PK)
- `EMPLOYEE_NAME`, `DEPARTMENT`, `DESIGNATION`, `ROOM_ID` (FK)

#### **APPOINTMENT**
- `APPOINTMENT_ID` (PK)
- `EMPLOYEE_ID` (FK), `PATIENT_ID` (FK), `APPOINTMENT_DATE`

#### **ADMISSION**
- `ADMISSION_ID` (PK)
- `APPOINTMENT_ID` (FK), `ROOM_ID` (FK), Admission/Discharge Dates

#### **TEST**
- `TEST_ID` (PK)
- `TEST_NAME`, `TEST_COST`

#### **INVOICE**
- `INVOICE_ID` (PK)
- `PATIENT_ID` (FK), `COST`, `PAYMENT_METHOD`

*[Full schema in SQL script]*

## Installation & Setup

1. **Run SQL Script**:
   ```sql
   USE Hospital_Management_System;
   -- Execute provided SQL script to create tables, views, roles, and sample data

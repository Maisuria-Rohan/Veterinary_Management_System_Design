# Veterinary Management System Design
## Overview
This project presents the full analysis and design of a Veterinary Information and Management System built to improve data centralization, appointment scheduling, billing accuracy, inventory tracking, and customer communication for a veterinary clinic.<br>

The system was designed using formal software engineering methods across the Planning, Analysis, and Design phases of the SDLC.<br>

The goal was to create a structured, maintainable, and scalable solution that reduces manual errors and improves operational efficiency.<br>

## Problem 
The clinic relied on spreadsheets, manual scheduling, and disconnected systems. 
This created:
 - Medical record inconsistencies
 - Missed or double-booked appointments
 - Manual billing errors
 - Poor inventory tracking
 - Limited data accessibility<br>

The lack of integration increased administrative workload and introduced data reliability risks.<br>

## Proposed Solution
**The designed system centralizes**:
 - Pet medical records
 - Appointment scheduling
 - Billing and payment tracking
 - Inventory management
 - Customer communication<br>

The system uses role-based access and structured data relationships to ensure secure and organized operations.<br>

## Key Features Designed
 - Role-based access for Staff, Vet, and Pet Owner
 - Centralized pet medical record management
 - Online appointment booking with reminders
 - Automated invoice generation and payment tracking
 - Real-time inventory tracking with low-stock alerts
 - Secure authentication and data validation
 - Structured customer communication support

## System Architecture and Design
### Use Case Diagram
<img width="1856" height="1304" alt="Screenshot 2026-02-18 at 4 19 32 PM" src="https://github.com/user-attachments/assets/08d913a5-ebe2-4800-8e05-0c1c2ab66100" /><br>

The use case diagram defines system behavior from the perspective of external actors.<br>

**Actors**:
 - Pet Owner – books appointments, views bills, accesses records
 - Vet – manages medical records and treatment information
 - Staff – manages scheduling, billing, and inventory
  <br>


### System Behavior
**Key interactions include**:<br>
Manage Pet Record<br>
   - Manage Medication Record
   - Manage Vaccination Record<br>

Book Appointment<br>
  - Includes schedule checking and can trigger follow-up reminders.<br>

Manage Inventory<br>
  - Extends to "Send Low Inventory Alert", showing conditional behavior.<br>

Bill Customer and Pay Bill<br>
  - Staff generate invoices, and pet owners complete payments through the portal.<br>
 <br>
 
**Design concepts demonstrated**:
- Generalization
- Include relationships
- Extend relationships
- System boundary definition<br>
This shows structured requirement modeling and controlled feature interactions.

---

### Class Diagram
<img width="2256" height="1350" alt="Screenshot 2026-02-18 at 4 19 51 PM" src="https://github.com/user-attachments/assets/34337ff2-d4df-42de-8d7e-23138b453dfc" /><br>
The class diagram models the internal system structure and object relationships.<br>

**Core system classes include**:<br>
PetRecord
   - Stores pet medical data.
   - Extended by MedicationRecord and VaccinationRecord using inheritance.
Appointment
   - Manages booking, rescheduling, reminders, and schedule validation.
Bill
   - Handles invoice generation, service tracking, and payment status.
Inventory
   - Tracks supplies and supports low-stock alerts.
CustomerPortal
   - Provides authenticated access for pet owners.
Employee, Staff, Vet
   - Base class extended by Staff and Vet using inheritance.

### Key Design Concepts Demonstrated
**Inheritance**
- Employee → Staff / Vet
- PetRecord → MedicationRecord / VaccinationRecord

**Associations**
- Appointments linked to Staff and CustomerPortal
- Bills linked to Staff and CustomerPortal

**Multiplicity**
- Many-to-many relationship between Inventory and Staff
- One-to-one relationship between PetOwner and CustomerPortal

**Encapsulation of behavior**
- Methods such as addRecord, reschedule, addService reflect system operations

This diagram reflects object-oriented design principles and data flow control.

---

## Process Followed
1. Conducted stakeholder interviews to identify inefficiencies 
2. Defined business needs and objectives 
3. Developed functional and non-functional requirements 
4. Created UML use case and class diagrams 
5. Revised diagrams based on design feedback 

## What I Learned
 - Translating business problems into structured system requirements
 - Writing formal SRS documentation
 - Designing UML use case and class diagrams
 - Modeling multiplicity, inheritance, and system boundaries
 - Applying SDLC phases in a real-world scenario
 - Thinking in terms of architecture before implementation

## Documentation
[VIMS_FinalReport.docx.pdf](https://github.com/user-attachments/files/25379261/VIMS_FinalReport.docx.pdf)<br>
[Class and Use Class Diagram .pdf](https://github.com/user-attachments/files/25379264/Class.and.Use.Class.Diagram.pdf)<br>



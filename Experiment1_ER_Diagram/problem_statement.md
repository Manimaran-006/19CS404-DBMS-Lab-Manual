# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.

---

# Scenario A: City Fitness Club Management

**Business Context:**  
FlexiFit Gym wants a database to manage its members, trainers, and fitness programs.

**Requirements:**  
- Members register with name, membership type, and start date.  
- Each member can join multiple programs (Yoga, Zumba, Weight Training).  
- Trainers assigned to programs; a program may have multiple trainers.  
- Members may book personal training sessions with trainers.  
- Attendance recorded for each session.  
- Payments tracked for memberships and sessions.

### ER Diagram:
<img width="1310" height="817" alt="image" src="https://github.com/user-attachments/assets/e02c9bdf-d34c-4957-a25e-37e21478dd3f" />


### Entities and Attributes
<img width="2125" height="740" alt="Dark Database Schema Table" src="https://github.com/user-attachments/assets/8f8cbf58-a6de-4f84-ae10-4d7a055e6e89" />


<img width="797" height="306" alt="image" src="https://github.com/user-attachments/assets/31ef937c-b32b-49f6-b9da-1d336469b475" />


### Assumptions

1.Each session involves exactly one trainer and one member.
2.Programs are predefined (Yoga, Zumba, Weight Training, etc.).
3.Payments are only for membership or session bookings.

---

# Scenario B: City Library Event & Book Lending System

**Business Context:**  
The Central Library wants to manage book lending and cultural events.

**Requirements:**  
- Members borrow books, with loan and return dates tracked.  
- Each book has title, author, and category.  
- Library organizes events; members can register.  
- Each event has one or more speakers/authors.  
- Rooms are booked for events and study.  
- Overdue fines apply for late returns.

### ER Diagram:
<img width="1220" height="896" alt="image" src="https://github.com/user-attachments/assets/1912c96d-1ea0-4087-8b35-46d951494800" />


### Entities and Attributes

<img width="830" height="292" alt="image" src="https://github.com/user-attachments/assets/ce50422e-f998-463f-9462-3eba62fe0164" />


### Relationships and Constraints

<img width="716" height="167" alt="image" src="https://github.com/user-attachments/assets/f291096f-45ef-4864-88c3-43fa31de82cb" />


### Assumptions
1.Books can be borrowed multiple times by different Members.
2.Each Event happens in one Room at a specific time.
3.A Speaker can participate in multiple Events.

---

# Scenario C: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**  
- Customers can reserve tables or walk in.  
- Each reservation includes date, time, and number of guests.  
- Customers place food orders linked to reservations.  
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).  
- Bills generated per reservation, including food and service charges.  
- Waiters assigned to serve reservations.

### ER Diagram:
<img width="1163" height="700" alt="image" src="https://github.com/user-attachments/assets/d0026981-8646-4497-b58e-f710af13ea3f" />


### Entities and Attributes

<img width="860" height="261" alt="image" src="https://github.com/user-attachments/assets/81cde94b-4364-468e-ae10-fb31720701e0" />


### Relationships and Constraints

<img width="710" height="210" alt="image" src="https://github.com/user-attachments/assets/809af941-008c-4a4b-8172-b901b6ffca65" />


### Assumptions

1.One reservation uses one table and one waiter.
2.Bill is generated automatically after service.
3.Customer details stored for every reservation.

---

## Instructions for Students

1. Complete **all three scenarios** (A, B, C).  
2. Identify entities, relationships, and attributes for each.  
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-drawn & scanned.  
4. Fill in all tables and assumptions for each scenario.  
5. Export the completed Markdown (with diagrams) as **a single PDF**

# Database Normalization for Airbnb Clone

## Introduction

Normalization is the process of organizing data in a database to reduce redundancy and improve data integrity. The goal is to ensure the database is in **Third Normal Form (3NF)**. Below is a step-by-step explanation of how we achieved normalization in our Airbnb Clone project.

---

## Step 1: First Normal Form (1NF)

**Criteria**:

- Eliminate repeating groups
- Ensure atomic (indivisible) values

**Action Taken**:

- Split composite fields (e.g., full name) into first name and last name.
- Ensured each field contains a single value (e.g., multiple property images stored in a separate table rather than one column).

---

## Step 2: Second Normal Form (2NF)

**Criteria**:

- Be in 1NF
- Remove partial dependencies (i.e., every non-key attribute is fully functionally dependent on the primary key)

**Action Taken**:

- Separated properties from users into their own tables.
- Created a `Bookings` table where each booking references both a user and a property.

---

## Step 3: Third Normal Form (3NF)

**Criteria**:

- Be in 2NF
- Remove transitive dependencies (non-key attributes depend only on the key)

**Action Taken**:

- Moved payment details (e.g., amount, payment date) to a separate `Payments` table.
- Separated reviews into their own table with foreign keys referencing users and properties.

---

## Final Tables

- Users
- Properties
- Bookings
- Payments
- Reviews
- Property_Images

This structure avoids data duplication, ensures data integrity, and improves scalability.

---

## Conclusion

By normalizing the Airbnb Clone database to 3NF, we ensured it is optimized for real-world use cases such as searching, filtering, and reporting, while avoiding anomalies during insert, update, or delete operations.

# Airbnb Clone Project

## Project Overview

The Airbnb Clone Project is a full-stack development simulation aimed at building a scalable web application that mimics core Airbnb functionalities. It focuses on backend systems, database design, application security, and CI/CD practices. This project enhances teamwork, problem-solving, and technical implementation in a real-world development context.

**Tech Stack:** Django, MySQL, GraphQL, Docker, GitHub Actions.

---

## 1. Team Roles

| Role                       | Responsibility                                                                  |
| -------------------------- | ------------------------------------------------------------------------------- |
| **Backend Developer**      | Implements business logic, API endpoints, and integrates with the database.     |
| **Database Administrator** | Designs and manages the relational database schema and ensures data integrity.  |
| **DevOps Engineer**        | Sets up CI/CD pipelines, Docker containers, and ensures smooth deployments.     |
| **Security Specialist**    | Ensures security standards for APIs, user data, and server configurations.      |
| **Project Manager**        | Coordinates team activities, timelines, and ensures project milestones are met. |

---

## 2. Technology Stack

| Technology         | Purpose                                                                       |
| ------------------ | ----------------------------------------------------------------------------- |
| **Django**         | Web framework for building RESTful APIs and handling backend logic.           |
| **MySQL**          | Relational database used to store structured application data.                |
| **GraphQL**        | API query language for flexible and efficient data retrieval.                 |
| **Docker**         | Containerization tool for consistent development and deployment environments. |
| **GitHub Actions** | Automates testing, builds, and deployment processes via CI/CD pipelines.      |

---

## 3. Database Design

### Key Entities

- **User**

  - Fields: id, name, email, password, role
  - Relationships: One user can own many properties and make many bookings.

- **Property**

  - Fields: id, owner_id (FK), title, description, location
  - Relationships: Each property belongs to a user (owner) and has multiple bookings and reviews.

- **Booking**

  - Fields: id, user_id (FK), property_id (FK), start_date, end_date
  - Relationships: Belongs to one user and one property.

- **Review**

  - Fields: id, user_id (FK), property_id (FK), rating, comment
  - Relationships: Linked to both user and property.

- **Payment**
  - Fields: id, booking_id (FK), amount, status, transaction_date
  - Relationships: Tied to a specific booking.

---

## 4. Feature Breakdown

- **User Management**

  - Users can register, log in, and manage their profile. Authentication and role-based access control are enforced.

- **Property Management**

  - Hosts can list properties, update descriptions, set prices, and manage availability.

- **Booking System**

  - Users can view property listings, make bookings, and receive booking confirmations.

- **Reviews**

  - After a stay, users can leave reviews with ratings and comments.

- **Payment Integration**
  - Secure payment gateway simulation for processing transactions and storing history.

---

## 5. API Security

- **Authentication**

  - JWT-based token authentication to verify user identity before accessing protected routes.

- **Authorization**

  - Role-based permissions to restrict access (e.g., only hosts can list properties).

- **Rate Limiting**
  - Limits on API request rates to prevent abuse or denial-of-service attacks.

**Why It Matters:**

- Protects user data and ensures only authorized users perform sensitive actions.
- Prevents financial fraud and maintains platform trust.
- Guards against brute-force attacks and system overload.

---

## 6. CI/CD Pipeline

CI/CD (Continuous Integration and Continuous Deployment) ensures code changes are automatically tested and deployed.

- **CI Tools:** GitHub Actions for running tests, linting code, and building images.
- **CD Tools:** Docker for containerizing the application; GitHub Actions for deployment automation.

**Importance:**

- Improves development efficiency and collaboration.
- Minimizes human error and ensures reliable, repeatable deployment.

---

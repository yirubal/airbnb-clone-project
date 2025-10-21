# Airbnb Clone Project

## 🏠 About the Project
The **Airbnb Clone Project** is a comprehensive full-stack web application designed to replicate the core functionalities of the Airbnb platform. It provides learners with a hands-on experience in backend architecture, database design, API development, and application security.  
The project simulates real-world software development processes and team collaboration to build a scalable, secure, and production-ready booking system.

---

## 🎯 Project Goals
1. **User Management:** Secure user registration, authentication, and profile management.  
2. **Property Management:** Create, update, and retrieve property listings.  
3. **Booking System:** Allow users to reserve properties and manage booking details.  
4. **Payment Processing:** Integrate payment gateway for handling transactions.  
5. **Review System:** Enable users to post and manage property reviews.  
6. **Data Optimization:** Ensure fast and efficient data access through indexing and caching.

---

## 👥 Team Roles
### Backend Developer
Responsible for implementing RESTful and GraphQL API endpoints, defining database schemas, and building the business logic. Ensures API performance and proper integration between services.

### Database Administrator
Designs and manages the PostgreSQL database schema. Handles indexing, normalization, and optimization for performance and scalability.

### DevOps Engineer
Manages the deployment process, sets up Docker containers, and configures CI/CD pipelines. Ensures scalability, uptime, and environment consistency across development and production.

### QA Engineer
Creates and executes automated and manual test plans to ensure the reliability of APIs and system functionalities. Verifies bug fixes and validates new features before deployment.

---

## ⚙️ Technology Stack
| Technology | Purpose |
|-------------|----------|
| **Django** | High-level Python web framework for building the backend logic and RESTful APIs. |
| **Django REST Framework (DRF)** | Simplifies API development with authentication, serialization, and permissions handling. |
| **PostgreSQL** | Primary relational database used for storing user, property, booking, and payment data. |
| **GraphQL** | Provides flexible, efficient querying of data with a single endpoint for complex data retrieval. |
| **Celery** | Handles background and asynchronous tasks like sending emails and processing payments. |
| **Redis** | Used as a cache layer and message broker for Celery tasks. |
| **Docker** | Provides containerization for consistent development and production environments. |
| **CI/CD Pipelines** | Automates testing, integration, and deployment using tools like GitHub Actions. |

---

## 🧩 Database Design
### Key Entities
1. **Users**
   - Fields: `id`, `username`, `email`, `password`, `profile_photo`, `date_joined`
   - Relation: Can own multiple properties and make multiple bookings.

2. **Properties**
   - Fields: `id`, `title`, `description`, `price_per_night`, `location`, `owner_id`
   - Relation: Belongs to a user (owner) and can have multiple bookings and reviews.

3. **Bookings**
   - Fields: `id`, `property_id`, `user_id`, `check_in_date`, `check_out_date`, `status`
   - Relation: Belongs to both a property and a user.

4. **Payments**
   - Fields: `id`, `booking_id`, `amount`, `payment_status`, `timestamp`
   - Relation: Linked to a specific booking.

5. **Reviews**
   - Fields: `id`, `property_id`, `user_id`, `rating`, `comment`, `created_at`
   - Relation: Each review belongs to both a user and a property.

---

## 🚀 Feature Breakdown
### 1. User Management
Allows users to register, log in, update profiles, and securely manage authentication tokens.  
Essential for personalizing user experiences and protecting access to data.

### 2. Property Management
Hosts can create, edit, and delete property listings, while guests can view and search listings.  
This feature forms the core marketplace functionality of the platform.

### 3. Booking System
Users can book available properties and view or cancel their bookings.  
Manages check-in/check-out dates and ensures booking conflicts are prevented.

### 4. Payment Processing
Handles secure online payments for property bookings.  
Supports transaction recording and refund mechanisms.

### 5. Review System
Enables users to rate and review properties after their stay.  
Helps maintain transparency and trust between hosts and guests.

### 6. Database Optimization
Implements indexing and caching to improve query speed and reduce load on PostgreSQL.  
Ensures smooth performance even under heavy user traffic.

---

## 🔒 API Security
Security is a top priority in this project to ensure data integrity and user protection.

- **Authentication:** Implemented using JWT (JSON Web Tokens) to verify user identity for each API request.  
- **Authorization:** Ensures users can only access their own data and actions (e.g., only a host can edit their property).  
- **Rate Limiting:** Prevents abuse of APIs and denial-of-service attacks.  
- **Data Encryption:** Sensitive user data (passwords, payment info) is encrypted using Django’s hashing mechanisms and HTTPS connections.  
- **Importance:** Security measures safeguard user trust, financial data, and ensure compliance with privacy regulations.

---

## ⚡ CI/CD Pipeline
**Continuous Integration/Continuous Deployment (CI/CD)** automates testing and deployment to maintain reliability and consistency.

- **Purpose:**  
  - Detect bugs early through automated tests.  
  - Ensure smooth deployment with minimal downtime.  
  - Maintain consistent environments across development and production.

- **Tools Used:**  
  - **GitHub Actions:** Automates code testing and deployment workflows.  
  - **Docker:** Ensures consistent environment configuration across all stages.  
  - **Celery + Redis:** Manage background task queues during deployment processes.

---

## 📘 License
This project is for educational purposes as part of the ALX Software Engineering program.

---

## 👨‍💻 Author
**Gedion Girma**  
[GitHub Repository: airbnb-clone-project](https://github.com/yirubal/airbnb-clone-project)


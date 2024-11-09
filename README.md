# Learn-Nest


# Overview

This project is a backend service built with Java and Spring Boot, designed to manage user data, skills, scheduling, and integration with Google Calendar. The backend provides a RESTful API to handle various user-related tasks, including authentication, skill listings, and scheduling appointments.

# Key Features

**User Authentication:** Secure user login and authentication using Spring Security.

**Google Calendar Integration:** Enables appointment scheduling and management 
through integration with Google Calendar.

**REST API Endpoints:** Provides endpoints for managing users, skills, availability, 

appointments, and notifications.

**Database Management:** MySQL database with structured tables and relationships to maintain data integrity.

# Technologies Used

**Java:** Core language for backend logic.

**Spring Boot:** Simplifies setup, configuration, and provides tools for rapid 

backend development.

**Spring Data JPA / Hibernate:** Manages database interactions with MySQL.

**Spring Security:** Provides user authentication and authorization.

**Google API Java Client:** Facilitates integration with Google Calendar for 
appointment scheduling.

**MySQL:** Relational database for storing user data, skills, appointments, and availability.

# Project Setup

Prerequisites

Java (version 11 or higher)

Maven (for dependency management)

MySQL (for database storage)

Google Developer Account (to set up API credentials for Google Calendar)

# Installation

**1.Clone the Repository:**

git clone https://github.com/your-username/project-repo.git

cd project-repo

**2.Set up MySQL Database:**

spring.datasource.url=jdbc:mysql://localhost:3306/user_management
spring.datasource.username=yourUsername
spring.datasource.password=yourPassword

**3.Google Calendar API Setup:**

Obtain API credentials from the Google Developer Console.
Download the credentials file and place it in the src/main/resources directory.

**4.Build and Run:**

mvn clean install
mvn spring-boot:run

The backend service should now be running on http://localhost:8080.

# Database Structure

The database includes tables for storing user information, skills, availability, and appointments. Key relationships link users with their skills and scheduled appointments.

# Tables

**Users:** Stores user information (e.g., ID, name, email).

**Skills:** Lists skills that users can have.

**Availability:** Tracks each user's available times.

**Appointments:** Holds appointment details and links users to scheduled events.

**Reviews:** Stores feedback and ratings for users or services.

# API Endpoints

**User Management**

**Register User:** POST /api/users/register

**Authenticate User:** POST /api/users/login

**Get User Details:** GET /api/users/{id}

# Skill Listings

**Add Skill:** POST /api/skills

**Get All Skills:** GET /api/skills

# Scheduling

**Add Availability:** POST /api/availability

**Book Appointment:** POST /api/appointments

**Get Appointments:** GET /api/appointments/{userId}

# Google Calendar Integration

**Create Event:** POST /api/calendar/event

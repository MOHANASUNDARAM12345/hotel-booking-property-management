# Problem Statement

## 1. Title

StayRest – Hotel Booking and Property Management System

## 2. Domain

Hospitality and Hotel Management

## 3. Who is the user?

### 1. Customer / User
Customers can search for hotels, view available rooms, check room details, make bookings, manage their bookings, and provide reviews.

### 2. Hotel Manager
Hotel managers can manage their hotel properties, rooms, room availability, bookings, and hotel-related information.

### 3. Admin
The administrator manages users, hotels, bookings, and monitors the overall system.

## 4. What problem are we solving?

Many customers find it difficult to search for suitable hotels, compare room details, check availability, and manage bookings through a single platform. Hotel managers also need an organized system to manage rooms, availability, and customer bookings. Manual booking processes can lead to duplicate bookings, incorrect availability information, and difficulty in tracking reservations. StayNest aims to provide a centralized platform that connects customers and hotel managers and simplifies the complete hotel booking process.

## 5. Proposed Solution

StayNest is a full-stack hotel booking and property management system that provides:

- User registration and login
- Role-based access for Customer, Hotel Manager, and Admin
- Hotel and room search
- Room availability checking
- Hotel and room details
- Online room booking
- Booking management
- Booking cancellation
- Hotel and room management for Hotel Managers
- User and hotel management for Admin
- Booking history
- Customer reviews and ratings
- Payment integration scope for future enhancement
- Email notification integration scope for future enhancement

## 6. Core Entities / Database Tables

The main database entities are:

1. Users
2. Hotels
3. Rooms
4. Bookings
5. Payments
6. Reviews

These entities have relationships such as users creating bookings, hotels containing rooms, bookings being associated with rooms and users, and users providing reviews for hotels.

## 7. User Roles & Permissions

### Customer / User
- Register and login
- Search hotels
- View hotel and room details
- Check room availability
- Make bookings
- View booking history
- Cancel bookings
- Submit reviews and ratings

### Hotel Manager
- Login
- Manage hotel information
- Add and update rooms
- Manage room availability
- View customer bookings
- Update booking status
- Manage hotel-related information

### Admin
- Manage users
- Manage hotels
- Manage hotel managers
- View and manage bookings
- Monitor the overall system
- Manage reported or inappropriate content

## 8. Success Criteria

The project will be considered successful when:

- A user can register and login successfully.
- A user can search and view available hotels and rooms.
- A user can check room availability for selected dates.
- A user can complete a room booking successfully.
- The system prevents double booking of the same room for overlapping dates.
- Hotel Managers can manage hotels, rooms, and availability.
- Admin can manage users, hotels, and bookings.
- The complete booking flow works from frontend to backend and database.

## 9. Out of Scope

The following features are outside the initial scope:

- Real-world hotel staff payroll management
- Flight and travel ticket booking
- Restaurant food ordering
- Real-time GPS tracking of hotel guests
- International currency conversion
- Full-scale financial accounting
- Native Android or iOS mobile application

## 10. Chosen Track

Java (Spring Boot)

### Technology Stack

- Frontend: React.js
- Backend: Spring Boot
- Database: MySQL
- Authentication: Spring Security + JWT
- ORM: Spring Data JPA + Hibernate
- Build Tool: Maven
- API Documentation: Swagger / OpenAPI
- Testing: JUnit 5
- Version Control: Git and GitHub
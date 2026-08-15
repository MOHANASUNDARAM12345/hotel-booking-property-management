# StayRest – Requirements

## 1. Project Overview

StayRest is a Hotel Booking and Property Management System designed to help customers search for hotels, view room details, check availability, and make hotel bookings.

The system also provides property management features for hotel owners and administrative features for managing the platform.

---

## 2. User Roles

### 2.1 Customer

The customer can:

- Register an account
- Login to the system
- Search for hotels
- Search hotels by location
- View hotel details
- View available rooms
- Check room availability
- Make hotel bookings
- View booking details
- Manage bookings
- Cancel bookings
- Submit reviews

### 2.2 Hotel Owner

The hotel owner can:

- Register and login
- Add hotel properties
- Update hotel details
- Delete hotel properties
- Add rooms
- Update room details
- Manage room availability
- Manage room pricing
- View customer bookings
- Manage property information

### 2.3 Administrator

The administrator can:

- Login securely
- Manage users
- Manage hotel properties
- Manage rooms
- Manage bookings
- Manage reviews
- Monitor the overall platform

---

## 3. Functional Requirements

### FR-01: User Registration

The system shall allow new customers and hotel owners to create an account.

### FR-02: User Login

The system shall authenticate registered users using their credentials.

### FR-03: Hotel Search

The system shall allow customers to search for hotels by location and hotel name.

### FR-04: Hotel Details

The system shall display hotel information including name, location, description, price, and available rooms.

### FR-05: Room Management

Hotel owners shall be able to add, update, and manage rooms.

### FR-06: Room Availability

The system shall display room availability based on the selected booking dates.

### FR-07: Hotel Booking

Customers shall be able to book available rooms by providing the required booking details.

### FR-08: Booking Management

Customers shall be able to view and manage their bookings.

### FR-09: Booking Cancellation

Customers shall be able to cancel eligible bookings.

### FR-10: Property Management

Hotel owners shall be able to manage their hotel properties and room information.

### FR-11: Review Management

Customers shall be able to submit reviews for hotels after completing a booking.

### FR-12: Administrative Management

Administrators shall be able to manage users, hotels, rooms, bookings, and reviews.

---

## 4. Non-Functional Requirements

### NFR-01: Security

User authentication and authorization shall be implemented securely.

### NFR-02: Performance

The system should provide fast responses for hotel searches and booking operations.

### NFR-03: Availability

The application should be available to users whenever the system is running.

### NFR-04: Usability

The user interface should be simple, responsive, and easy to use.

### NFR-05: Maintainability

The application should use a modular architecture so that features can be maintained and extended easily.

### NFR-06: Scalability

The system should be designed so that additional hotels, rooms, users, and bookings can be supported in the future.

---

## 5. Main Modules

The StayRest system consists of the following modules:

1. User Authentication
2. Hotel Management
3. Room Management
4. Hotel Search
5. Booking Management
6. Property Management
7. Review Management
8. Administration

---

## 6. Technology Requirements

### Frontend

- React
- Vite
- HTML
- CSS
- JavaScript

### Backend

- Java
- Spring Boot
- REST API

### Database

- MySQL

### Development Tools

- Visual Studio Code
- Git
- GitHub
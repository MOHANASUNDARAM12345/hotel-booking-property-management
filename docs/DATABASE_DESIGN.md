# StayRest – Database Design

## 1. Database

Database Name: stayrest

Database Management System: MySQL

---

## 2. Tables

### 2.1 Users

Stores customer, hotel owner, and administrator information.

Fields:

- id
- name
- email
- password
- role

---

### 2.2 Hotels

Stores hotel property information.

Fields:

- id
- name
- location
- description
- image_url
- owner_id

---

### 2.3 Rooms

Stores room information for each hotel.

Fields:

- id
- hotel_id
- room_number
- room_type
- price
- capacity
- availability

---

### 2.4 Bookings

Stores customer hotel room booking information.

Fields:

- id
- user_id
- room_id
- check_in
- check_out
- guests
- status
- total_price

---

### 2.5 Reviews

Stores customer reviews and ratings for hotels.

Fields:

- id
- user_id
- hotel_id
- rating
- comment
- created_at

---

## 3. Relationships

- One user can have many bookings.
- One user can write many reviews.
- One hotel can have many rooms.
- One hotel can have many bookings.
- One hotel can have many reviews.
- One room can have many bookings.
- One hotel owner can manage multiple hotels.

---

## 4. Primary Keys

- users.id
- hotels.id
- rooms.id
- bookings.id
- reviews.id

---

## 5. Foreign Keys

- hotels.owner_id → users.id
- rooms.hotel_id → hotels.id
- bookings.user_id → users.id
- bookings.room_id → rooms.id
- reviews.user_id → users.id
- reviews.hotel_id → hotels.id

## 6. Table Structure

### 6.1 Users

| Column | Data Type | Constraint | Description |
|---|---|---|---|
| id | BIGINT | Primary Key, Auto Increment | User ID |
| name | VARCHAR(100) | NOT NULL | User name |
| email | VARCHAR(150) | UNIQUE, NOT NULL | User email |
| password | VARCHAR(255) | NOT NULL | Encrypted password |
| role | VARCHAR(20) | NOT NULL | USER / OWNER / ADMIN |

### 6.2 Hotels

| Column | Data Type | Constraint | Description |
|---|---|---|---|
| id | BIGINT | Primary Key, Auto Increment | Hotel ID |
| name | VARCHAR(150) | NOT NULL | Hotel name |
| location | VARCHAR(150) | NOT NULL | Hotel location |
| description | TEXT | - | Hotel description |
| image_url | VARCHAR(500) | - | Hotel image |
| owner_id | BIGINT | Foreign Key | Hotel owner |

### 6.3 Rooms

| Column | Data Type | Constraint | Description |
|---|---|---|---|
| id | BIGINT | Primary Key, Auto Increment | Room ID |
| hotel_id | BIGINT | Foreign Key, NOT NULL | Hotel ID |
| room_number | VARCHAR(20) | NOT NULL | Room number |
| room_type | VARCHAR(50) | NOT NULL | Room type |
| price | DECIMAL(10,2) | NOT NULL | Price per night |
| capacity | INT | NOT NULL | Maximum guests |
| availability | BOOLEAN | NOT NULL | Room availability |

### 6.4 Bookings

| Column | Data Type | Constraint | Description |
|---|---|---|---|
| id | BIGINT | Primary Key, Auto Increment | Booking ID |
| user_id | BIGINT | Foreign Key, NOT NULL | Customer ID |
| room_id | BIGINT | Foreign Key, NOT NULL | Room ID |
| check_in | DATE | NOT NULL | Check-in date |
| check_out | DATE | NOT NULL | Check-out date |
| guests | INT | NOT NULL | Number of guests |
| status | VARCHAR(30) | NOT NULL | PENDING / CONFIRMED / CANCELLED |
| total_price | DECIMAL(10,2) | NOT NULL | Total booking price |

### 6.5 Reviews

| Column | Data Type | Constraint | Description |
|---|---|---|---|
| id | BIGINT | Primary Key, Auto Increment | Review ID |
| user_id | BIGINT | Foreign Key, NOT NULL | User ID |
| hotel_id | BIGINT | Foreign Key, NOT NULL | Hotel ID |
| rating | INT | NOT NULL | Rating from 1 to 5 |
| comment | TEXT | - | User review |
| created_at | TIMESTAMP | NOT NULL | Review creation time |
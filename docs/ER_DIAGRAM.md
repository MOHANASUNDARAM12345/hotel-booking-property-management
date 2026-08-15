# StayRest – ER Diagram

## Entities

### USERS
- id (PK)
- name
- email
- password
- role

### HOTELS
- id (PK)
- name
- location
- description
- image_url
- owner_id (FK)

### ROOMS
- id (PK)
- hotel_id (FK)
- room_number
- room_type
- price
- capacity
- availability

### BOOKINGS
- id (PK)
- user_id (FK)
- room_id (FK)
- check_in
- check_out
- guests
- status
- total_price

### REVIEWS
- id (PK)
- user_id (FK)
- hotel_id (FK)
- rating
- comment
- created_at

## Relationships

USERS 1 ──── N BOOKINGS

USERS 1 ──── N REVIEWS

USERS 1 ──── N HOTELS

HOTELS 1 ──── N ROOMS

ROOMS 1 ──── N BOOKINGS

HOTELS 1 ──── N REVIEWS
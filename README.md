# Vehicle Rental Management System – Database Queries

## Project Overview
This project is a **Vehicle Rental Management System** designed to demonstrate proper relational database design and SQL querying skills.

The system manages:
- Users (customers and admins)
- Vehicles
- Bookings

Main focus: **database structure, relationships, and SQL queries**.

---

## Database Schema Summary

### Tables Used
1. **users**
   - Stores customer and admin information
2. **vehicles**
   - Stores rentable vehicle details
3. **bookings**
   - Stores booking records linking users and vehicles

### Relationships
- One user can create multiple bookings
- One vehicle can appear in multiple bookings
- bookings.user_id references users.user_id
- bookings.vehicle_id references vehicles.vehicle_id

All relationships are enforced using **foreign keys**.

---

## Enum Types Used
The following ENUM types are used to ensure data consistency:

- `user_role`: `admin`, `customer`
- `vehicles_type`: `car`, `bike`, `truck`
- `vehicles_status`: `available`, `rented`, `maintenance`
- `booking_status`: `pending`, `confirmed`, `completed`, `cancelled`

---

## Queries Explanation (queries.sql)

All required queries are written inside the `queries.sql` file.  
Below is a brief explanation of the purpose of each category.

### 1. Table Creation Queries
- `CREATE TYPE` is used to define ENUM values.
- `CREATE TABLE` is used to define tables with primary keys and foreign keys.
- `BIGINT` is used for IDs to allow scalability.
- `UNIQUE` constraint is applied on email and vehicle registration number.

### 2. Insert Queries
- Sample data is inserted into:
  - users
  - vehicles
  - bookings
- These records follow assignment requirements and respect foreign key constraints.

### 3. Join Queries
Used to fetch meaningful combined data from multiple tables.

Example:
- Fetch booking details along with customer name and vehicle name using `INNER JOIN`.

### 4. Filtering Queries
- Bookings filtered by status
- Vehicles filtered by availability
- User-specific booking history

### 5. Aggregate Queries
- Total booking cost calculation
- Count of bookings per user or vehicle

---

## ERD (Entity Relationship Diagram)

The ERD visually represents:
- Tables
- Primary keys
- Foreign keys
- One-to-many relationships

**ERD Link:**  
_https://drawsql.app/teams/bytebuilders-4/diagrams/vehicle-rental-system_

---

## Author
**Rubaid Islam**
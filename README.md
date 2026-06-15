# Football Ticket Booking System

A database design project for managing football match ticket bookings.

## Overview

This project implements a complete database solution for a Football Ticket Booking System with three main entities: Users, Matches, and Bookings.

## Database Schema

### Tables

**Users Table**
- Stores user information (fans and ticket managers)
- Fields: user_id (PK), full_name, email, role, phone_number

**Matches Table**
- Contains football match information
- Fields: match_id (PK), fixture, tournament_category, base_ticket_price, match_status

**Bookings Table**
- Records ticket purchases
- Fields: booking_id (PK), user_id (FK), match_id (FK), seat_number, payment_status, total_cost

### Relationships

- One User → Many Bookings (One-to-Many)
- Many Bookings → One Match (Many-to-One)

## Files

- `SCHEMA.sql` - Database schema and sample data
- `QUERY.sql` - SQL queries for data retrieval

## Setup

```bash
# Create database
createdb football_booking

# Run schema
psql -d football_booking -f SCHEMA.sql

# Test queries
psql -d football_booking -f QUERY.sql
```

## Queries

The project includes 7 SQL queries demonstrating:
- Filtering with WHERE clause
- Pattern matching with ILIKE
- NULL handling with COALESCE
- INNER JOIN and LEFT JOIN
- Subqueries with aggregation
- Pagination with LIMIT and OFFSET

## License

MIT License

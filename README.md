# Universe Database Project

This repository contains my completed **PostgreSQL Relational Database** project for the [freeCodeCamp.org Relational Database Certification](https://www.freecodecamp.org/learn/relational-database/).

## Overview

The goal of this project is to create a structured database representing a fictional universe. It includes information about galaxies, stars, planets, and moons, all connected through a relational schema.

The project demonstrates:

- Creation of a PostgreSQL database and multiple relational tables
- Use of data types such as `INT`, `NUMERIC`, `TEXT`, `BOOLEAN`, and `VARCHAR`
- Proper use of `PRIMARY KEY`, `UNIQUE`, and `FOREIGN KEY` constraints
- Normalization and logical relationships between entities
- Adherence to freeCodeCamp’s validation requirements

## Project Requirements

The project satisfies all freeCodeCamp test criteria, including:

- [x] Database named `universe`
- [x] Tables: `galaxy`, `star`, `planet`, `moon`
- [x] Each table contains a `PRIMARY KEY` using the naming convention `table_name_id`
- [x] Columns using `BOOLEAN`, `NUMERIC`, `TEXT`, and `VARCHAR` data types
- [x] Proper use of `FOREIGN KEY` relationships
- [x] At least 5 tables and required row minimums
- [x] Constraints like `NOT NULL` and `UNIQUE` applied appropriately

## Schema Overview

Here’s a brief summary of the core tables and their relationships:

- **Galaxy**
  - `galaxy_id` (PK), `name`, `description`, `age_in_millions_of_years`, `galaxy_type`
- **Star**
  - `star_id` (PK), `name`, `galaxy_id` (FK), `temperature`, `mass`, `is_spherical`, `has_life`
- **Planet**
  - `planet_id` (PK), `name`, `star_id` (FK), `distance_from_star`, `planet_type`, `has_life`, `is_spherical`
- **Moon**
  - `moon_id` (PK), `name`, `planet_id` (FK), `diameter_km`, `is_spherical`, `has_life`
- *(Optional additional tables may be added for normalization)*

## 💾 How to Run

1. Make sure PostgreSQL is installed on your system.
2. Clone this repository:
   ```bash
   git clone https://github.com/YOUR-USERNAME/universe-database.git
   cd universe-database
3. Run the SQL dump file to create the database:
   psql -U postgres < universe.sql
   
4. Connect to the database:
psql -U postgres -d universe


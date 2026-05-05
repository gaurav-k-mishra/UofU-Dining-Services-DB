# University of Utah Dining Services — Database Design

A full-cycle relational database project designed for the University of Utah Dining Services, built as part of IS 6420: Database Theory & Design (Spring 2025, David Eccles School of Business).

**Team:** April Greenwood · Astha K C · Gaurav Mishra · Josie Marshall

---

## Project Overview

University dining is a complex operation — managing meal plans, nutritional needs, inventory, payments, and student feedback across multiple campus locations. This project designs and implements a transactional database to support both consumers (students, staff, faculty) and producers (dining services, suppliers, administration).

### What the database supports

- **Meal plan management** — linking students to their plans, tracking balances, supporting multiple payment types including Dining Dollars
- **Nutritional transparency** — full macro/micronutrient data, allergen tracking, and health scores per menu item
- **Order & inventory tracking** — real-time updates to stock levels as orders are placed
- **Student feedback** — ratings and comments tied to individual students
- **Event management** — campus dining events linked to specific restaurants
- **Delivery logistics** — order tracking from placement to delivery building
- **Employee management** — staff records per dining location

---

## Database Design

| Stage | Description |
|---|---|
| Conceptual model | 15 entities — ERD mapping all major business objects and relationships |
| Logical model | 3rd Normal Form (3NF) — full normalization with PKs, FKs, and unique constraints |
| Physical model | 16 entities implemented in PostgreSQL with typed columns and referential integrity |

### Entities

`student` · `rating` · `allergy` · `payment` · `cuisine` · `menu` · `menu_item` · `item_allergen` · `nutrition` · `restaurant` · `orders` · `order_item` · `meal_plan` · `event` · `seating` · `employee` · `delivery` · `student_nutrition`

---

## Tech Stack

- **Database:** PostgreSQL
- **IDE:** DBeaver
- **Data generation:** ChatGPT
- **Modeling tools:** ERD diagramming (conceptual → logical → physical)

---

## Key Highlights

- Full 3NF normalization — no partial or transitive dependencies
- Allergen tracking at both the student level and the menu item level
- `student_nutrition` entity bridges individual students with their nutritional intake
- `delivery` entity tracks order fulfillment to building-level granularity
- Referential integrity enforced across all foreign key relationships

---

## About

Built by [Gaurav K. Mishra](https://gaurav-k-mishra.github.io) as part of the MS in Business Analytics program at the University of Utah.

[![Portfolio](https://img.shields.io/badge/Portfolio-gaurav--k--mishra.github.io-blue)](https://gaurav-k-mishra.github.io)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?logo=LinkedIn)](https://www.linkedin.com/in/gaurav-mishra1/)

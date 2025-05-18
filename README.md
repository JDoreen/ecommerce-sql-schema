
# 🛒 E-Commerce SQL Schema

This repository contains a PostgreSQL-compatible SQL schema for a simple e-commerce platform.

## 🗂️ Database Tables

The schema includes the following tables:

| Table Name    | Description |
|---------------|-------------|
| `Customers`   | Stores user details such as name, email, phone, and address |
| `Products`    | Product catalog with pricing and inventory information |
| `Orders`      | Tracks customer orders, order date, and status |
| `OrderItems`  | Line items in each order, linking products to orders |
| `Payments`    | Payment information linked to each order |

## 🧱 Schema Overview

- Uses `INT GENERATED ALWAYS AS IDENTITY` for auto-incremented primary keys  
- Uses `TIMESTAMP` for all date-time fields  
- Columns are declared as `NOT NULL` where values are mandatory (e.g. `name`, `price`, `quantity`)  
- `NULL` is allowed for optional fields (e.g. `phone`, `description`)  
- `DEFAULT` values are defined for fields like `created_at`, `status`, and `stock_quantity`  
- `FOREIGN KEY` constraints (`REFERENCES`) are used to enforce relationships between tables  
  - e.g., `Orders.customer_id` references `Customers.customer_id`  
  

## 📋 Usage

1. Clone the repository or download the `.sql` file:
   ```bash
   git clone https://github.com/your-username/ecommerce-sql-schema.git
   cd ecommerce-sql-schema

# TechStore Data Analysis Project

## Overview
This project simulates a tech store database system using MySQL and Python, perfect for learning database management and data analysis concepts. It includes sample data about customers, products, orders, and order items.

## Project Structure
```
techstore Project/
├── fundamentos/           # SQL practice queries
└── techstore_data/       # Data files and scripts
    ├── clientes.csv      # Customer data
    ├── produtos.csv      # Product data
    ├── pedidos.csv       # Order data
    ├── item_pedido.csv   # Order items data
    ├── exploringpandas   # Python script for pandas exploration
    └── exploringsqlalch  # Python script for SQLAlchemy database setup
```

## Dataset Description
The project contains four main datasets:
- **Customers (clientes)**: Customer information including ID, name, registration date, city, and state
- **Products (produtos)**: Product details including ID, name, category, and price
- **Orders (pedidos)**: Order information including order ID, customer ID, order date, and status
- **Order Items (item_pedido)**: Details of items in each order including quantity and unit price

## Technologies Used
- **Python**: Data manipulation and database interaction
- **MySQL**: Database management
- **Pandas**: Data analysis library
- **SQLAlchemy**: SQL toolkit and ORM

## Getting Started

### Prerequisites
- Python 3.x
- MySQL Server
- Required Python packages:
  ```
  pandas
  sqlalchemy
  pymysql
  ```

### Database Setup
1. Install the required Python packages:
````markdown
```bash
pip install pandas sqlalchemy pymysql
```

2. Create a MySQL database named 'techstore'

3. Update the database credentials in the [exploringsqlalch](http://_vscodecontentref_/0) script:
```python
user = 'your_username'
password = 'your_password'
host = 'localhost'
db = 'techstore'
```

### Running the Project
1. Run the SQLAlchemy script to load data:
```bash
python exploringsqlalch
```

## Learning Resources
The [fundamentos](http://_vscodecontentref_/1) folder contains various SQL queries for practice, including:
- Basic SELECT statements
- Filtering with WHERE
- Sorting with ORDER BY
- Aggregations (COUNT, AVG, SUM)
- Joins (INNER JOIN, LEFT JOIN)
- Group operations (GROUP BY)

## Practice Examples
Start with these basic queries:
```sql
-- Count total customers
SELECT COUNT(id_cliente) AS total_clientes FROM clientes;

-- View latest orders
SELECT * FROM pedidos
ORDER BY data_pedido DESC
LIMIT 10;

-- Find average price of accessories
SELECT categoria, AVG(preco) AS preco_medio
FROM produtos
WHERE categoria = 'Acessórios'
GROUP BY categoria;
```

## Security Note
Remember to:
- Never commit database credentials to version control
- Use environment variables for sensitive information
- Always backup your data

## Next Steps
1. Try writing your own SQL queries
2. Experiment with different data analysis techniques
3. Create visualizations using Python libraries
4. Practice database normalization concepts

---

Created as part of a computer science learning journey. Feel free to explore and learn!

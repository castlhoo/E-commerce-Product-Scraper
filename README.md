# 🛍️ E-commerce Product Scraper

This project is a Python script that **scrapes product information** from a specific website and **stores it in a MySQL database**.

## 📖 Project Overview
- Uses `requests` and `BeautifulSoup` to scrape product information from a website.
- Utilizes `pymysql` to **store product names and categories** in a MySQL database.
- **Parses and scrapes data from a public website** (Example URL: `https://davelee-fun.github.io/`).

---

## 📁 Project Structure
```
📂 crawling_SQL_project
├── 📄 crawling_SQL.py        # Crawling and MySQL storage script
└── 📄 README.md              # Project documentation file
```

---

## 🔧 Installation Guide

### 1️⃣ **Install Required Libraries**
Ensure you have Python 3.x installed, then install the necessary packages:
```sh
pip install requests beautifulsoup4 pymysql
```

### 2️⃣ **Set Up MySQL Database**
Log into MySQL and execute the following SQL commands:
```sql
CREATE DATABASE ecommerce;
USE ecommerce;

CREATE TABLE teddyproducts (
    ID INT AUTO_INCREMENT PRIMARY KEY,
    TITLE VARCHAR(255),
    CATEGORY VARCHAR(255)
);
```

### 3️⃣ **Configure MySQL Connection**
Create a `config.py` file and add your MySQL connection details:
```python
DB_CONFIG = {
    'host': 'localhost',
    'port': 3306,
    'user': 'your_username',
    'passwd': 'your_password',
    'db': 'ecommerce',
    'charset': 'utf8'
}
```
---

## 📡 Crawling Target (Public Data)
This script scrapes data from the following **public website**:
- **URL:** [`https://davelee-fun.github.io/`](https://davelee-fun.github.io/)
- Collects product categories and product names, then stores them in MySQL.

---

## 📜 License
This project is distributed under the **MIT License**.

✅ **If you have any questions, feel free to open an issue or discussion!** 😊

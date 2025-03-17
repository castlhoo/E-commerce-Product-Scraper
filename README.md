# 🛍️ E-commerce Product Scraper

이 프로젝트는 특정 웹사이트에서 **상품 정보를 크롤링**하고, 이를 **MySQL 데이터베이스에 저장**하는 Python 스크립트입니다.

## 📖 프로젝트 개요
- `requests`와 `BeautifulSoup`을 사용하여 웹사이트에서 상품 정보 수집
- `pymysql`을 이용해 **MySQL 데이터베이스에 상품명과 카테고리 저장**
- **퍼블릭 웹사이트의 데이터를 파싱하여 크롤링** (예제 URL: `https://davelee-fun.github.io/`)

---

## 📁 프로젝트 구조
```
📂 crawling_SQL_project
├── 📄 crawling_SQL.py        # 크롤링 및 MySQL 저장 스크립트
└── 📄 README.md         # 프로젝트 설명 파일
```

---

## 🔧 설치 방법

### 1️⃣ **필수 라이브러리 설치**
Python 3.x 환경에서 아래 패키지를 설치하세요:
```sh
pip install requests beautifulsoup4 pymysql
```

### 2️⃣ **MySQL 데이터베이스 설정**
MySQL에 접속하여 다음 SQL을 실행하세요:
```sql
CREATE DATABASE ecommerce;
USE ecommerce;

CREATE TABLE teddyproducts (
    ID INT AUTO_INCREMENT PRIMARY KEY,
    TITLE VARCHAR(255),
    CATEGORY VARCHAR(255)
);
```

### 3️⃣ **MySQL 접속 정보 설정**
MySQL 접속 정보를 저장할 `config.py` 파일을 생성하세요:
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

## 📡 크롤링 대상 (퍼블릭 데이터)
이 스크립트는 아래 **퍼블릭 웹사이트**의 데이터를 크롤링합니다:
- **URL:** [`https://davelee-fun.github.io/`](https://davelee-fun.github.io/)
- 상품 카테고리와 상품명을 수집하여 MySQL에 저장

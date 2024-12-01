# Scrapy Books 🕷️📚

A web scraper built using **Scrapy** to extract book details (title, price, and URL) from [Books to Scrape](https://books.toscrape.com/) and store the data in a **MongoDB** database.

---

## Features
- Extracts:
  - Book Title
  - Price
  - URL
- Handles pagination to scrape all pages of the website.
- Stores scraped data in a MongoDB collection for easy access and management.

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Chebil-Ilef/Scrapy-Books
   cd Scrapy-books
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Install and configure MongoDB (ensure it’s running locally or use a remote instance).

---

## Usage

1. **Run the spider**:
   ```bash
   scrapy crawl book
   ```

2. **Configure MongoDB**:
   Update `settings.py` with your MongoDB URI and database name:
   ```python
   MONGO_URI = "mongodb://localhost:27017"
   MONGO_DATABASE = "books_db"
   ```

---

## Project Structure
```
Scrapy-books/
├── books/
│   ├── spiders/
│   │   └── book.py           # Scrapy spider implementation
│   ├── items.py              # Item definitions
│   ├── pipelines.py          # MongoDB pipeline
│   └── settings.py           # Scrapy settings
├── requirements.txt          # Project dependencies
└── README.md                 # Project documentation
```

## Useful Links

https://realpython.com/web-scraping-with-scrapy-and-mongodb/#debug-and-test-your-scrapy-web-scraper


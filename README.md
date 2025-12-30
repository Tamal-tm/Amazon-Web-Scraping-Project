# Amazon-Web-Scraping-Project

Below is **clean, structured project documentation** you can directly submit, upload to GitHub, or include in a resume/project report.
No italics used.

---

## 1. Project Overview

This project is a Python-based web scraping application that extracts laptop product data from Amazon India. The scraper collects structured information such as product title, price, rating, number of reviews, and availability status, cleans the data, and exports it into a CSV file for further analysis or visualization.

The project demonstrates real-world data extraction, cleaning, and storage practices while handling common challenges like dynamic HTML structures, encoding issues, and request blocking.

---

## 2. Objectives

* Scrape laptop product listings from Amazon India
* Extract key product attributes:

  * Product Title
  * Price
  * Rating
  * Number of Reviews
  * Availability
* Clean and normalize the scraped data
* Export the processed data into a CSV file
* Make the dataset compatible with Excel and Power BI

---

## 3. Technologies Used

* Programming Language: Python
* Libraries:

  * requests – for HTTP requests
  * BeautifulSoup (bs4) – for HTML parsing
  * pandas – for data manipulation and storage
  * numpy – for handling missing values
  * urllib.parse – for safe URL handling
  * time – for request throttling
* Data Output Format: CSV
* Target Website: Amazon India (amazon.in)

---

## 4. Project Workflow

1. Send an HTTP request to the Amazon search results page
2. Parse the HTML content using BeautifulSoup
3. Extract product page links
4. Visit each product page individually
5. Scrape required product details
6. Clean and format the extracted data
7. Store the final dataset in a CSV file


## 5. Sample Output

```
Lenovo V14 Laptop | ₹35,990.00 | 4.5 | 56 | In stock
Lenovo V15 Laptop | ₹38,999.00 | 4.3 | 313 | In stock
Acer Aspire Lite | ₹30,990.00 | 3.9 | 2070 | In stock
```

---

## 6. Challenges Faced & Solutions

| Challenge               | Solution                                   |
| ----------------------- | ------------------------------------------ |
| Dynamic HTML structure  | Used CSS selectors instead of fixed IDs    |
| Blocked requests        | Added headers and time delay               |
| Broken currency symbols | Used UTF-8 encoding and string replacement |
| Malformed URLs          | Used urljoin for safe URL handling         |
| Future pandas warnings  | Avoided inplace chained assignments        |

---

## 7. Limitations

* Amazon may block requests if scraping frequency is increased
* Some prices may not appear due to location or login restrictions
* Data accuracy depends on page availability at scrape time


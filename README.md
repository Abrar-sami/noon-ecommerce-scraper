# 📱 Noon Mobile Phones Web Scraper

An automated web scraping pipeline built with **Python**, **Selenium**, and **Pandas** to extract structured mobile phone listings, pricing, discounts, promotional badges, and product galleries across multiple catalog pages on [Noon.com (Egypt)](https://www.noon.com/egypt-ar/).

---

## 📌 Project Overview
This project dynamically scrapes mobile device listings from Noon's catalog, handling dynamic content, lazy loading, and inconsistent promotional tags. The extracted data is exported into clean, structured datasets for analysis.

---

## ✨ Implemented Features & Bonus Requirements
* **Container-Based Extraction:** Isolates each item within its product card container (`_productBoxLink_1ts6x_5`) to maintain data alignment.
* **Missing Value Handling:** Accurately accounts for products without discounts or old prices without disrupting row integrity.
* **Dynamic Promotional Metadata:** Scrapes live inventory notes, stock alerts, and shipping indicators (`_nudgesContainer_1f9au_1`).
* **Bonus — Multi-Image Slider Scraping:** Extracts all gallery images per device separated by commas rather than only the main cover image.
* **Bonus — Automated Pagination:** Navigates across 3 catalog pages dynamically, retrieving 150 unique devices.
* **Structured Data Export:** Exports the resulting dataset directly into spreadsheet-friendly formats.

---

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Scraping Framework:** Selenium WebDriver
* **Driver Management:** `webdriver-manager`
* **Data Processing:** Pandas, OpenPyXL

---

## 📊 Dataset Schema

| Column Name | Description |
| :--- | :--- |
| `Price` | Current listing price |
| `Old_Price` | Original price before discount (if available) |
| `Discount` | Discount percentage tag |
| `Rating_Count` | Number of reviews and ratings |
| `Images` | Full URLs of all device gallery shots |
| `Status_And_Offers` | Device popularity ranking, stock alerts, and shipping badges |

---

## 📁 Repository Structure
```text
├── selenium.ipynb          # End-to-end Selenium scraper notebook
├── noon_mobiles_data.xlsx  # Clean extracted dataset (150 products)
└── README.md               # Project documentation

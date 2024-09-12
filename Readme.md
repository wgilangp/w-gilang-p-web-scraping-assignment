The script scrapes product details (name, price, rating, promo, sales, seller, location, and image link) from Tokopedia.
It simulates scrolling to load all products and iterates through multiple pages.
The scraped data is saved in a DataFrame for further analysis.

# Tokopedia Web Scraping Project

This project scrapes product information from Tokopedia's search results page using Python, Selenium, and BeautifulSoup. The goal is to gather data such as product name, price, rating, promotion, seller, and location for laptops with specific search queries.

## Project Description

This project automates the process of collecting product data from Tokopedia's search results for laptops (e.g., "laptop core i7 gaming"). The script navigates through multiple pages, scrolls to load more products, and extracts relevant information (name, price, rating, promo, sales, seller, location, and image link).

## Technologies

- Python 3.9+
- Selenium
- BeautifulSoup (from bs4)
- Pandas
- Chrome WebDriver

## Output

The output will be saved as a Pandas DataFrame containing the following fields:

- product_name: Name of the product.
- price: Price of the product.
- rating: Rating of the product.
- promo: Promotional details (if available).
- sold: Number of units sold.
- seller: Name of the seller.
- location: Location of the seller.
- link_image: URL of the product image.
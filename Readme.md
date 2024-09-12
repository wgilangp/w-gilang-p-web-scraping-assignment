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

## The Process for building the Python web scraping code for Tokopedia

1. Setting Up Selenium & BeautifulSoup
    - First, we use Selenium to automatically open the Tokopedia web page because the website uses JavaScript to dynamically display content.
    - BeautifulSoup is used to parse the HTML, making it easier to extract important elements from the loaded page.
2. Opening the Target URL
    - The Tokopedia URL with the search query (e.g., laptop gaming core i7) is inserted, and Selenium directs Chrome to open it.
3. Navigation and Scrolling
    - To load all the products on the page, vertical and horizontal scrolling simulations are performed. This is important because Tokopedia uses lazy loading, where products are only loaded as you scroll down the page.
4. Parsing and Data Extraction
    - Using BeautifulSoup, we search for the HTML elements containing essential information such as product name, price, rating, promotions, seller, location, and images.
    - Each product is extracted from specific HTML tags defined by CSS classes, and the data is stored in a dictionary.
5. Page Navigation (Pagination)
    - After collecting data from one page, Selenium clicks the "Next Page" button to move to the next page and repeats the process for a total of 3 pages.
6. Storing Data
    - After data from all pages has been collected, it's stored in a DataFrame using Pandas and then exported to a CSV file for further analysis.
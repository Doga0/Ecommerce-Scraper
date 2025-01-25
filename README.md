# Ecommerce Web Scraper

This repository contains a web scraper designed to extract product information and customer reviews from [Trendyol](https://www.trendyol.com/), a popular e-commerce platform. The scraper is built using Selenium for web automation and BeautifulSoup for HTML parsing. It supports multi-threading to speed up the scraping process and saves the extracted data into a CSV file.

## Requirements

To run this scraper, you need the following Python packages:

-   `selenium`
    
-   `beautifulsoup4`
    
-   `numpy`

You can install these packages using pip:

    pip install selenium beautifulsoup4 numpy

Additionally, you need to have the Chrome WebDriver installed and properly configured. You can download it from [here](https://sites.google.com/chromium.org/driver/).

## Usage

1.  **Clone the Repository**:
``` 
git clone https://github.com/Doga0/Ecommerce-Scraper.git
cd Ecommerce-Scraper
```	
    
2. **Run the Scraper**:

The scraper can be run from the command line with the following arguments:

-   `--url`: The base URL of the Trendyol category or search page to scrape.
    
-   `--start`: The starting page number.
    
-   `--end`: The ending page number.
    
-   `--num_threads`: The number of threads to use for concurrent scraping.
    
-   `--save_path`: The path where the CSV file will be saved.

Example command:

    python trendyol.py --url "https://www.trendyol.com/kadin-giyim-x-g1-c82" --start 1 --end 10 --num_threads 4 --save_path "output.csv"

## Output

The scraper outputs a CSV file with the following columns:

-   `brand`: The brand of the product.
    
-   `product_name`: The name of the product.
    
-   `category`: The category of the product.
    
-   `price`: The price of the product.
    
-   `rating`: The average rating of the product.
    
-   `info`: Additional information or description of the product.
    
-   `comments`: A list of customer reviews for the product.
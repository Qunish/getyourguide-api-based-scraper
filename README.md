# Web Scrapers for GetYourGuide Dubai

This repository contains two Jupyter Notebook web scrapers for extracting data from the website "https://www.getyourguide.com/" related to activities and attractions in Dubai. The data is scraped using Selenium, and the scraped information is stored in a MongoDB database.

## Prerequisites

Before running the web scrapers, make sure you have the following installed:

1. Python 3.x
2. Selenium
3. pandas
4. pymongo
5. Chrome WebDriver

You can install the Python dependencies using the following command:
```
pip install selenium pandas pymongo
```

Make sure to download the appropriate Chrome WebDriver for your operating system and set the `DRIVER_FILE_PATH` variable in both scripts to the correct path.

## LV Spider - Get Activities and Attractions Data

The `getyourguide_lv.ipynb` notebook scrapes data for various categories of activities and attractions in Dubai from the GetYourGuide website. The scraped data includes activity type, name, time, price, rating, and more. The data is organized into a nested dictionary based on different category groups and categories. The final data is stored in a MongoDB database.

To use the LV spider:

1. Ensure that the MongoDB is running on your local machine or replace the `MONGODB_URI`, `DATABASE_NAME`, and `COLLECTION_NAME` variables with your MongoDB connection details.

2. Run the notebook and execute each cell to perform the web scraping and store the data in the MongoDB database.

## PV Spider - Get Product Details

The `getyourguide_pv.ipynb` notebook scrapes detailed information about specific activities and attractions in Dubai from the GetYourGuide website. The script fetches product URLs from a MongoDB database and then extracts data such as activity overview, details, experience, important information, and review summary. The scraped information is updated in the MongoDB database.

To use the PV spider:

1. Ensure that the MongoDB is running on your local machine or replace the `MONGODB_URI` variable with your MongoDB connection URI.

2. Run the notebook and execute each cell to perform the web scraping and update the data in the MongoDB database.

**Note**: Both web scrapers use Selenium for automation, and web scraping may be subject to website terms of service. Always check a website's terms of service and robots.txt file before scraping data. Additionally, use web scraping responsibly and respectfully to avoid IP blocking or other issues.# getyourguide-api-based-scraper

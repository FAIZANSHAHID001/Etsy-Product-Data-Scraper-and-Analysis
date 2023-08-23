# Etsy-Product-Data-Scraper-and-Analysis
Project Description:
This project involves the creation of a web scraper and subsequent data analysis for Etsy products. It aims to extract product information such as titles, ratings, the number of reviews, and prices from Etsy's search results page for the query "caps." The extracted data is then stored in a CSV file for further analysis.

**Project Usefulness**:
This project serves multiple purposes:

**Data Collection:** It allows users to scrape data from Etsy's search results, which can be valuable for market research, competitor analysis, or price tracking.

**Data Cleaning:** The script includes data cleaning steps to ensure the extracted data is consistent and usable for analysis.

**Data Analysis:** The project provides basic data analysis, including statistics and visualizations, to gain insights into the collected data.

**Automation:** The script can be scheduled to run at regular intervals to keep the dataset up to date without manual intervention.

**Customization:** Users can easily modify the code to scrape data for different search queries or from other websites with similar structures.

**Documentation:**

1. **Importing Libraries:**

The project starts by importing necessary libraries, such as BeautifulSoup for web scraping, requests for making HTTP requests, time for introducing delays, datetime for timestamping, csv for data storage, and various data analysis libraries like pandas, numpy, seaborn, and matplotlib.

2. **User-Agent Configuration:**

This section sets up a User-Agent header, mimicking a web browser, to avoid being blocked by the website while scraping. This is a crucial step for ethical web scraping.

3. **CSV File Creation:**

The script creates a CSV file named "etsy_products.csv" to store the scraped data. It defines the CSV's header with columns: Product Title, Rating, Number of Reviews, and Price.

4. **Web Scraping Loop:**

The core of the project is the web scraping loop that iterates through multiple pages of Etsy search results.
It constructs the URL for each page and sends an HTTP request to fetch the page's content.
BeautifulSoup is used to parse the HTML content and extract product information.
The script handles cases where data may be missing by assigning "N/A" to the respective fields.
Extracted data is then written row by row to the CSV file.

5. **Data Analysis:**

After scraping, the project uses pandas to read the CSV file into a DataFrame for analysis.
Descriptive statistics, like count, mean, and more, are calculated for the data.
Data type conversions ensure that 'Rating' and 'Number of Reviews' are treated as strings.
Data quality checks identify and print rows with non-numeric values in 'Rating' and 'Number of Reviews'.

6. **Data Visualization:**

The project employs seaborn and matplotlib to create data visualizations:
A heatmap shows the presence of missing values.
Histograms display the distribution of ratings, number of reviews, and prices.
A scatter plot examines the relationship between the number of reviews and ratings.
A bar chart visualizes the relationship between price and rating.

7. **Project Conclusion:**

The project concludes with a message indicating that the CSV file "etsy_products.csv" has been created on the user's desktop.

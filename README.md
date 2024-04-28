# Web Data Extraction/Scraper
Extracting data from a universities ranking website using Selenium and BeautifulSoup\
This web scraping exercise is intended to extract information from a website and successfully store the information in usable format for further data science endeavors. I have developed a web scraper to extract information from https://www.topuniversities.com/universities.

<img width="411" alt="image" src="https://github.com/dataphoric/Web-Data-Extraction-Scraper/assets/143677328/02feea26-160a-427b-abc6-fdaed1b1fb00">

# Tools
The tools used include:\
1	BeautifulSoup: Beautiful Soup is a Python library for pulling data out of HTML and XML files. It works with parsers to provide ways of navigating, searching, and modifying the parse tree\
2	Selenium: Selenium is a tool for controlling web browsers through programs and performing browser automation. It is most useful for scraping JS-rendered web pages\
3	Requests: The requests library is used for making HTTP requests in Python\
4	Pandas: Python library used for working with data sets, manipulation and analysis. Different python packages/libraries were used including pandas, matplot and Numpy

# Methology
The target website was scraped in two phases

In the first phase, the parent page was requested to extract the name and urls of the listed universities. Being a dynamic website, whose contents change after each load, Selenium was used in addition to the other tools. This is to allow for the handling the web page's JavaScript code, execute XHR requests, and wait for elements to load before scraping the data. The combination of Beautiful Soup and Selenium was used to the job of dynamic scraping. Selenium automates web browser interaction from python. Hence the data rendered by JavaScript links is made available by automating the button clicks with Selenium and then extracted by Beautiful Soup\

In the second phase, using each of the previously extracted urls, the specific university pages were scraped to extract their unique details. The DOM (document object model) of each of the pages was accessed and the useful details extracted.
The generated information was then saved in both JSON and CSV formats.

# Result
The base url was first passed to the Selenium web-driver which worked with chromedriver to open a browser session that gets dynamic contents. This is passed to BeautifulSoup to allow access to the HTML and CSS elements and tags.
<img width="396" alt="image" src="https://github.com/dataphoric/Web-Data-Extraction-Scraper/assets/143677328/c0955cb4-2f20-4c6a-911f-a2f79c102ae1">

<img width="431" alt="image" src="https://github.com/dataphoric/Web-Data-Extraction-Scraper/assets/143677328/688e7111-a976-4d10-9858-24a4c659a62d">

# Outlook
Navigate and scrape all the pages of the base url to extract the information of over 6000 universities listed across 250+ pages on the website. The current approach is time-consuming and times out. Using AJAX analysis to fetch the JSON contents directly could be an alternative.

Another area of focus is the the use of a NoSQL database like MongoDB to store the extracted data.





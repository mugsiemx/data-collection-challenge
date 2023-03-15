# data-collection-challenge

Module 11 DUE 16 Mar 2023

### Background

A full web-scraping and data analysis project utilizing articles from Mars weather and news. This project will identify HTML elements on a page, identify their `id` and `class` attributes, and use this knowledge to extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup. We scrape various types of information, including HTML tables and recurring elements, like multiple news articles on a webpage. With this project, we are strengthening the same core skills that colleagues have been developing until now: collecting data, organizing and storing data, analyzing data, and then visually communicating our insights.

### What we are creating

This new assignment consists of two technical products with the following deliverables:

- Deliverable 1: Scrape titles and preview text from Mars news articles.

- Deliverable 2: Scrape and analyze Mars weather data, which exists in a table.

### Files

Download the following files to get started:

[Module 11 Challenge files](https://static.bc-edx.com/data/dl-1-2/m11/lms/starter/Starter_Code_v1.2.2.zip)

### Instructions

#### Part 1: Scrape Titles and Preview Text from Mars News

Utilizing Jupyter Notebook, use the starter code folder named `part_1_mars_news.ipynb`, working in this code following the steps below to scrape the Mars News website.

1. Use automated browsing to visit the [Mars news site](https://static.bc-edx.com/data/web/mars_news/index.html). Inspect the page to identify which elements to scrape. To identify which elements to scrape, inspected the page by using Chrome DevTools.

2. Create a Beautiful Soup object and use it to extract text elements from the website.

3. Extract the titles and preview text of the news articles that we scraped. Store the scraping results in Python data structures as follows:

   - Store each title-and-preview pair in a Python dictionary and, give each dictionary two keys: `title` and `preview`. An example is the following:

     ```python
     {'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm",
      'preview': "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27."}
     ```

   - Store all the dictionaries in a Python list.

   - Print the list in your notebook.

4. Optionally, store the scraped data in a file (to ease sharing the data with others). To do so, export the scraped data to a JSON file.
   (Note: While there will be no extra points for completing this, it is included in this project.)

#### Part 2: Scrape and Analyze Mars Weather Data

Utilizing Jupyter Notebook, use the starter code folder named `part_2_mars_weather.ipynb`, working in this code following the steps below to scrape and analyze Mars weather data.

1. Use automated browsing to visit the [Mars Temperature Data Site](https://static.bc-edx.com/data/web/mars_facts/temperature.html). Inspect the page to identify which elements to scrape. Note that the URL is `https://static.bc-edx.com/data/web/mars_facts/temperature.html`. Identify which elements to scrape, inspect the page by using Chrome DevTools to discover whether the table contains usable classes.

2. Create a Beautiful Soup object and use it to scrape the data in the HTML table. Although this can also be achieved by using the Pandas `read_html` function, use Beautiful Soup here to continue sharpening our web scraping skills.

3. Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. An explanation of the column headings as follows:

   - `id`: the identification number of a single transmission from the Curiosity rover
   - `terrestrial_date`: the date on Earth
   - `sol`: the number of elapsed sols (Martian days) since Curiosity landed on Mars
   - `ls`: the solar longitude
   - `month`: the Martian month
   - `min_temp`: the minimum temperature, in Celsius, of a single Martian day (sol)
   - `pressure`: The atmospheric pressure at Curiosity's location

4. Examine the data types that are currently associated with each column. Cast (or convert) the data to the appropriate `datetime`, `int`, or `float` data types, using the Pandas `astype` and `to_datetime` methods to accomplish this task.

5. Analyze the dataset by using Pandas functions to answer the following questions:

   - How many months exist on Mars?
   - How many Martian (and not Earth) days worth of data exist in the scraped dataset?
   - What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
     - Find the average minimum daily temperature for all of the months.
     - Plot the results as a bar chart.
   - Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
     - Find the average daily atmospheric pressure of all the months.
     - Plot the results as a bar chart.
   - About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
     - Consider how many days elapse on Earth in the time that Mars circles the Sun once.
     - Visually estimate the result by plotting the daily minimum temperature.

6. Export the DataFrame to a CSV file.

### References

[The Mars News website](https://static.bc-edx.com/data/web/mars_news/index.html) is operated by edX Boot Camps LLC for educational purposes only. The news article titles, summaries, dates, and images were scraped from [NASA's Mars News](https://mars.nasa.gov/) website in November 2022. Images are used according to the [JPL Image Use Policy](https://www.jpl.nasa.gov/jpl-image-use-policy), courtesy NASA/JPL-Caltech.

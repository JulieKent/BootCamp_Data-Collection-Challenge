# BootCamp_Data-Collection-Challenge


## Part 1: Scrape Titles and Preview Text from Mars News

1. Use automated browsing to visit the ![Mars news site](https://static.bc-edx.com/data/web/mars_news/index.html). Inspect the page to identify which elements to scrape.

2. Create a Beautiful Soup object and use it to extract text elements from the website.

3. Extract the titles and preview text of the news articles that you scraped. Store the scraping results in Python data structures as follows:
   * Store each title-and-preview pair in a Python dictionary and, give each dictionary two keys: title and preview. An example is the following:
   ```
   {'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm", 
   'preview': "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27."}
   ```
   * Store all the dictionaries in a Python list.
   * Print the list in your notebook.

   ![Python List](Images/print_news_list.png)

4. Optionally, store the scraped data in a file (to ease sharing the data with others). To do so, export the scraped data to a JSON file.


## Part 2: Scrape and Analyse Mars Weather Data

1. Use automated browsing to visit the ![Mars Temperature Data Site](https://static.bc-edx.com/data/web/mars_facts/temperature.html). Inspect the page to identify which elements to scrape.

2. Create a Beautiful Soup object and use it to scrape the data in the HTML table.

3. Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:
   * id: the identification number of a single transmission from the Curiosity rover
   * terrestrial_date: the date on Earth
   * sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
   * ls: the solar longitude
   * month: the Martian month
   * min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
   * pressure: The atmospheric pressure at Curiosity's location

   ![Pandas Dataframe](Images/pandas_dataframe.png)

4. Examine the data types that are currently associated with each column. If necessary, cast (or convert) the data to the appropriate datetime, int, or float data types.

![Initial DTypes](Images/initial_dtypes.png)   ![Changed DTypes](Images/changed_dtypes.png)

5. Analyse your dataset by using Pandas functions to answer the following questions:
   * How many months exist on Mars?
   ![Months](Images/months.png)

   * How many Martian (and not Earth) days worth of data exist in the scraped dataset?
   ![Days](Images/days.png)

   * What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
      * Find the average minimum daily temperature for all of the months.
      ![Minimum Average Daily Temp](Images/min_avg_temp.png)
      * Plot the results as a bar chart.
      ![Plot Average Minimum Temp](Images/plot_min_temp.png)
      ![Coldest to Warmest](Images/coldest_to_warmest.png)

   * Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
      * Find the average daily atmospheric pressure of all the months.
      ![Average Atmospheric Pressures](Images/pressure.png)
      * Plot the results as a bar chart.
      ![Pressures Lowest to Highest](Images/pressure_low_to_high.png)

   * About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
      * Consider how many days elapse on Earth in the time that Mars circles the Sun once.
      * Visually estimate the result by plotting the daily minimum temperature.
      ![Minimum Temp by Day](Images/min_temp_by_day.png)

6. Export the DataFrame to a CSV file.

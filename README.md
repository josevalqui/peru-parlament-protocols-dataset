# peru-parlament-protocols-dataset
A collection of the protocols of the Peruvian Parliament from the 26.07.1997 to the 11.10.2023.

Methods
The data was scraped from the official website of the parliament (https://www.congreso.gob.pe/actaspleno/) on the 01.11.2023 using BeautifulSoup in Python.

The csv file "raw_data" contains a table with x entries with the session name (when applicable), the session date and the session protocol text. 
There were x sessions for which only a lower quality image PDF was provided (from the x to the x), which couldn't be extracted with the usual Python libraries. These sessions were thus excluded from the dataset.
There are a few other csv files aiming to make it easier to work with the data, since the raw texts were not standardized:
  1. The csv named "attendance.csv" contains the list of all sessions and the attendance of all congresspeople.
     This information was extracted using regular expressions, and cthen manually checked for errors caused by mistakes in the original text.
     Based on 130 congresspeople being active at once, the average error rate of this table can be calculated (130 - number of people mentioned per session in the table): x
  2. The csv file "sentiment_analysis.csv" contains the sentiment analysis on a set of topics, clustered by month.

To contribute to the dataset, 

# portfolio projects!!
**1. Project: Simple Amazon Price Scraper with CSV Logging**\
**2. Chicago Transit Authority (CTA) Ridership Trends Dashboard project**



## Project: Simple Amazon Price Scraper with CSV Logging
### Objective:
Automate the process of extracting the price and title of an Amazon product and store the data in a CSV file. The script runs continuously at regular intervals (once every 24 hours) to track price changes over time.

### Steps Involved:
**1. Connect to the Website:**

Use the requests library to send a GET request to the Amazon product page.\
Use custom headers to mimic a browser visit and avoid being blocked.\

**2. Parse HTML Data:**

Use BeautifulSoup to parse and prettify the HTML content.\
Extract the product title and price using the appropriate HTML tags and IDs.\

**3. Clean and Validate Data:**

Remove unnecessary whitespace from the title and price.\
Remove the dollar sign ($) from the price to keep it clean.\

**4. Write Data to CSV:**

Create or append data to a CSV file named AmazonWebScraperDataset.csv.\
Add a header (Title, Price, Date) if the file is new.\
Append new data with each run to log price changes.\



## Outputs:
- Writes product title, price, and the current date to AmazonWebScraperDataset.csv.\
- Logs errors or missing data if extraction fails.\
- Continuous Monitoring:\



## Chicago Transit Authority (CTA) Ridership Trends Dashboard project
### Dataset:

*data1*-dataset with ridership data for various CTA stations, including station names, monthly ridership data (average weekday, Saturday, Sunday/holiday), and the total ridership for the month. 

*data2*-contains information about specific CTA stops, including:

STOP_ID: Unique identifier for the stop\
DIRECTION_ID: Direction of the train\
STOP_NAME: Name of the stop\
STATION_NAME: Name of the station\
STATION_DESCRIPTIVE_NAME: Full descriptive name of the station\
MAP_ID: Identifier for the map\
ADA: ADA accessibility (TRUE/FALSE)\
RED, BLUE, G, BRN, P, Pexp, Y, Pnk, O: Indicator columns for which lines pass through the station (True for presence, False for absence)\
Location: Coordinates (latitude, longitude)\

## What can be explored with this dataset?
**1. Accessibility Analysis**
Objective: Analyze ADA accessibility across different stations and stops.
Description: Using the "ADA" column, create a map or dashboard to visualize which stations are ADA-compliant and which are not. You can perform a spatial analysis to identify areas with high or low accessibility, and create recommendations for improving accessibility at stations that lack ADA features.

*Tools: Python (GeoPandas, Folium), Power BI, Tableau, ArcGIS.*

**2. Transit Line Usage Visualization**
Objective: Visualize the usage of different train lines (e.g., Red, Blue, Green, etc.) at various stations.
Description: Analyze how many lines each station serves and create a visualization of how heavily trafficked different lines are based on the number of stations serving those lines. You could also calculate and visualize the average number of stations per line.

*Tools: Python (Pandas, Matplotlib/Seaborn), Power BI, Tableau.*

**3. Station Location Analysis**
Objective: Explore the geographic distribution of stations and their proximity to key areas.
Description: Use the latitude and longitude information to create a heatmap or map showing the density of stations in different neighborhoods of Chicago. You could also analyze the proximity of stations to landmarks, universities, or commercial districts.

*Tools: Python (Folium, GeoPandas), Tableau, QGIS.*

**4. Route Optimization and Accessibility**
Objective: Develop a model for optimizing routes for people with mobility challenges.
Description: Build a model that recommends the fastest or most accessible routes for people with disabilities, considering ADA-compliant stations. You could also recommend improvements for non-ADA stations based on the results.

*Tools: Python (NetworkX for route optimization), GIS tools.*

**5. Visualizing Stations by Line and Direction**
Objective: Create an interactive map or dashboard showing stations grouped by line and direction.
Description: Build a visual representation of stations by line (e.g., all Blue Line stations or all Pink Line stations) and further categorize by direction (e.g., inbound or outbound). The map could display which direction each station serves.

*Tools: Power BI, Tableau, Python (Dash, Plotly).*

**6. Transit Time Prediction (Extended with Ridership Data)**
Objective: Predict transit times between stations based on their locations and the number of stations served.
Description: Combine this dataset with your existing ridership data to predict expected travel times between stations based on traffic, distance, and accessibility. This could be a part of a larger system that helps riders plan their journeys more efficiently.

*Tools: Python (scikit-learn for prediction models), Power BI, Tableau.*

**7. Station Popularity Analysis**
Objective: Analyze and predict the popularity of stations.
Description: Using the station names and lines, create a model or visualization to predict the popularity of different stations based on ridership trends, accessibility, or other factors like proximity to important locations.

*Tools: Python (scikit-learn, Pandas), Power BI.*

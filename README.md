# Weather and City Analysis with Python APIs

## How to Use 
In the file named WeatherPy there are two Jupyter Notebook files: WeatherPy and VacationPy. WeatherPy contains code to visualize the weather of over 500 cities of varying distances from the equator. I created a series of linear regressions to demonstrate how different aspects of weather change as one moves closer to the equator. All charts of the linear regression are contained in the output_data folder. VacationPy contains code to narrow down a list of cities based on types of weather. To begin, I created a map of cities in the csv based on humidity. Each point on the map contains a hover message containing information about each city, and the size of the city marker is dependent on the average humidity. For the second map, I chose to narrow my cities down to places that are around 70 degrees F, with 50% cloud cover, and wind speeds less than 3 mph. Then I used GeoApify API to generate a list of hotels in the cities that met my criteria. I then updated the hover messages for each city to include the name of the hotel found in the previous step. 


## Background
Data's true power is its ability to definitively answer questions. So, let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What is the weather like as we approach the equator?"

Now, we know what you may be thinking: “That’s obvious. It gets hotter.” But, if pressed for more information, how would you prove that?

## Before You Begin
1. Create a new repository for this project called python-api-challenge. Do not add this homework to an existing repository.

2. Clone the new repository to your computer.

3. Inside your local Git repository, create a directory for this assignment. Use a folder name that corresponds to the Challenges, such as WeatherPy.

4. Inside the folder you just created, add the files called api_keys.py, WeatherPy.ipynb, and VacationPy.ipynb that you will find in the starter code ZIP file provided. These will be the main scripts to run for each analysis.

5. Before you push your changes to GitHub, add a .gitignore file.

## Add a .gitignore File
For this assignment, you will need to add a .gitignore file to your repo. Doing so will prevent the api_keys.py file that contains your API key from being shared with the public. If you skip this step, anyone using GitHub could copy and use your API key, and you may incur charges as a result.

To get started, type git status in the command line to see a list of all the untracked files that you have created so far.

To add only the WeatherPy.ipynb file to GitHub, for example, type git add WeatherPy.ipynb. Keep in mind that you would have to add each file individually when adding or updating a file. A more efficient solution is to add all of the files that you don't want to track to the .gitignore file.

# Instructions
This activity is broken down into two deliverables, WeatherPy and VacationPy.

## Part 1: WeatherPy
In this deliverable, you'll create a Python script to visualize the weather of over 500 cities of varying distances from the equator. You'll use the citipy Python libraryLinks to an external site., the OpenWeatherMap APILinks to an external site., and your problem-solving skills to create a representative model of weather across cities.

For this part, you'll use the WeatherPy.ipynb Jupyter notebook provided in the starter code ZIP file. The starter code will guide you through the process of using your Python coding skills to develop a solution to address the required functionalities.

To get started, the code required to generate random geographic coordinates and the nearest city to each latitude and longitude combination is provided.

## Requirement 1: Create Plots to Showcase the Relationship Between Weather Variables and Latitude
To fulfill the first requirement, you'll use the OpenWeatherMap API to retrieve weather data from the cities list generated in the starter code. Next, you'll create a series of scatter plots to showcase the following relationships:

  - Latitude vs. Temperature
  - Latitude vs. Humidity
  - Latitude vs. Cloudiness
  - Latitude vs. Wind Speed
 
![image](https://github.com/taschaef/Weather_And_City_Analysis_With_Python_APIs/assets/124079708/85e204fa-4f98-4d0f-8332-e15b9cd32759)

![image](https://github.com/taschaef/Weather_And_City_Analysis_With_Python_APIs/assets/124079708/d8ce052a-35eb-44cc-b917-52708594863f)

![image](https://github.com/taschaef/Weather_And_City_Analysis_With_Python_APIs/assets/124079708/8847bd5e-70f4-4d5d-a056-b462e455890a)

![image](https://github.com/taschaef/Weather_And_City_Analysis_With_Python_APIs/assets/124079708/faced631-bfb8-4ba8-96dc-f1f4d0d0fefb)


## Requirement 2: Compute Linear Regression for Each Relationship
To fulfill the second requirement, compute the linear regression for each relationship. Separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude). You may find it helpful to define a function in order to create the linear regression plots.

Next, create a series of scatter plots. Be sure to include the linear regression line, the model's formula, and the r values. 

You should create the following plots:
  - Northern Hemisphere: Temperature vs. Latitude
  - Southern Hemisphere: Temperature vs. Latitude
  - Northern Hemisphere: Humidity vs. Latitude
  - Southern Hemisphere: Humidity vs. Latitude
  - Northern Hemisphere: Cloudiness vs. Latitude
  - Southern Hemisphere: Cloudiness vs. Latitude
  - Northern Hemisphere: Wind Speed vs. Latitude
  - Southern Hemisphere: Wind Speed vs. Latitude

After each pair of plots, explain what the linear regression is modeling. Describe any relationships that you notice and any other findings you may uncover.

## Part 2: VacationPy
In this deliverable, you'll use your weather data skills to plan future vacations. Also, you'll use Jupyter notebooks, the geoViews Python library, and the Geoapify API.

The code needed to import the required libraries and load the CSV file with the weather and coordinates data for each city created in Part 1 is provided to help you get started.

Your main tasks will be to use the Geoapify API and the geoViews Python library and employ your Python skills to create map visualizations.

To succeed on this deliverable of the assignment, open the VacationPy.ipynb starter code and complete the following steps:
1. Create a map that displays a point for every city in the city_data_df DataFrame as shown in the following image. The size of the point should be the humidity in each city.
2. Narrow down the city_data_df DataFrame to find your ideal weather condition. For example:
  - A max temperature lower than 27 degrees but higher than 21
  - Wind speed less than 4.5 m/s
  - Zero cloudiness
    
3. Create a new DataFrame called hotel_df to store the city, country, coordinates, and humidity.

4. For each city, use the Geoapify API to find the first hotel located within 10,000 meters of your coordinates.

5. Add the hotel name and the country as additional information in the hover message for each city on the map. 





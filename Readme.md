# Covid Tracker

The code you provided is a Python program that creates a simple graphical user interface (GUI) using the tkinter library for tracking COVID-19 data. Here's a step-by-step explanation of what's happening in the code:

Importing Libraries: The code starts by importing three libraries: requests, bs4 (Beautiful Soup 4), and tkinter. These libraries are used for web scraping, parsing HTML data, and creating the GUI.

get_html_data Function: This function is defined to make an HTTP GET request to a given URL using the requests library and returns the response data.

get_covid_data Function: This function is used to fetch COVID-19 data from the website "https://www.worldometers.info/coronavirus/". It calls the get_html_data function to retrieve the HTML content of the webpage.
It uses Beautiful Soup (bs4) to parse the HTML data and extract specific information about COVID-19 cases (total cases, deaths, and recoveries). The extracted data is then formatted and returned as a string.

get_country_data Function: This function is intended to retrieve COVID-19 data for a specific country. It takes the name of the country from a text input field (textfield), constructs the URL for the specific country, and fetches the HTML data.
Similar to get_covid_data, it parses the HTML data to extract COVID-19 information for the specified country. The extracted data is displayed in the mainlabel widget.

reload Function: This function is called when the "Reload" button (rbtn) is clicked. It calls the get_covid_data function to retrieve the latest global COVID-19 data and updates the information displayed in the mainlabel widget.

Creating the GUI: A tkinter window (root) is created with a size of 900x700 pixels and a title "Covid Tracker." A text input field (textfield) is added to enter the name of the country for which you want to fetch COVID-19 data.
A label (mainlabel) is added to display the COVID-19 data. Initially, it shows global COVID-19 data obtained from get_covid_data. Two buttons, "Reload" (rbtn) and "Get Data" (gbtn), are added to trigger the functions for reloading global data and fetching country-specific data, respectively.

Running the GUI: The root window is started using root.mainloop(), which displays the GUI to the user. 

When you run this program, you can enter a country name in the text input field and click the "Get Data" button to fetch and display COVID-19 data for that specific country. The "Reload" button allows you to refresh and retrieve the latest global COVID-19 data.

# weatherMonitor
short: warns about changes in temperature in cities around the world according to configuration threshold and frequency


This application monitors and displays weather in cities of choice around the world
taking data from the openweathermap.org API according to the configuration file.
For obtaining data successfully the configuration file must include an array of 1 city property or more for example:
[
    {
      "city_id":2643743,
      "city_name":"London",
      "frequency":10,
      "threshold":1
    }
]

Additionally, the API requests an APPID which is hard-coded and prevents obtaining the data if expires or not valid.

The openweathermap API recommendeds using city_id so the application uses the city_name property only for display.

The configuration file is located in: src\main\resources\application.properties
To start monitoring open the project from the pom.xml file and run the function public static void main(String[] args) with no arguments.

Dependencies:
Java 8
json-simple-1.1.jar
Maven

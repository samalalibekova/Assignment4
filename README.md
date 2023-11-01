# Weather Data 

This Java program allows you to fetch weather data from the OpenWeatherMap API for a specified location and map the retrieved data into a common data model. The common data model includes temperature, humidity, weather condition, location, and wind speed.

## Prerequisites

Before using this program, you need to have the following:

1. **OpenWeatherMap API Key**: You'll need to sign up on the OpenWeatherMap website and obtain an API key. Replace the placeholder for the `apiKey` in the code with your own key.

2. **Java Development Environment**: Ensure you have Java and a suitable development environment (e.g., Eclipse, IntelliJ IDEA, or a text editor) installed on your system.

## How to Use

Follow these steps to use the program:

1. Clone or download this repository to your local machine.

2. Open the Java source code file `Adapter_Weather.java`.

3. Replace the placeholder for the `apiKey` with your OpenWeatherMap API key in the code.

4. Compile and run the `Adapter_Weather` class:

5. The program will fetch weather data for a specified location (in this example, "Aral") from the OpenWeatherMap API.

6. If the API call is successful, it will print out the common weather data, including location, temperature, condition, humidity, and wind speed.

## Dependencies

This program uses the following Java libraries:

- `org.json.JSONObject` for working with JSON data.

Make sure you have these dependencies available in your Java project.

## Methods

 `fetchWeatherData` method:
   - This method is responsible for fetching weather data using the OpenWeatherMap API.
   - It takes two parameters: `apiName` (the API to use, in this case, "OpenWeatherMap") and `location` (the location for which you want to fetch weather data).
   - It constructs the API URL with the provided location and API key.
   - It makes an HTTP GET request to the API and checks the response code.
   - If the response code is 200 (OK), it reads the response data, converts it to a JSON object, and then calls the `mapToCommonModel` method to map the data to a common data model.
   - It returns the common data model as a `JSONObject`.

 `mapToCommonModel` method:
   - This private method takes the JSON data from the OpenWeatherMap API and maps it to a common data model.
   - It extracts temperature (in Celsius), humidity, wind speed, weather condition, and location from the OpenWeatherMap JSON response.
   - It converts the temperature from Kelvin to Celsius and stores all the values in a new `JSONObject`.
   - The common data model includes temperature, humidity, condition, location, and wind speed.

`main` method:
   - The `main` method serves as the entry point for the program.
   - It creates an instance of the `Adapter_Weather` class and calls the `fetchWeatherData` method to retrieve weather data for the specified location ("Aral").
   - If weather data is successfully retrieved, it prints out the common weather data, including location, temperature, condition, humidity, and wind speed.



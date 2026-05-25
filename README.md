# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools
# Name: CHARITHRAKSHI K
# Register no: 212224040053
# Aim:
Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools

# AI Tools Required:
### chatGPT

# Explanation:
Experiment the persona pattern as a programmer for any specific applications related with your interesting area. 
Generate the outoput using more than one AI tool and based on the code generation analyse and discussing that. 
# Stage 1: Prompt for Generating Python Code for Multiple APIs
Prompt Designed

“Generate Python code that fetches weather information from two different APIs such as OpenWeatherMap API and WeatherAPI.
The program should:

Accept a city name as input.
Retrieve temperature, humidity, and weather condition from both APIs.
Display the outputs clearly.
Use Python requests library.
Include proper exception handling and comments.
# AI-Generated Response:
```
import requests

# API Keys
OPENWEATHER_API_KEY = "your_openweather_api_key"
WEATHERAPI_KEY = "your_weatherapi_key"

city = input("Enter city name: ")

try:
    # OpenWeatherMap API
    openweather_url = f"https://api.openweathermap.org/data/2.5/weather?q={city}&appid={OPENWEATHER_API_KEY}&units=metric"
    response1 = requests.get(openweather_url)
    data1 = response1.json()

    # WeatherAPI
    weatherapi_url = f"http://api.weatherapi.com/v1/current.json?key={WEATHERAPI_KEY}&q={city}"
    response2 = requests.get(weatherapi_url)
    data2 = response2.json()

    print("\n--- OpenWeatherMap ---")
    print("Temperature:", data1['main']['temp'], "°C")
    print("Humidity:", data1['main']['humidity'], "%")
    print("Condition:", data1['weather'][0]['description'])

    print("\n--- WeatherAPI ---")
    print("Temperature:", data2['current']['temp_c'], "°C")
    print("Humidity:", data2['current']['humidity'], "%")
    print("Condition:", data2['current']['condition']['text'])

except Exception as e:
    print("Error occurred:", e)
```
## Explanation
The code uses two APIs to fetch weather data.
requests library is used for API calls.
User provides a city name as input.
Results from both APIs are displayed separately.
Exception handling prevents crashes if errors occur.

# Stage 2: Prompt for Comparing Outputs from Different APIs
Prompt Designed

“Write Python code that compares the outputs received from OpenWeatherMap API and WeatherAPI.
The program should:

Compare temperature and humidity values.
Calculate the difference between values.
Display which API reports higher temperature and humidity.
Print the comparison in a readable format.”
# AI-Generated Response:
```
# Sample values from APIs

open_temp = 30
weather_temp = 28

open_humidity = 70
weather_humidity = 65

temp_difference = abs(open_temp - weather_temp)
humidity_difference = abs(open_humidity - weather_humidity)

print("Temperature Difference:", temp_difference, "°C")
print("Humidity Difference:", humidity_difference, "%")

if open_temp > weather_temp:
    print("OpenWeatherMap reports higher temperature.")
else:
    print("WeatherAPI reports higher temperature.")

if open_humidity > weather_humidity:
    print("OpenWeatherMap reports higher humidity.")
else:
    print("WeatherAPI reports higher humidity.")
```

## Explanation
The program compares values from both APIs.
abs() function calculates the difference.
Conditional statements identify higher values.
Results are shown in an easy-to-read format.

# Stage 3: Prompt for Generating Insights and Suggestions
Prompt Designed

“Generate Python code that analyzes weather data collected from multiple APIs and provides useful insights.
The program should:

Identify if the weather is hot, cold, or moderate.
Suggest whether users should carry an umbrella based on weather conditions.
Recommend precautions if humidity is high.
Display meaningful conclusions.”
# AI-Generated Response:
```
temperature = 32
humidity = 85
condition = "Rain"

print("\nWeather Insights")

if temperature > 30:
    print("The weather is hot.")
elif temperature < 20:
    print("The weather is cold.")
else:
    print("The weather is moderate.")

if "rain" in condition.lower():
    print("Carry an umbrella.")
else:
    print("No umbrella needed.")

if humidity > 80:
    print("High humidity detected. Stay hydrated.")
```
## Explanation:
The program analyzes weather conditions.
Decision-making is done using if-elif-else.
Suggestions help users take precautions.
The output becomes more meaningful and actionable.
Reflection Note
# Effectiveness of the Prompts

The prompts were effective because they clearly specified:

The task to be performed.
The technologies to be used.
The expected output format.
Additional requirements such as exception handling and comparisons.

This helped the AI generate structured and accurate Python code with explanations.

# Improvements for Future Prompts

The prompts can be improved further by:

Mentioning exact API response formats.
Asking for modular code using functions.
Requesting advanced features like data visualization and logging.
Including requirements for better UI or database storage.

# Result: 
The corresponding Prompt is executed successfully.

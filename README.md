# Weather_data_notifier_system


Overview
This project is a simple client-server application that retrieves weather data for a specified city using the OpenWeatherMap API. The server fetches weather data from the API and sends it to the client over a TCP socket connection. The client allows users to input a city name and displays the weather information.

Features
Client: Prompts the user to enter a city name and displays the temperature, weather description, and humidity.
Server: Listens for client connections, fetches weather data from OpenWeatherMap, and sends it back to the client.
Uses TCP sockets for communication and JSON for data serialization.

Prerequisites
Python 3.6 or higher
An active OpenWeatherMap API key (sign up at OpenWeatherMap to get one)
Internet connection for API requests

Installation
Clone the repository:git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name


Install the required Python packages:pip install -r requirements.txt
Replace 'Your API KEY' in server.py with your OpenWeatherMap API key.

Usage
Start the server:python server.py
The server will start listening on 127.0.0.1:65433.
In a separate terminal, run the client:python client.py
Enter a city name when prompted (e.g., London), or type quit to exit.
The client will display the weather data (temperature, description, and humidity) for the specified city.

Project Structure
client.py: The client script that connects to the server and requests weather data.
server.py: The server script that fetches weather data from OpenWeatherMap and responds to client requests.
requirements.txt: Lists the Python dependencies for the project.

Example Output
Server:
Server listening on 127.0.0.1:65433
Connected by ('127.0.0.1', 54321)

Client:
Enter city name (or 'quit' to exit): London
Weather in London:
Temperature: 15.2°C
Description: clear sky
Humidity: 72%
Enter city name (or 'quit' to exit): quit

Notes
Ensure the server is running before starting the client.
The server uses the OpenWeatherMap API, so a valid API key is required.
Error handling is implemented to manage invalid city names or API failures.


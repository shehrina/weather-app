# WeatherWorks!

A simple, consise web application that displays current weather information for cities around the world using the OpenWeatherMap API.

## Features

- Clean, minimalist user interface
- Search for weather by city name
- Displays current temperature and weather conditions
- Shows "feels like" temperature
- Graceful handling of invalid city names
- Default city set to Toronto
- Responsive design that works on both desktop and mobile

## Technical Stack

- **Backend**: Python/Flask
- **Server**: Waitress WSGI server
- **Frontend**: HTML with Jinja2 templating
- **Styling**: Custom CSS
- **Weather Data**: OpenWeatherMap API
- **Environment Variables**: python-dotenv

## Prerequisites

- Python 3.x
- OpenWeatherMap API key

## Installation

1. Clone the repository:
   ```bash
   git clone [ https://github.com/shehrina/weather-app.git]
   ```

2. Install required packages:
   ```bash
   pip install flask requests python-dotenv waitress
   ```

3. Create a `.env` file in the root directory with your OpenWeatherMap API key:
   ```
   API_KEY=your_api_key_here
   ```

## Usage

1. Start the server:
   ```bash
   python server.py
   ```

2. Open your browser and navigate to `http://localhost:8000`
3. Enter a city name in the search box
4. View the current weather conditions

## Design

The application features a user-friendly interface with:
- Soft pink background (#ffe4e1)
- Large, readable Verdana/Arial fonts
- Centered layout with consistent spacing
- Rounded input fields and buttons
- Mobile-responsive design

## Error Handling

- Provides a friendly error page for invalid city names
- Allows immediate re-search from the error page
- Defaults to Toronto if no city is specified

## Project Structure

```
├── server.py           # Main Flask application
├── weather.py         # Weather API integration
├── .env              # API key configuration
├── static/
│   └── styles/
│       └── style.css # Application styling
└── templates/
    ├── index.html           # Landing page
    ├── weather.html         # Weather display
    └── city-not-found.html  # Error page
```

## Development

To run the weather module independently for testing:
```bash
python weather.py
```

## API Reference

The application uses the OpenWeatherMap API with the following endpoint:
```
GET http://api.openweathermap.org/data/2.5/weather
```

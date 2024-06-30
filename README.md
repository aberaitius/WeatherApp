
░██╗░░░░░░░██╗███████╗░█████╗░████████╗██╗░░██╗███████╗██████╗░  ░█████╗░██████╗░██████╗░
░██║░░██╗░░██║██╔════╝██╔══██╗╚══██╔══╝██║░░██║██╔════╝██╔══██╗  ██╔══██╗██╔══██╗██╔══██╗
░╚██╗████╗██╔╝█████╗░░███████║░░░██║░░░███████║█████╗░░██████╔╝  ███████║██████╔╝██████╔╝
░░████╔═████║░██╔══╝░░██╔══██║░░░██║░░░██╔══██║██╔══╝░░██╔══██╗  ██╔══██║██╔═══╝░██╔═══╝░
░░╚██╔╝░╚██╔╝░███████╗██║░░██║░░░██║░░░██║░░██║███████╗██║░░██║  ██║░░██║██║░░░░░██║░░░░░
░░░╚═╝░░░╚═╝░░╚══════╝╚═╝░░╚═╝░░░╚═╝░░░╚═╝░░╚═╝╚══════╝╚═╝░░╚═╝  ╚═╝░░╚═╝╚═╝░░░░░╚═╝░░░░░


# Weather Application

A simple weather application built with Angular and .NET that fetches weather data from the OpenWeatherMap API and displays it with a user-friendly interface.

## Features

- Fetch current weather data for any location
- Display weather information including temperature, humidity, wind speed, and pressure
- Show weather icons corresponding to current conditions
- Loading spinner while fetching data
- Responsive design

## Prerequisites

- Node.js and npm installed
- Angular CLI installed globally
- .NET 6.0 SDK or later
- 

## Getting Started

### Backend (.NET API)

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/aberaitius/weather-app.git
   cd weather-app
   ```

2. **Navigate to the API Directory:**

   ```bash
   cd WeatherApi
   ```

3. **Add appsettings.json:**

   Create an `appsettings.json` file in the `WeatherApi` directory with the following content:

   ```json
   {
     "OpenWeatherMap": {
       "ApiKey": "your_openweathermap_api_key"
     }
   }
   ```

   Replace `your_openweathermap_api_key` with your actual OpenWeatherMap API key.

4. **Restore Dependencies and Run the API:**

   ```bash
   dotnet restore
   dotnet run
   ```

   The API should now be running at `http://localhost:5000`.

### Frontend (Angular Application)

1. **Navigate to the Angular Directory:**

   ```bash
   cd ../weather-app
   ```

2. **Install Dependencies:**

   ```bash
   npm install
   ```

3. **Run the Angular Application:**

   ```bash
   ng serve
   ```

   The application should now be running at `http://localhost:4200`.

## Project Structure

```
weather-app/
├── WeatherApi/                 # .NET API project
│   ├── Controllers/
│   │   └── WeatherController.cs
│   ├── appsettings.json        # Configuration file for API key
│   └── Program.cs
├── weather-app/                # Angular project
│   ├── src/
│   │   ├── app/
│   │   │   ├── weather-display/
│   │   │   │   ├── weather-display.component.ts
│   │   │   │   ├── weather-display.component.html
│   │   │   │   └── weather-display.component.less
│   │   │   ├── weather.service.ts
│   │   │   └── app.module.ts
│   │   └── index.html
│   ├── angular.json
│   ├── package.json
│   └── README.md
└── README.md                   # Project documentation
```

## Usage

- Open the application in your browser.
- Enter the name of the location you want to check the weather for.
- Click the "Get Weather" button.
- The weather information will be displayed along with an icon representing the current weather conditions.

## Dependencies

### Backend

- .NET 6.0 or later
- Newtonsoft.Json

### Frontend

- Angular 14
- Angular Material
- RxJS

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [OpenWeatherMap API](https://openweathermap.org/api) for providing weather data
- [Angular](https://angular.io/) for the front-end framework
- [Angular Material](https://material.angular.io/) for UI components

# 🔥 FireWatch — Wildfire Risk Dashboard

A live wildfire risk monitoring dashboard built with real satellite and weather data. Search any location in the world to see current fire danger conditions, active fire detections, air quality, and a 7-day forecast.

**[View Live Site](https://kaiscolieri.github.io/firewatch-dashboard/)**

-----

## Features

- **Live Fire Risk Score** — calculated from real-time temperature, humidity, wind, and precipitation
- **7-Day Forecast** — predicted fire risk for the next week based on weather forecasts
- **Air Quality Index** — live AQI with PM2.5, PM10, and CO readings
- **NASA Satellite Fire Map** — active fire detections from the VIIRS sensor updated every few hours
- **Risk Alerts** — save your email and a risk threshold to be reminded to check back
- **Share Button** — share a direct link to any location’s risk data
- **Mobile Friendly** — works on phones, tablets, and desktops

-----

## Data Sources

|Source                                                |Data                                    |Cost|
|------------------------------------------------------|----------------------------------------|----|
|[NASA FIRMS](https://firms.modaps.eosdis.nasa.gov)    |Active fire detections (VIIRS satellite)|Free|
|[Open-Meteo](https://open-meteo.com)                  |Weather & 7-day forecast                |Free|
|[Open-Meteo Air Quality](https://open-meteo.com)      |AQI, PM2.5, PM10, CO                    |Free|
|[OpenStreetMap / Nominatim](https://openstreetmap.org)|Maps & geocoding                        |Free|

**Total cost to run: $0**

-----

## How the Risk Score Works

The fire risk score (0–100) is calculated using a simplified Fire Weather Index:

- **Temperature** — higher temps increase risk (up to +40 points)
- **Humidity** — lower humidity increases risk (up to +35 points)
- **Wind Speed** — stronger winds increase risk (up to +20 points)
- **Precipitation** — recent rain reduces risk (up to -30 points)

|Score |Level      |Description                      |
|------|-----------|---------------------------------|
|0–19  |🟢 Low      |Minimal fire danger              |
|20–39 |🟡 Moderate |Some fire weather present        |
|40–59 |🟠 High     |Fires can start and spread easily|
|60–79 |🔴 Very High|Extreme caution required         |
|80–100|⛔ Extreme  |Critical fire danger             |

-----

## Tech Stack

- **HTML, CSS, JavaScript** — no frameworks, no build tools
- **Leaflet.js** — interactive map
- **Open-Meteo API** — weather & forecast data
- **NASA FIRMS API** — satellite fire data
- **Nominatim API** — location search
- **GitHub Pages** — free hosting

-----

## Getting Started

Just open `index.html` in any browser — no installation or setup required.

To run locally:

```
git clone https://github.com/yourusername/firewatch-dashboard
open index.html
```

-----

## Future Ideas

- [ ] Push notifications via service worker
- [ ] Historical fire data comparison
- [ ] Wind direction arrows on map
- [ ] Evacuation route integration

-----

Built as a student project to demonstrate real-world use of public APIs and satellite data for environmental monitoring.


#  Real-Time Weather Dashboard (Power BI)

An interactive Power BI dashboard that visualizes real-time weather data using a Weather API.  
This project demonstrates API integration, data transformation, and dashboard design.

---

## Features

-  Multi-city weather tracking (Mumbai, Jaipur, Gurgaon)
-  Real-time temperature & weather conditions
-  7-day forecast visualization
-  Wind speed, humidity, pressure, visibility
-  Sunrise & sunset timings
-  Air Quality Index (AQI) with pollutant breakdown
-  Chances of rain

---

##  Tech Stack

- Power BI
- Weather API
- Power Query (M)
- DAX

---

##  API Integration

Data is fetched using Weather API and transformed in Power Query.

Example:

```powerquery
Json.Document(
    Web.Contents(
        "https://api.weatherapi.com",
        [
            RelativePath = "v1/current.json",
            Query = [
                key = "YOUR_API_KEY",
                q = "Mumbai",
                aqi = "yes"
            ]
        ]
    )
)

# Eco-Route

An eco-friendly route navigation application that helps users find the most environmentally sustainable paths based on air quality, CO2 emissions, and weather conditions.

## Features

- 🌍 **Eco-Friendly Routing**: Find routes with the lowest environmental impact
- 📍 **Location-Based Air Quality**: Real-time AQI (Air Quality Index) data for different zones
- 🌡️ **Weather Integration**: Current weather conditions and precipitation probability
- 📊 **Environmental Metrics**: 
  - CO2 emissions calculation
  - Pollution index analysis
  - Eco-score for each route
- 👤 **User Authentication**: Secure signup and login system
- 🗺️ **Interactive Maps**: View routes with pollution levels
- 📈 **Real-time Streaming**: Live updates for AQI and weather data

## Tech Stack

- **Backend**: Flask (Python)
- **Database**: SQLite
- **Frontend**: HTML, CSS, JavaScript
- **APIs Used**:
  - OpenStreetMap Nominatim (Geocoding)
  - Project OSRM (Routing)
  - Open-Meteo (Weather & Air Quality)

## Project Structure

```
Eco-Route/
├── Eco-route/
│   ├── app.py              # Main Flask application
│   └── eco_route.db        # SQLite database
├── templates/
│   ├── welcome.html        # Welcome page
│   ├── login.html          # Login page
│   ├── signup.html         # Signup page
│   └── dashboard.html      # Main dashboard
├── static/
│   ├── css/
│   │   └── styles.css      # Stylesheet
│   └── js/
│       ├── app.js          # Main JavaScript
│       └── dashboard.js    # Dashboard logic
├── .gitignore
├── README.md
└── requirements.txt
```

## Installation

### Prerequisites
- Python 3.8+
- pip (Python package manager)

### Setup Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/Eco-Route.git
   cd Eco-Route
   ```

2. **Create virtual environment**
   ```bash
   python -m venv .venv
   .venv\Scripts\activate  # On Windows
   source .venv/bin/activate  # On macOS/Linux
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set environment variables (optional)**
   ```bash
   set ECO_ROUTE_SECRET=your_secret_key_here  # Windows
   export ECO_ROUTE_SECRET=your_secret_key_here  # macOS/Linux
   ```

5. **Run the application**
   ```bash
   cd Eco-route
   python app.py
   ```

6. **Access the app**
   Open your browser and navigate to: `http://localhost:5000`

## API Endpoints

### Authentication
- `POST /api/signup` - Register a new user
- `POST /api/login` - Login user
- `POST /api/logout` - Logout user
- `GET /api/profile` - Get current user profile

### Location & Routing
- `GET /api/geocode?q=location` - Geocode location name
- `GET /api/route` - Get eco-friendly routes
  - Parameters: `from_lat`, `from_lon`, `to_lat`, `to_lon`

### Environmental Data
- `GET /api/areas-metrics?speed_kmh=30` - Get area metrics
- `GET /api/aqi-stream?speed_kmh=30` - Stream AQI updates (Server-Sent Events)
- `GET /api/weather?lat=12.3&lon=76.6` - Get weather data
- `GET /api/weather-stream?lat=12.3&lon=76.6` - Stream weather updates (Server-Sent Events)

## Configuration

### Mysore Zones
The app includes predefined zones for Mysore, India with:
- Devaraja Mohalla
- VV Mohalla
- Kuvempunagar
- Jayalakshmipuram
- Saraswathipuram
- Chamundi Hills
- Hebbal

Each zone has latitude, longitude, radius, AQI level, and CO2 factor data.

## Database Schema

### Users Table
```sql
CREATE TABLE users (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    email TEXT UNIQUE NOT NULL,
    password_hash TEXT NOT NULL
)
```

## Usage

1. **Sign Up**: Create a new account with email and password
2. **Login**: Access your account
3. **Search Routes**: Enter source and destination locations
4. **View Results**: Compare eco-friendly vs polluted routes
5. **Check Metrics**: View AQI, CO2, and eco-score for each route
6. **Track Weather**: See real-time weather conditions

## Environmental Calculations

### Eco-Score Formula
```
Eco-Score = 100 - (0.6 * AQI_normalized + 0.4 * CO2_normalized)
```

### AQI Calculation
Uses Indian AQI standards based on PM2.5 and PM10 levels.

### CO2 Emissions
- Base: 0.192 kg CO2/km
- Varies by zone and speed

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see LICENSE file for details.

## Support

For issues, questions, or suggestions, please open an issue on GitHub or contact the development team.

## Future Enhancements

- [ ] Mobile app (React Native/Flutter)
- [ ] Historical data analysis
- [ ] Route sharing and favorites
- [ ] Multi-modal transportation options
- [ ] Carbon footprint tracking
- [ ] Integration with public transport APIs
- [ ] Machine learning for route optimization

## Acknowledgments

- OpenStreetMap for map data
- Project OSRM for routing
- Open-Meteo for weather and air quality data
- Flask community for the excellent framework

---

**Made with ♻️ for a sustainable future**

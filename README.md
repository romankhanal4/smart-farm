# Smart Farm

A comprehensive agricultural intelligence platform that empowers farmers with real-time data, predictive analytics, and expert guidance to maximize crop productivity and profitability.

## 📋 Table of Contents
- [About](#about)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies](#technologies)
- [API Documentation](#api-documentation)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## 🌾 About

Smart Farm is an IoT and AI-powered platform designed to help farmers make data-driven decisions. The app provides real-time monitoring of crops, weather conditions, soil health, and market prices while offering intelligent recommendations for irrigation, pest management, and harvesting.

**Mission**: Improve agricultural productivity and sustainability through technology.

## ✨ Features

### 📊 Crop Monitoring
- Real-time crop health tracking
- Disease detection using AI/ML
- Growth stage monitoring
- Yield prediction
- Field mapping and visualization

### 🌤️ Weather Intelligence
- Real-time weather updates
- 7-day weather forecasting
- Severe weather alerts
- Rainfall tracking
- Temperature and humidity monitoring

### 🌱 Soil Analytics
- Soil moisture monitoring
- Soil nutrient levels
- pH balance tracking
- Soil health recommendations
- Sensor data integration

### 💰 Market Insights
- Real-time crop prices
- Market trends and predictions
- Buyer connections
- Price history charts
- Seasonal analysis

### 💧 Smart Irrigation
- Automated irrigation scheduling
- Water usage optimization
- Soil moisture-based watering
- Cost-saving recommendations
- Weather-integrated scheduling

### 🤖 AI Assistant
- Farming tips and advice
- Disease identification
- Pest management recommendations
- Expert consultation
- Historical data analysis

### 👨‍🌾 Farmer Community
- Connect with other farmers
- Expert consultation marketplace
- Knowledge sharing forum
- Success stories and best practices

### 📈 Analytics Dashboard
- Comprehensive farm statistics
- Revenue tracking
- Resource usage analytics
- Performance comparisons
- Custom reports generation

## 🚀 Installation

### Prerequisites
- Node.js (v14+)
- MongoDB (v4.4+)
- Python 3.8+
- npm or yarn
- Redis (v6+)

### Backend Setup

```bash
# Clone the repository
git clone https://github.com/romankhanal4/smart-farm.git
cd smart-farm/backend

# Install dependencies
npm install

# Configure environment variables
cp .env.example .env
# Edit .env with your database and API keys

# Install ML dependencies
pip install -r requirements.txt

# Start the server
npm run dev
```

### Frontend Setup

```bash
cd ../frontend

# Install dependencies
npm install

# Configure API endpoint
cp .env.example .env
# Edit .env with your backend URL

# Start the app
npm start
```

### IoT Sensor Integration

```bash
cd ../iot

# Install sensor packages
pip install -r requirements.txt

# Configure sensor connections
python configure_sensors.py

# Start sensor data collection
python sensor_gateway.py
```

## 🎯 Usage

### Getting Started

1. **Register/Login**: Create an account or log in to Smart Farm
2. **Add Farm**: Register your farm with location and size details
3. **Connect Sensors**: Integrate IoT sensors for real-time monitoring
4. **Set Preferences**: Configure crop types, weather location, and goals
5. **Monitor & Act**: Receive insights and act on recommendations

### Key Features in Action

#### Crop Monitoring
```
1. Navigate to "My Crops" section
2. View real-time crop health metrics
3. Check disease alerts and recommendations
4. Track growth progress with photos
5. Get harvest readiness updates
```

#### Weather Planning
```
1. Check daily and weekly forecasts
2. Receive severe weather alerts
3. Plan irrigation based on rainfall
4. Adjust farming activities accordingly
```

#### Market Intelligence
```
1. View current market prices
2. Check price trends
3. Connect with buyers
4. Schedule sales based on market conditions
```

## 💻 Technologies

### Frontend
- **Framework**: React.js 18+
- **State Management**: Redux Toolkit
- **Maps**: Mapbox GL
- **Charts**: Chart.js & Recharts
- **UI Components**: Material-UI, Ant Design
- **Real-time**: Socket.io

### Backend
- **Runtime**: Node.js & Express.js
- **Database**: MongoDB with Mongoose
- **Cache**: Redis
- **Authentication**: JWT & OAuth2
- **API**: RESTful + GraphQL
- **Task Queue**: Bull

### AI/ML
- **Framework**: Python with TensorFlow
- **Disease Detection**: CNN models
- **Yield Prediction**: Time-series forecasting
- **Recommendations**: Collaborative filtering
- **NLP**: Chatbot for advice

### IoT & Integration
- **Sensors**: Arduino, Raspberry Pi
- **Communication**: MQTT, CoAP
- **Weather API**: OpenWeatherMap
- **SMS Alerts**: Twilio
- **Payment**: Stripe

### DevOps & Deployment
- **Containerization**: Docker & Docker Compose
- **Cloud**: AWS (EC2, S3, RDS)
- **CI/CD**: GitHub Actions
- **Monitoring**: Prometheus & Grafana
- **Logging**: ELK Stack

## 📁 Project Structure

```
smart-farm/
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Dashboard/
│   │   │   ├── CropMonitor/
│   │   │   ├── Weather/
│   │   │   └── Market/
│   │   ├── pages/
│   │   ├── redux/
│   │   └── utils/
│   └── package.json
├── backend/
│   ├── config/
│   ├── controllers/
│   │   ├── cropController.js
│   │   ├── weatherController.js
│   │   ├── marketController.js
│   │   └── userController.js
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── services/
│   └── server.js
├── iot/
│   ├── sensor_gateway.py
│   ├── data_processor.py
│   └── requirements.txt
├── ml/
│   ├── disease_detection/
│   ├── yield_prediction/
│   └── models/
├── docker-compose.yml
└── README.md
```

## 🔌 API Documentation

### Authentication
```
POST /api/auth/register
POST /api/auth/login
POST /api/auth/logout
GET /api/auth/profile
POST /api/auth/refresh-token
```

### Crops
```
GET /api/crops
POST /api/crops/create
PUT /api/crops/:id
DELETE /api/crops/:id
GET /api/crops/:id/health
POST /api/crops/:id/photos
```

### Weather
```
GET /api/weather/current
GET /api/weather/forecast
GET /api/weather/history
POST /api/weather/alerts
```

### Soil & Sensors
```
GET /api/sensors
POST /api/sensors/register
GET /api/sensors/:id/data
POST /api/soil/analysis
```

### Market
```
GET /api/market/prices
GET /api/market/trends
POST /api/market/sell
GET /api/market/buyers
```

### Analytics
```
GET /api/analytics/overview
GET /api/analytics/crop/:id
GET /api/analytics/farm/revenue
GET /api/analytics/resources
```

## 🗺️ Roadmap

### v1.0 (Current)
- ✅ Basic crop monitoring
- ✅ Weather integration
- ✅ Market price tracking
- ✅ User authentication

### v1.5 (Q3 2026)
- 🔄 Advanced disease detection
- 🔄 Irrigation automation
- 🔄 IoT sensor integration
- 🔄 Mobile app (React Native)

### v2.0 (Q4 2026)
- 📅 Blockchain for supply chain
- 📅 AI-powered advisory
- 📅 Drone integration
- 📅 Community marketplace

### v2.5+ (2027)
- 📅 Satellite imagery integration
- 📅 Autonomous farming features
- 📅 Multi-language support
- 📅 Advanced ML models

## 🤝 Contributing

We welcome contributions from developers, farmers, and agricultural experts!

### How to Contribute

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Make your changes
4. Write tests for new features
5. Commit your changes (`git commit -m 'Add AmazingFeature'`)
6. Push to the branch (`git push origin feature/AmazingFeature`)
7. Open a Pull Request

### Development Guidelines
- Follow existing code style
- Write meaningful commit messages
- Add tests for new features
- Update documentation
- Test on mobile devices

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👤 Author & Contact

**Roman Khanal**
- 📧 Email: romankhanal4@gmail.com
- 🐙 GitHub: [@romankhanal4](https://github.com/romankhanal4)
- 🌐 Portfolio: [Coming Soon]

## 🐛 Bug Reports & Feature Requests

Found an issue? Have a suggestion? [Open an issue](https://github.com/romankhanal4/smart-farm/issues)

## 💡 Acknowledgments

- OpenWeatherMap API
- Agricultural research institutions
- Open-source community
- Beta testers and farmers

## 📚 Resources

- [FAO Agricultural Technology](http://www.fao.org/)
- [Modern Farming Practices](https://www.agriculture.gov/)
- [IoT in Agriculture](https://iot.ieee.org/)

## 📞 Support

For technical support:
- 📧 Email: romankhanal4@gmail.com
- 💬 GitHub Issues: [Create Issue](https://github.com/romankhanal4/smart-farm/issues)
- 📖 Documentation: [Wiki](https://github.com/romankhanal4/smart-farm/wiki)

---

<div align="center">

### Empowering Farmers with Technology 🌾

Made with ❤️ by Roman Khanal

**Last Updated**: May 2026

</div>

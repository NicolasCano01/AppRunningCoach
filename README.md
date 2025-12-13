# 🏃 Running Coach Pro

An intelligent web-based training management system for marathon runners, featuring comprehensive analytics, session tracking, and performance insights.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## 🎯 Features

### 📊 Analytics Dashboard
- **Training Load Metrics**: Real-time CTL (Chronic Training Load), ATL (Acute Training Load), and TSB (Training Stress Balance) tracking
- **Performance Insights**: Pace progression analysis, zone distribution, and marathon time predictions
- **Injury Risk Assessment**: ACWR-based injury risk monitoring with actionable alerts
- **Visual Analytics**: Interactive charts powered by Recharts for training load trends, pace evolution, and zone distribution

### 📝 Session History Manager
- **Quick Logging**: Log any session type in under 60 seconds
- **Special Session Support**: 
  - Futsal (high-intensity soccer with automatic TSS calculations)
  - Pedicab shifts (cycling cross-training with route-based multipliers)
- **Advanced Filtering**: Filter by date range, session type, distance, and more
- **CRUD Operations**: Full create, read, update, and delete functionality
- **Data Export**: Export your training history to CSV or JSON

## 🚀 Live Demo

Visit the app: [Your-GitHub-Username.github.io/running-coach-pro](https://your-github-username.github.io/running-coach-pro)

## 💡 Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **React**: v18 (via CDN for simplified deployment)
- **Charts**: Recharts v2.1
- **Database**: Firebase Firestore
- **Styling**: Tailwind CSS
- **Fonts**: DM Sans, Space Mono

## 📦 Project Structure

```
running-coach-pro/
│
├── index.html              # Navigation landing page
├── AnalyticsPanel.html     # Analytics dashboard
├── HistoryPanel.html       # Session history manager
├── README.md               # This file
└── .gitignore             # Git ignore file
```

## 🛠️ Setup Instructions

### Prerequisites
- A web browser (Chrome, Firefox, Safari, or Edge)
- A Firebase account (free tier works perfectly)

### Firebase Configuration

1. **Create a Firebase Project**:
   - Go to [Firebase Console](https://console.firebase.google.com/)
   - Click "Add Project"
   - Follow the setup wizard

2. **Enable Firestore Database**:
   - In your Firebase project, go to "Firestore Database"
   - Click "Create Database"
   - Start in production mode
   - Choose a location close to you

3. **Get Your Firebase Config**:
   - Go to Project Settings (gear icon)
   - Scroll to "Your apps" section
   - Click the web icon (`</>`)
   - Copy your Firebase configuration

4. **Update Both Panel Files**:
   - Open `AnalyticsPanel.html` in a text editor
   - Find the `firebaseConfig` object (around line 186)
   - Replace with your configuration
   - Repeat for `HistoryPanel.html` (around line 60)

### Local Testing

1. Open `index.html` in your web browser
2. Click on either "Analytics" or "Session History"
3. You'll be prompted to sign in with Firebase Authentication

## 🌐 Deployment to GitHub Pages

See the **DEPLOYMENT_GUIDE.md** file for detailed step-by-step instructions on deploying to GitHub Pages.

## 📊 Training Methodology

This app implements evidence-based training load management:

### Training Load Calculations
- **TSS (Training Stress Score)**: Based on duration, intensity, and RPE
- **CTL (Chronic Training Load)**: 42-day exponential moving average (fitness)
- **ATL (Acute Training Load)**: 7-day exponential moving average (fatigue)
- **TSB (Training Stress Balance)**: CTL - ATL (form/readiness)
- **ACWR (Acute:Chronic Workload Ratio)**: Injury risk indicator

### Heart Rate Zones (based on LTHR of 165 bpm)
- **Z1 (Recovery)**: < 124 bpm
- **Z2 (Easy)**: 124-140 bpm
- **Z3 (Moderate)**: 140-157 bpm
- **Z4 (Threshold)**: 157-173 bpm
- **Z5 (VO2 Max)**: > 173 bpm

### Special Session Types

#### Futsal Sessions
- **Default Duration**: 60 minutes
- **Estimated TSS**: 95 (high intensity)
- **RPE**: 8/10
- **Zone Distribution**: Primarily Z4-Z5

#### Pedicab Sessions
- **Variable Duration**: 4-7 hours typical
- **TSS Calculation**: `hours × 12 × route_multiplier`
- **Route Multipliers**:
  - Flat: 1.0
  - Mixed: 1.15
  - Hilly: 1.3

## 🎯 Roadmap

- [x] Phase 1: History Panel (Session Management)
- [x] Phase 2: Analytics Panel (Performance Insights)
- [x] Phase 3: Integration (Navigation & Shared Firebase)
- [ ] Phase 4: AI Training Plan Generator
- [ ] Phase 5: Mobile App Conversion
- [ ] Phase 6: Strava Integration

## 🤝 Contributing

This is a personal project, but feedback and suggestions are welcome! Feel free to:
- Open an issue for bugs or feature requests
- Fork the repository and experiment
- Share your training insights

## 📝 License

MIT License - feel free to use this project for your own training needs.

## 👤 Author

**Nic** - Marathon runner based in Melbourne, Australia

- Training Philosophy: Evidence-based, data-driven approach
- Constraints: Tuesday futsal, Saturday pedicab work, Friday rest
- Goal: Sub-3:30 marathon

## 🙏 Acknowledgments

- Training load methodology based on TrainingPeaks and Joe Friel's work
- Analytics inspired by Strava and Garmin Connect
- Built with passion for running and data science

## 📧 Contact

For questions or suggestions, please open an issue on GitHub.

---

**Happy Running! 🏃‍♂️💨**

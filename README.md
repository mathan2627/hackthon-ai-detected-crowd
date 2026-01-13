# CrowdSense AI - People Powered Disaster Intelligence System

A real-time disaster reporting and AI-powered intelligence system that helps authorities respond faster and save lives during natural disasters like floods, fires, earthquakes, and cyclones.

## 🚨 Features

### Core Functionality
- **Real-time Disaster Reporting**: Citizens can submit disaster reports with location and description
- **AI-Powered Analysis**: Advanced AI analyzes reports to classify disaster types and assess severity
- **Live Interactive Map**: Real-time, color-coded disaster markers based on severity levels
- **Authority Dashboard**: Emergency response command center with statistics and critical zones
- **Duplicate Detection**: Automatic filtering and aggregation of similar reports from the same area
- **Severity Escalation**: AI automatically increases severity when multiple reports come from the same location

### AI Intelligence Features
- **Keyword-based Classification**: Identifies disaster types (flood, fire, earthquake, cyclone, other)
- **Severity Scoring**: Assigns risk levels (low, medium, high, critical) based on description analysis
- **Confidence Rating**: Auto-verifies high-confidence reports
- **Priority Recommendations**: AI suggests response priorities for authorities

### User Interface
- **Dark Emergency Theme**: Red, yellow, and green color indicators for severity levels
- **Responsive Design**: Works on desktop and mobile devices
- **Real-time Updates**: Live data refresh every 30 seconds
- **Geolocation Integration**: Automatic location detection for accurate reporting

## 🛠 Technology Stack

### Frontend
- **React.js** with React Router for navigation
- **TypeScript** for type safety
- **Tailwind CSS** for styling with emergency theme
- **Leaflet.js** for interactive mapping
- **TanStack Query** for data fetching and caching

### Backend
- **Node.js** with Express.js
- **ORPC** for type-safe API communication
- **MongoDB** with Mongoose for data storage
- **Better Auth** for authentication

### AI & Data Processing
- **Custom AI Analyzer** with keyword-based classification
- **Geospatial Queries** for duplicate detection
- **Real-time Aggregation** for statistics and trends

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or higher)
- MongoDB (optional - uses in-memory storage for demo)
- npm or yarn

### Installation

1. **Install dependencies**
   ```bash
   npm install
   ```

2. **Set up environment variables**
   
   Server (.env in apps/server/):
   ```
   DATABASE_URL=mongodb://localhost:27017/crowdsense-ai
   BETTER_AUTH_SECRET=your-secret-key-here
   BETTER_AUTH_URL=http://localhost:3000
   CORS_ORIGIN=http://localhost:5173
   ```
   
   Web (.env in apps/web/):
   ```
   VITE_SERVER_URL=http://localhost:3000
   ```

3. **Start the development servers**
   
   Backend server:
   ```bash
   npm run dev:server
   ```
   
   Frontend application:
   ```bash
   npm run dev:web
   ```

4. **Access the application**
   - Frontend: http://localhost:5173
   - Backend API: http://localhost:3000

## 📱 Usage

### For Citizens
1. **Report Emergency**: Navigate to "Report Emergency" and describe the disaster situation
2. **Share Location**: Allow location access for accurate incident mapping
3. **Submit Report**: AI analyzes and categorizes your report automatically

### For Authorities
1. **View Live Map**: Monitor real-time disaster reports with color-coded severity
2. **Authority Dashboard**: Access statistics, critical zones, and AI recommendations
3. **Priority Response**: Get AI-suggested priorities based on severity and duplicate reports

## 🎯 Project Structure

```
crowdsense-ai/
├── apps/
│   ├── web/                 # React frontend application
│   │   ├── src/routes/      # Page components
│   │   ├── src/components/  # Reusable UI components
│   │   └── src/utils/       # API client and utilities
│   └── server/              # Express backend server
├── packages/
│   ├── api/                 # API routes and business logic
│   │   ├── src/routers/     # ORPC route handlers
│   │   └── src/services/    # AI analyzer and demo storage
│   ├── db/                  # Database models and connection
│   ├── auth/                # Authentication configuration
│   └── env/                 # Environment variable validation
```

## 🤖 AI Analysis System

The AI analyzer uses keyword-based classification to:

### Disaster Type Detection
- **Flood**: Keywords like "flood", "water", "overflow", "submerged"
- **Fire**: Keywords like "fire", "smoke", "flames", "wildfire"
- **Earthquake**: Keywords like "earthquake", "tremor", "shake", "collapsed"
- **Cyclone**: Keywords like "cyclone", "hurricane", "storm", "wind"

### Severity Assessment
- **Critical**: "death", "killed", "trapped", "destroyed", "emergency"
- **High**: "injured", "damage", "evacuation", "dangerous", "urgent"
- **Medium**: "affected", "concern", "problem", "moderate"
- **Low**: "minor", "small", "light", "manageable"

### Smart Features
- **Duplicate Detection**: Identifies similar reports within 1km radius
- **Severity Escalation**: Automatically upgrades severity when multiple reports detected
- **Confidence Scoring**: Rates report reliability based on keyword matches

## 🚨 Emergency Notice

This system is designed to supplement, not replace, official emergency services. In case of immediate danger, always call your local emergency number first (911, 112, etc.).

## 🏆 Hackathon Project

This project was built for a hackathon to demonstrate:
- Real-time disaster intelligence gathering
- AI-powered emergency response optimization
- Community-driven disaster reporting
- Scalable emergency management platform

---

*Built with Better-T-Stack: React, React Router, Express, ORPC, TypeScript, TailwindCSS, MongoDB, and more.*

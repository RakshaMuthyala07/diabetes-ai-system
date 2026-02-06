# AI Diabetes Risk Intelligence System

> A premium, hospital-grade web application for predicting diabetes risk using advanced machine learning algorithms

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?logo=chartdotjs&logoColor=white)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Demo](#demo)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Data Source](#data-source)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

The **AI Diabetes Risk Intelligence System** is a sophisticated web-based application that leverages machine learning to predict diabetes risk based on clinical parameters. Built with a focus on user experience and medical-grade accuracy, this system provides:

- **Real-time risk assessment** with interactive visualizations
- **Feature importance analysis** to understand key risk factors
- **Personalized health recommendations** based on patient data
- **Comprehensive prediction history** tracking
- **Professional PDF report generation**

This project demonstrates the practical application of AI in healthcare, combining data science with modern web development to create an accessible diagnostic tool.

##  Features

### Core Functionality

- **ML-Powered Predictions**: Advanced risk scoring algorithm trained on 768 clinical cases
- **Interactive Dashboard**: Real-time visualization of diabetes risk metrics
- **Feature Analysis**: Horizontal bar chart showing contribution of each health parameter
- **Risk Categorization**: Automatic classification into Low, Moderate, or High risk levels
- **History Tracking**: Complete log of all predictions with local storage

###  User Interface

- **Premium Design**: Dark, sophisticated interface with glassmorphism effects
- **Smooth Animations**: Fade-in effects, hover states, and progress animations
- **Responsive Layout**: Works seamlessly on desktop, tablet, and mobile devices
- **Circular Progress Gauge**: Animated risk score visualization
- **Multi-Page Navigation**: Dashboard, History, Analytics, and About sections

###  Visualizations

- **Feature Importance Chart**: Bar chart showing parameter contributions
- **Risk Distribution**: Doughnut chart analyzing prediction patterns
- **Performance Metrics**: Radar chart displaying model accuracy
- **Real-time Stats**: Live counters for predictions and risk levels

###  Health Features

- **Smart Recommendations**: Context-aware health advice based on input parameters
- **PDF Report Export**: Downloadable assessment reports
- **Medical Disclaimers**: Appropriate warnings about consulting healthcare professionals
- **Data Privacy**: All processing done locally in the browser

##  Demo

**Live Demo**: file:///C:/Users/raksh/Downloads/diabetes-dashboard.html

### Screenshots

<img width="1916" height="996" alt="image" src="https://github.com/user-attachments/assets/5ac56a5f-385d-44df-8458-ca6913c00224" />
<img width="1897" height="993" alt="image" src="https://github.com/user-attachments/assets/647bb1b9-2028-4d89-ae43-b8b0a2065387" />
<img width="1893" height="995" alt="image" src="https://github.com/user-attachments/assets/d7ca3530-e870-480e-b92b-5435e40528a2" />
<img width="1893" height="993" alt="image" src="https://github.com/user-attachments/assets/aef7621a-f39b-43cc-8903-8a075814e5a8" />
<img width="1894" height="1068" alt="image" src="https://github.com/user-attachments/assets/820dd798-8e87-403a-82b0-ea2b86bd7177" />
<img width="1906" height="995" alt="image" src="https://github.com/user-attachments/assets/e384d925-d82d-491d-8216-f8e6e3875e84" />
<img width="1918" height="996" alt="image" src="https://github.com/user-attachments/assets/bf78795f-5d14-4087-aabc-1194bd70a1d5" />
<img width="1866" height="823" alt="image" src="https://github.com/user-attachments/assets/00c144e2-1e20-4d28-97c8-a5f0aee91b22" />
<img width="1473" height="806" alt="image" src="https://github.com/user-attachments/assets/7f701d5b-b8bb-401a-8242-e8624e73e526" />


##  Installation

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- No server or backend required - runs entirely in the browser!

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/RakshaMuthyala07/diabetes-ai-system.git
   cd diabetes-ai-system
   ```

2. **Open the application**
   ```bash
   # Simply open index.html in your browser
   # On macOS:
   open index.html
   
   # On Linux:
   xdg-open index.html
   
   # On Windows:
   start index.html
   ```

3. **Or use a local server (optional)**
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx http-server
   
   # Then visit http://localhost:8000
   ```

That's it! No installation, no dependencies, no configuration needed.

##  Usage

### Making a Prediction

1. **Navigate to the Dashboard**
2. **Enter Patient Parameters**:
   - Pregnancies (0-17)
   - Glucose Level (0-200 mg/dL)
   - Blood Pressure (0-122 mm Hg)
   - Skin Thickness (0-99 mm)
   - Insulin Level (0-846 μU/ml)
   - BMI (0.0-67.1 kg/m²)
   - Diabetes Pedigree Function (0.078-2.42)
   - Age (21-81 years)

3. **Click "Analyze Risk"**
4. **View Results**:
   - Risk score percentage
   - Risk level classification
   - Feature importance breakdown
   - Personalized recommendations

5. **Download PDF Report** (optional)

### Viewing History

- Navigate to the **History** page to see all past predictions
- View timestamps, risk scores, and key parameters
- Track patterns over time

### Analytics Dashboard

- See risk distribution across all predictions
- View model performance metrics
- Analyze trends in your data

##  How It Works

### Machine Learning Model

The system uses a **Random Forest-inspired algorithm** trained on the Pima Indians Diabetes Database:

1. **Data Normalization**: All input features are normalized to 0-1 scale
2. **Weight-Based Scoring**: Each parameter contributes to the final risk score:
   - **Glucose** (35%): Primary indicator
   - **BMI** (25%): Body composition factor
   - **Age** (12%): Age-related risk
   - **Diabetes Pedigree** (15%): Genetic predisposition
   - **Insulin** (8%): Metabolic health
   - **Blood Pressure** (5%): Cardiovascular factor

3. **Interaction Effects**: The model considers combinations:
   - High glucose + High BMI = Increased risk
   - Advanced age + High pedigree = Elevated risk

4. **Risk Classification**:
   - **0-39%**: Low Risk
   - **40-59%**: Moderate Risk
   - **60-100%**: High Risk

### Feature Importance Calculation

Each input parameter's contribution is calculated and visualized to help users understand which factors are driving their risk score.

## 🛠️ Technologies Used

### Frontend
- **HTML5**: Semantic markup and structure
- **CSS3**: Custom styling with CSS variables and animations
- **JavaScript (ES6+)**: Application logic and interactivity

### Libraries
- **[Chart.js](https://www.chartjs.org/)**: Data visualization
- **[jsPDF](https://github.com/parallax/jsPDF)**: PDF generation

### Design
- **Google Fonts**: Archivo and JetBrains Mono
- **Glassmorphism**: Modern UI design pattern
- **CSS Grid & Flexbox**: Responsive layouts

## 📁 Project Structure

```
diabetes-ai-system/
│
├── index.html              # Main application file
├── README.md               # Project documentation
├── LICENSE                 # MIT License
|
│
├── assets/
│   └── diabetes_data.csv   # Training dataset (768 samples)
│
├── docs/
│   ├── SETUP_GUIDE.md      # Detailed setup instructions
│   ├── USER_MANUAL.md      # User guide
│   └── API_REFERENCE.md    # JavaScript API documentation
│
└── screenshots/
    ├── dashboard.png       # Dashboard screenshot
    ├── results.png         # Results page screenshot
    └── analytics.png       # Analytics screenshot
```

## 📊 Data Source

This project uses the **Pima Indians Diabetes Database**, originally from the National Institute of Diabetes and Digestive and Kidney Diseases.

**Dataset Details**:
- **Samples**: 768 patient records
- **Features**: 8 diagnostic measurements
- **Target**: Binary outcome (diabetes/no diabetes)
- **Source**: [UCI Machine Learning Repository](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)

**Features**:
1. Pregnancies
2. Glucose concentration
3. Blood pressure
4. Skin thickness
5. Insulin levels
6. Body Mass Index (BMI)
7. Diabetes pedigree function
8. Age

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/AmazingFeature`)
3. **Commit your changes** (`git commit -m 'Add some AmazingFeature'`)
4. **Push to the branch** (`git push origin feature/AmazingFeature`)
5. **Open a Pull Request**


### Ideas for Contribution

-  UI/UX improvements
- Additional visualizations
-  Model accuracy improvements
-  Multi-language support
-  Accessibility enhancements
-  Mobile app version
-  Backend integration for data persistence

## License

This project is licensed under the MIT License - see the [LICENSE] file for details.

##  Medical Disclaimer

**IMPORTANT**: This application is designed for **educational and research purposes only**. It is NOT intended to replace professional medical advice, diagnosis, or treatment.

- Always seek the advice of qualified healthcare providers
- Never disregard professional medical advice
- Do not delay seeking medical attention based on this tool
- This is a demonstration project, not a certified medical device

## Author

**[Raksha Muthyala]**

- GitHub: [@RakshaMuthyala07](https://github.com/RakshaMuthyala07)
- Email: rakshamuthyala@gmail.com


##  Acknowledgments

- Pima Indians Diabetes Database contributors
- Chart.js team for excellent visualization library
- The open-source community for inspiration and tools


##  Future Enhancements

- [ ] Integration with real medical databases
- [ ] Advanced ML models (Neural Networks, XGBoost)
- [ ] User authentication and data persistence
- [ ] Mobile application (React Native)
- [ ] API for third-party integrations
- [ ] Multi-factor risk assessment
- [ ] Real-time monitoring dashboard
- [ ] Integration with wearable devices

## Star History

If you find this project useful, please consider giving it a star! ⭐

---


# User Manual - AI Diabetes Risk Intelligence System

## Welcome! 👋

This guide will help you understand and use the AI Diabetes Risk Intelligence System effectively.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Understanding the Dashboard](#understanding-the-dashboard)
3. [Making a Prediction](#making-a-prediction)
4. [Interpreting Results](#interpreting-results)
5. [Using Advanced Features](#using-advanced-features)
6. [Tips for Best Results](#tips-for-best-results)
7. [FAQs](#faqs)

---

## Getting Started

### What is This System?

The AI Diabetes Risk Intelligence System is a web-based tool that predicts diabetes risk based on medical parameters. It uses machine learning algorithms trained on 768 real patient cases.

### Who Should Use This?

- Students learning about ML and healthcare AI
- Researchers studying diabetes prediction
- Developers building similar systems
- Anyone interested in understanding diabetes risk factors

⚠️ **Important:** This is for educational purposes only. Always consult healthcare professionals for medical advice.

### System Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (for loading Chart.js library)
- No login required
- No installation needed

### Opening the Application

Simply open `index.html` in your web browser. That's it!

---

## Understanding the Dashboard

### Main Sections

The dashboard has 4 main pages accessible from the left sidebar:

#### 1. 📊 Dashboard (Main Page)
- Statistics overview
- Patient parameter input form
- Risk assessment results
- Health recommendations

#### 2. 📜 History
- View all past predictions
- See patterns over time
- Track changes in risk levels

#### 3. 📈 Analytics
- Risk distribution charts
- Model performance metrics
- Data visualization

#### 4. ℹ️ About
- System information
- Model details
- Medical disclaimer

### Top Statistics Cards

- **Total Predictions**: How many analyses you've run
- **Avg Risk Score**: Average risk across all predictions
- **High Risk Cases**: Number of high-risk assessments

---

## Making a Prediction

### Step-by-Step Guide

#### Step 1: Navigate to Dashboard

Click **Dashboard** in the left sidebar (should be selected by default).

#### Step 2: Enter Patient Parameters

Fill in all 8 required fields:

| Parameter | Range | What It Means | Example |
|-----------|-------|---------------|---------|
| **Pregnancies** | 0-17 | Number of times pregnant | 3 |
| **Glucose** | 0-200 mg/dL | Plasma glucose concentration | 120 |
| **Blood Pressure** | 0-122 mm Hg | Diastolic blood pressure | 80 |
| **Skin Thickness** | 0-99 mm | Triceps skin fold thickness | 25 |
| **Insulin** | 0-846 μU/ml | 2-hour serum insulin | 100 |
| **BMI** | 0-67.1 | Body Mass Index | 28.5 |
| **Diabetes Pedigree** | 0.078-2.42 | Genetic diabetes risk score | 0.5 |
| **Age** | 21-81 years | Patient age | 45 |

**Input Helpers:**
- Each field shows the valid range below it
- Hover over labels for more information
- Red border appears if input is invalid

#### Step 3: Click "Analyze Risk"

- The system will show a loading animation
- Processing takes about 1.5 seconds
- Results appear automatically

#### Step 4: View Results

The page scrolls to show your results in multiple sections.

---

## Interpreting Results

### 1. Risk Score Gauge

**Circular Progress Indicator:**
- Shows your risk percentage (0-100%)
- Color changes based on risk level:
  - 🟢 **Green (0-39%)**: Low Risk
  - 🟡 **Yellow (40-59%)**: Moderate Risk
  - 🔴 **Red (60-100%)**: High Risk

**Animated Counter:**
- Counts up to your actual score
- Makes it easy to see the final number

### 2. Risk Level Badge

**Color-coded classification:**

- **Low Risk** (Green)
  - Score: 0-39%
  - Minimal diabetes risk
  - Continue healthy practices

- **Moderate Risk** (Yellow)
  - Score: 40-59%
  - Some risk factors present
  - Lifestyle changes recommended

- **High Risk** (Red)
  - Score: 60-100%
  - Elevated risk indicators
  - Medical consultation advised

### 3. Feature Importance Chart

**Horizontal Bar Chart showing:**
- Which parameters contributed most to your score
- Percentage contribution of each factor
- Sorted from highest to lowest impact

**How to Read It:**
- Longer bars = greater influence on risk score
- Typically, Glucose and BMI are top contributors
- Helps understand which factors to focus on

### 4. Health Recommendations

**Personalized advice based on your inputs:**

Example recommendations might include:

🍎 **Monitor Blood Glucose**
- Triggered if: Glucose > 140 mg/dL
- Advice: Regular monitoring, dietary adjustments

🏃 **Weight Management**
- Triggered if: BMI > 30
- Advice: Balanced diet, regular exercise

🩺 **Regular Checkups**
- Triggered if: Age > 45 or high pedigree score
- Advice: Schedule health screenings

❤️ **Blood Pressure Control**
- Triggered if: Blood Pressure > 80 mm Hg
- Advice: Monitor regularly, reduce sodium

🥗 **Healthy Diet**
- Always included
- General nutritional advice

💧 **Stay Hydrated**
- Always included
- Importance of water intake

### 5. Download PDF Report

Click the **Download PDF** button to get a report containing:
- Risk score and level
- All input parameters
- Date and time of assessment
- Medical disclaimer

---

## Using Advanced Features

### History Tracking

**Accessing History:**
1. Click **History** in the sidebar
2. View table of all predictions
3. See date, time, risk score, and key parameters

**What's Stored:**
- Timestamp of each prediction
- Risk score percentage
- Risk level classification
- All 8 input parameters

**Data Persistence:**
- Stored in browser's localStorage
- Persists across sessions
- Cleared if you clear browser data

### Analytics Dashboard

**Risk Distribution Chart:**
- Pie chart showing breakdown of Low/Moderate/High risk predictions
- Helps identify patterns in your assessments

**Model Performance Metrics:**
- Radar chart showing model accuracy
- Metrics include: Precision, Recall, F1-Score, Accuracy, AUC-ROC
- All metrics ~95% (demonstration values)

### Resetting the Form

Click the **Reset** button to:
- Clear all input fields
- Hide results section
- Start fresh with a new prediction

---

## Tips for Best Results

### Data Entry Tips

1. **Be Accurate**: Enter precise values from medical records
2. **Use 0 for Unknown**: If a value is unknown, enter 0
3. **Check Units**: Make sure you're using the correct units
4. **Double-check**: Review all entries before analyzing

### Understanding Limitations

**This System:**
- ✅ Demonstrates ML concepts
- ✅ Shows risk factor relationships
- ✅ Provides educational insights

**This System Does NOT:**
- ❌ Replace medical diagnosis
- ❌ Provide treatment plans
- ❌ Guarantee accuracy for real patients
- ❌ Store data on servers (all local)

### Privacy & Security

**Your Data:**
- Processed entirely in your browser
- Never sent to any server
- Stored only in browser localStorage
- Cleared when you clear browser data

**To Clear History:**
```javascript
// Open browser console (F12) and run:
localStorage.clear();
// Then refresh the page
```

---

## FAQs

### General Questions

**Q: Is this medically accurate?**
A: This is an educational demonstration. For medical decisions, always consult healthcare professionals.

**Q: Do I need to install anything?**
A: No! Just open index.html in a browser.

**Q: Can I use this offline?**
A: Partially. The app works offline except for Chart.js which loads from CDN.

**Q: Is my data safe?**
A: Yes. All processing happens in your browser. Nothing is sent to servers.

### Technical Questions

**Q: Which browsers are supported?**
A: All modern browsers: Chrome, Firefox, Safari, Edge (latest versions).

**Q: Why is the chart not showing?**
A: You need an internet connection to load Chart.js library.

**Q: Can I export my history?**
A: Currently no, but you can manually copy data from the History table.

**Q: How is the risk score calculated?**
A: Using a weighted algorithm based on normalized input values. See the About page for details.

### Troubleshooting

**Q: The app isn't loading properly**
A: Try:
- Hard refresh (Ctrl+Shift+R or Cmd+Shift+R)
- Clear browser cache
- Try a different browser
- Check browser console for errors (F12)

**Q: PDF download isn't working**
A: 
- Ensure pop-ups are not blocked
- Try a different browser
- Check if jsPDF library loaded (needs internet)

**Q: My history disappeared**
A: History is stored in localStorage. It's cleared when you:
- Clear browser data
- Use incognito/private mode
- Manually clear localStorage

**Q: Results seem inconsistent**
A: The model uses a simplified algorithm for demonstration. Small input changes can affect results.

---

## Understanding the Science

### How Machine Learning Works Here

1. **Data Normalization**: Each input is scaled to 0-1 range
2. **Feature Weighting**: Important features get higher weights
3. **Score Calculation**: Weighted sum of normalized values
4. **Classification**: Score converted to Low/Moderate/High

### Key Risk Factors (in order of importance)

1. **Glucose Level** (35% weight) - Most critical
2. **BMI** (25% weight) - Body composition
3. **Diabetes Pedigree** (15% weight) - Genetics
4. **Age** (12% weight) - Age-related risk
5. **Insulin** (8% weight) - Metabolic health
6. **Blood Pressure** (5% weight) - Cardiovascular

### Model Accuracy

- Trained on: 768 patient records
- Accuracy: ~95% (demonstration)
- Source: Pima Indians Diabetes Database

---

## Best Practices

### For Students

- Experiment with different values
- Note which factors change risk most
- Compare multiple scenarios
- Use for learning, not diagnosis

### For Developers

- Review the code to understand ML implementation
- Modify weights to see effect on predictions
- Add new features or visualizations
- Use as a template for similar projects

### For Researchers

- Understand the limitations
- Don't use for actual medical research
- Use as a teaching tool
- Cite the Pima Indians dataset if referencing

---

## Additional Resources

### Learning More

- **Machine Learning**: [Coursera ML Course](https://www.coursera.org/learn/machine-learning)
- **Diabetes Info**: [American Diabetes Association](https://www.diabetes.org)
- **Web Development**: [MDN Web Docs](https://developer.mozilla.org)

### Dataset Information

- **Source**: UCI Machine Learning Repository
- **Name**: Pima Indians Diabetes Database
- **Link**: [Kaggle Dataset](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)

---

## Support & Feedback

### Getting Help

- Check this manual first
- Review the code comments
- Open an issue on GitHub
- Contact the developer

### Providing Feedback

We welcome feedback! Please:
- Report bugs via GitHub Issues
- Suggest features
- Share your experience
- Contribute improvements

---

## Medical Disclaimer

⚠️ **IMPORTANT MEDICAL DISCLAIMER**

This application is for **educational and demonstration purposes only**.

**This tool:**
- Is NOT a medical device
- Is NOT approved by any health authority
- Should NOT be used for medical diagnosis
- Should NOT replace professional medical advice

**Always:**
- Consult qualified healthcare providers
- Seek professional medical advice
- Get proper medical testing
- Follow your doctor's recommendations

**Never:**
- Self-diagnose based on this tool
- Delay seeking medical attention
- Make treatment decisions without consulting doctors
- Share results as medical evidence

---

## Conclusion

Thank you for using the AI Diabetes Risk Intelligence System! This tool demonstrates the power of machine learning in healthcare while emphasizing the importance of professional medical care.

Remember:
- This is a learning tool
- Real medical decisions need professional input
- Have fun exploring the technology
- Share your learnings with others!

---

**Questions or suggestions? Feel free to reach out!**

*Last updated: January 2026*

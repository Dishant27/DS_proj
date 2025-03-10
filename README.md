# 📊 Data Science Salary Estimator

![Python](https://img.shields.io/badge/Python-3.7-blue.svg?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-WebScraping-green.svg?style=for-the-badge&logo=selenium&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-red.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

## 📋 Project Overview

This project implements an end-to-end data science pipeline to predict data scientist salaries based on job postings from Glassdoor. From web scraping to model deployment, it demonstrates key data science skills including data collection, cleaning, exploratory analysis, feature engineering, and predictive modeling.

## 🎯 Project Objectives

- Develop an automated data collection system for Glassdoor job listings
- Clean and preprocess salary and job description data
- Extract valuable features from text job descriptions
- Build and compare multiple machine learning models for salary prediction
- Provide insights into factors influencing data scientist compensation

## 🔍 Key Features

- **Automated Web Scraping**: Custom Selenium-based scraper for Glassdoor job postings
- **Text Analysis**: NLP techniques to extract skills and requirements from job descriptions
- **Feature Engineering**: Creation of meaningful variables from raw job posting data
- **Predictive Modeling**: Implementation of regression models to predict salary ranges
- **Interactive Visualization**: Salary trends across locations, experience levels, and skills

## 📈 Project Workflow

1. **Data Collection**
   - Automated Glassdoor scraping using Selenium WebDriver
   - Collection of job title, company, location, salary, and full job descriptions
   - Storage in structured format for analysis

2. **Data Cleaning & Preprocessing**
   - Handling missing values and outliers
   - Normalizing company names and locations
   - Extracting salary data from various formats
   - Converting text descriptions to analyzable features

3. **Exploratory Data Analysis**
   - Distribution of salaries across locations and company sizes
   - Correlation between skills mentioned and compensation
   - Visualization of market trends for data science roles

4. **Feature Engineering**
   - Text parsing to identify required skills and technologies
   - Creation of categorical variables for company size, industry, etc.
   - Development of experience level indicators
   - Geographic grouping for regional analysis

5. **Model Building**
   - Linear Regression
   - Random Forest
   - Gradient Boosting
   - Neural Networks
   - Model comparison and evaluation

6. **Model Deployment**
   - Serialization of best performing model
   - Development of prediction API
   - Simple web interface for salary estimation

## 🛠️ Technical Stack

- **Python 3.7**
- **Data Collection**: Selenium, BeautifulSoup, Requests
- **Data Processing**: Pandas, NumPy
- **Data Visualization**: Matplotlib, Seaborn
- **Machine Learning**: Scikit-learn, TensorFlow/Keras
- **NLP**: NLTK, SpaCy
- **Deployment**: Flask, Heroku

## 📊 Sample Results

Initial analysis from the collected data reveals:

- Average data scientist salary: $XXX,XXX
- Highest paying locations: San Francisco, Seattle, New York
- Most valuable skills: Python, SQL, AWS, Deep Learning
- Company size correlation: +X% for enterprise companies

## 🖥️ Setup and Installation

```bash
# Clone the repository
git clone https://github.com/Dishant27/DS_proj.git
cd DS_proj

# Install required packages
pip install -r requirements.txt

# Download ChromeDriver for your Chrome version
# Place it in the project directory or add to PATH

# Run the Glassdoor scraper
python glassdoor_scraper.py

# Run the data analysis notebook
jupyter notebook salary_analysis.ipynb
```

## 🚀 Usage

### Data Collection
```python
from glassdoor_scraper import GlassdoorScraper

# Initialize the scraper
scraper = GlassdoorScraper()

# Collect job listings
jobs = scraper.get_jobs(keyword="data scientist", location="United States", num_jobs=15)

# Save to CSV
jobs.to_csv("data_scientist_jobs.csv", index=False)
```

### Salary Prediction
```python
from salary_predictor import SalaryPredictor

# Load the trained model
predictor = SalaryPredictor.load_model("models/gbm_model.pkl")

# Predict salary for a job
salary_range = predictor.predict({
    "title": "Senior Data Scientist",
    "location": "San Francisco",
    "skills": ["Python", "SQL", "AWS", "Machine Learning"],
    "experience_years": 5
})

print(f"Estimated salary range: ${salary_range[0]:,.2f} - ${salary_range[1]:,.2f}")
```

## 📈 Project Status

- [x] Project planning and repository setup
- [x] Implement Glassdoor scraper
- [x] Collect initial dataset (15 job postings)
- [ ] Data cleaning and preprocessing
- [ ] Exploratory data analysis
- [ ] Feature engineering
- [ ] Model training and evaluation
- [ ] Model deployment and API development

## 📚 Resources & References

- [Selenium Tutorial for Glassdoor Scraping](https://towardsdatascience.com/selenium-tutorial-scraping-glassdoor-com-in-10-minutes-3d0915c6d905)
- [ChromeDriver Downloads](https://chromedriver.chromium.org/downloads)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
- [Kaggle's Data Science Salary Dataset](https://www.kaggle.com/datasets/kaggle/ds-jobs-survey-2018)

## 🔮 Future Improvements

- Expand dataset with more job postings and global locations
- Implement advanced NLP techniques for better feature extraction
- Add time-series analysis of salary trends
- Create interactive dashboard for exploring results
- Implement continuous data collection for up-to-date predictions

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

Dishant - [GitHub Profile](https://github.com/Dishant27)

---

**Note**: This project is for educational purposes and is not affiliated with Glassdoor.
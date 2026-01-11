# pfda-project
by Zoe McNamara Harlowe

### Welcome to my submission for the assessment for the Programming for Data Analytics module. This module is provided by ATU (Atlantic Technological University) as part of the HDip in Computing in Data Analytics.

---

## Table of Contents

1. [Prerequisites](#prerequisites)  
2. [Setup](#setup)
3. [Technologies](#technologies)
4. [Libraries](#libraries)
5. [Project Structure](#project-structure)
6. [Preprocessing](#preprocessing)   
7. [Analysis of the Datasets](#analysis-of-the-datasets)

---

## Prerequisites

- Python 3.7 or higher  
- Required packages (listed in `requirements.txt`):  
  ```bash
  numpy
  scikit-learn
  pandas
  matplotlib
  seaborn


---

## Setup

**View the repository online using Github Codespaces:**
1. Sign up for a free Github account.
2. Go to the repository page in your browser.
3. Click the green 'Code' button.
4. Click the 'Codespaces' tab.
5. Click 'Create New Codespace' on main.


**Or you can clone the repository onto your own machine:**
1. In Commander, clone the repo and change directory:
```bash 
git clone <https://github.com/zoeharlowe/pfda-projectt>
cd <pfda-project>
```
2. Install dependencies:
```bash
pip install -r requirements.txt
```
3. Launch the Jupyter Notebook weather_project.ipynb locally:
```bash
jupyter notebook weather_project.ipynb
```

--- 

## Technologies

- Python
- Git
- Github
- Codespaces
- Jupyter

---

## Libraries & Packages

- Numpy: https://numpy.org/doc/2.3/user/absolute_beginners.html
- Scikit-learn: https://scikit-learn.org/
- Matplotlib: https://matplotlib.org/3.5.3/api/_as_gen/matplotlib.pyplot.html
- Seaborn: https://seaborn.pydata.org/
- Pandas: https://pandas.pydata.org/

--- 

## Project Structure

### PFDA Project:
- .gitignore
- README.md            
- requirements.txt
- dublin_data.csv
- shannon_data.csv
- Images
- Plots      
- weather_project.ipynb:
  - [Imports](weather_project.ipynb#imports)
  - [Notebook Layout](weather_project.ipynb#notebook-layout)
  - [1. Retrieve the Dataset](weather_project.ipynb#1-retrieve-the-dataset)
  - [2. Clean the Dataset](weather_project.ipynb#2-clean-the-dataset)
  - [3. Analyse the Dataset](weather_project.ipynb#3-analyse-the-dataset)
  - [4. Conclusion](weather_project.ipynb#4-conclusion)

---

## Preprocessing
I sourced both the Dublin and Shannon Airport hourly weather data from: https://www.met.ie/climate/available-data/historical-data

**Other references:**
- *str.strip() method documentation:* https://docs.python.org/3.6/library/stdtypes.html
- *pd.df.dropna() documentation:* https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.dropna.html
- *pd.df.set_index() documentation:* https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.set_index.html

---

## Analysis of the Datasets

### (a) Mean Wind Speed
I first found the hourly, daily, monthly and yearly mean wind speeds in both Shannon and Dublin Airports. I plotted all results using individual and multiple plots on one figure and compared with one another.

**References:** 
  - *pd.date_range documentation:* https://pandas.pydata.org/docs/reference/api/pandas.date_range.html
  - *Conversation with ChatGPT about formatting datetime x-ticks:* https://chatgpt.com/share/693177e4-c100-800c-a547-01ab88af2e68
  - *Week 9 Visualisation: Multiple axes on one fig - Andrew Beatty:* https://github.com/andrewbeattycourseware/PFDA-courseware/blob/main/code/Topic09-plots/Lectures/lecture%203%20axis.ipynb
  - *df.resample.mean() and .max() method:* https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.resample.html

### (b) Max Wind Speed
Using the same resample method as I used for mean windspeed, I found the maximum wind speed for both airports on a daily, monthly and yearly scale and did some interpretation of the plots I created.

**References:**
  - *Photo of Shannon Airport in 1959:* https://www.theguardian.com/cities/2016/apr/19/story-of-cities-25-shannon-ireland-china-economic-boom
  - *Photo of Shannon Airport in 2018:* https://www.limerickpost.ie/2018/12/18/things-are-looking-up-at-shannon-airport/

### (c) Wind Speed by Month
In this section I look at the highest and lowest winds on average per month in each airport. I create a plot displaying the windspeed by month of the two airports and compare and contrast with one another.

**References:**
  - *Conversation with ChatGPT about grouping months:* https://chatgpt.com/share/693177e4-c100-800c-a547-01ab88af2e68

### (d) Correlation Matrix
I created a correlation matrix displaying the relationship between certain features in each dataset to show the effect different weather features have on one another. I used this information to build a machine learning model in the next step.

**References:**
  - *pd.df.corr() documentation:* https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.corr.html
  - *GeeksForGeeks guide to creating a correlation matrix:* https://www.geeksforgeeks.org/data-science/create-a-correlation-matrix-using-python/

### (e) Making Predictions
I built a predictive model using Linear Regression to predict the relative humidity in each airport using other features in the dataset (temperature, dew point temp, windspeed, vapour pressure, sunshine, wind direction and visibility).

**References:**
- *GeeksForGeeks guide on using linear regression to predict rainfall:* https://www.geeksforgeeks.org/machine-learning/ml-rainfall-prediction-using-linear-regression/
- *Humidity impact on aircraft performance guide:* https://simpleflying.com/humidity-impact-on-aircraft-performance-guide/
- *Topic 7 Regression - Andrew Beatty:* https://atlantictu-my.sharepoint.com/personal/andrew_beatty_atu_ie/_layouts/15/stream.aspx?id=%2Fpersonal%2Fandrew%5Fbeatty%5Fatu%5Fie%2FDocuments%2FPFDA%20private%202025%2Fvideos%2FPFDA7%2E03%20regression%2Emp4&ga=1&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2E3dec4e1e%2Df99e%2D46f1%2Da9d5%2D2d531f6aa154
- *What is a Residual Plot?* https://dovetail.com/research/what-is-a-residual-plot/
- *Conversation with Copilot on plot interpretation:* https://copilot.microsoft.com/shares/aCFGUN6c6i4bG3kFXBAtL
- *Conversation with Copilot on error metrics interpretation:* https://copilot.microsoft.com/shares/aoeWxvmpkp5qZwdNu71Ve
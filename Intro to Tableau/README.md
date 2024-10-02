# Workshop Overview

## Objective
Introduce students to data visualization using Tableau and guide them in creating an interactive dashboard on Netflix data (popular TV shows/movies).

## Dataset
[Netflix Shows Dataset](https://www.kaggle.com/datasets/shivamb/netflix-shows)

## End Product
An interactive dashboard showcasing Netflix content by release year, genre, and ratings.

---

# Key Learning Outcomes
- Understanding the basics of Tableau and its interface.
- Learning how to import and explore datasets.
- Creating simple visualizations: bar chart, line chart, and pie chart.
- Building an interactive dashboard with multiple visualizations.
- Basic filtering and interactivity within dashboards.

# Preparation for the Workshop
- Download the Netflix dataset from Kaggle ([link](https://www.kaggle.com/datasets/shivamb/netflix-shows)).
- Ensure Tableau Public is installed on your laptop.
- Prepare a sample dashboard to showcase before starting the workshop as an example.

---

# Workshop Instructions

### Step 1: Introduction to Tableau (5 minutes)
**Objective**: Briefly learn about Tableau and its applications for data visualization.
![image](https://github.com/user-attachments/assets/ef35137c-afd0-4c38-ada2-94deccf68fc3)
- What is Tableau? Explain how it allows users to connect, visualize, and share data insights quickly.
- Show how to download and install Tableau Public if attendees haven't done so already.

### Step 2: Load the Dataset (5 minutes)
**Objective**: Learn how to import a dataset into Tableau.
- Open Tableau.
- Click on “More” under the "To a File" section (CSV file).
![image](https://github.com/user-attachments/assets/000b8a57-9d45-4dfc-9a3b-37a36115ebc3)
- Once the dataset is loaded, show the preview of the data in Tableau’s Data Source tab.

### Step 3: Data Exploration and Preparation (5 minutes)
**Objective**: Learn to explore and clean data.
- In the Data Source tab, explain the various columns (Title, Director, Genre, Release Year, Rating, etc.).
![image](https://github.com/user-attachments/assets/c3dd0e40-06b4-4df8-9f0b-88ed35277dd2)
- Discuss how Tableau auto-detects data types (numeric, string, date).
- Check for any missing data and explain how to filter or clean it within Tableau if needed.
- Filter the dataset to focus only on the most relevant information (split any data that could be useful/interesting).

### Step 4: Creating Basic Visualizations (15 minutes)
**Objective**: Learn and pracitce creating basic visualizations.

#### Bar Chart of Content by Genre
1. Go to the Sheet 1 tab.
2. Drag Genre to the Columns shelf and Title to the Rows shelf.
3. Change the Title field to COUNT (Title) to display the number of titles per genre.
4. Add color by dragging Rating to the Color shelf.
![image](https://github.com/user-attachments/assets/29d5a199-e00d-4102-a20c-c334dff084c5)

#### Line Chart of Content Released per Year
1. Create a new sheet (click the sheet icon).
2. Drag Release Year to the Columns shelf and Title to the Rows shelf.
3. Aggregate Title as COUNT to see the number of shows/movies released per year.
4. Change the chart type to Line.
![image](https://github.com/user-attachments/assets/b5175a27-5b8e-48c1-9cd2-44d2ac3d75d8)

#### Pie Chart for Content by Rating
1. Create another new sheet.
2. Drag Rating to the Columns shelf and Title to the Rows shelf (aggregate by COUNT).
3. Change the chart type to Pie.
![image](https://github.com/user-attachments/assets/34aa839a-d64f-42da-bd51-2c7706bff48c)

### Step 5: Building an Interactive Dashboard (10 minutes)
**Objective**: Combine visualizations into a single interactive dashboard.
1. Click on the New Dashboard icon at the bottom of the screen.
2. Drag each of the created sheets onto the dashboard.
3. Arrange them in a grid or stacked format, adjusting the sizes as needed.
![image](https://github.com/user-attachments/assets/0021ebf1-85a9-404f-8ccb-d584e6f3da8f)

### Try it Yourself
Contruct the following graphic showing "Content by Country"
![image](https://github.com/user-attachments/assets/a5781412-9ec2-4198-8ff7-7c1c752e5c25)


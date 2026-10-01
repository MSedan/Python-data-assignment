# Data Management System

## Overview

The Data Management System is a Python desktop application developed using Tkinter. It allows users to load, clean, transform and analyse educational activity data through a graphical user interface.

The application combines data from multiple sources, removes unnecessary records, creates interaction counts, generates pivot tables and produces correlation heatmaps to identify relationships between learning components.

## Features

### Load Dataset
The application loads three CSV files:

- ACTIVITY_LOG.csv
- COMPONENT_CODES.csv
- USER_LOG.csv

The system validates whether the data has already been loaded and provides feedback messages to the user.

### Data Cleaning and Transformation

The cleaning process performs the following tasks:

- Renames `User Full Name *Anonymized` to `USER_ID`
- Merges activity, user and component datasets
- Combines separate Date and Time columns into a single `DateTime` column
- Removes records containing the components:
  - System
  - Folder
- Creates a cleaned dataset
- Exports the cleaned data to `Dataset.json`

### Interaction Counts

The application calculates the number of interactions each user has with a component during a given month.

A new `Count` column is created and stored within the dataset.

### Pivot Table Creation

The application reshapes the data using a pivot table structure, allowing user interactions to be summarised by component and making the dataset suitable for further analysis.

### Correlation Analysis

The system generates a correlation matrix using interaction counts from selected learning components:

- Assignment
- Quiz
- Lecture
- Book
- Project
- Course

Results are displayed as a heatmap using Seaborn and Matplotlib to help identify relationships between components.

### User Interface

The application provides:

- Dataset loading controls
- Data cleaning functionality
- Data transformation tools
- Correlation visualisation
- User feedback and validation messages
- Error handling for missing files and invalid operations

## Technologies Used

- Python 3
- Tkinter
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Application Workflow

1. Load the source CSV files.
2. Clean and merge the datasets.
3. Generate a cleaned JSON dataset.
4. Calculate interaction counts.
5. Create a pivot table structure.
6. Generate a correlation heatmap for selected components.

## File Structure

```text
Project Folder
│
├── main.py
├── ACTIVITY_LOG.csv
├── COMPONENT_CODES.csv
├── USER_LOG.csv
├── Dataset.json
└── README.md
```

## Installation

Install the required Python packages:

```bash
pip install pandas numpy matplotlib seaborn
```

## Running the Application

Run the application using:

```bash
python main.py
```

## Skills Demonstrated

This project demonstrates:

- Data cleaning
- Data transformation
- Data integration
- Data aggregation
- Pivot table generation
- Correlation analysis
- Data visualisation
- JSON data export
- GUI development using Tkinter
- Error handling and user validation

## Future Improvements

- Add descriptive statistics (mean, median and mode)
- Allow exporting pivot tables to CSV files
- Add additional visualisations
- Implement filtering and search functionality
- Improve data validation and error reporting


This application was developed as a university project to demonstrate practical data processing, visualisation and software development skills using Python.

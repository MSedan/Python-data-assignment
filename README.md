# Data Management System

## Overview

This application was developed as part of a university project and provides a graphical user interface (GUI) for loading, cleaning, transforming, and analysing educational activity data.

The application allows users to load raw data, clean and combine datasets, calculate user interaction counts, create pivot tables, and generate correlation heatmaps to identify relationships between different learning components.

## Features

### Load Data
- Loads data from:
  - `ACTIVITY_LOG.csv`
  - `COMPONENT_CODES.csv`
  - `USER_LOG.csv`
- Validates that data is not loaded multiple times.
- Displays feedback messages to the user.

### Data Cleaning
- Renames anonymised user identifiers to `USER_ID`.
- Merges activity, component, and user datasets.
- Combines date and time into a single `DateTime` column.
- Removes unnecessary components such as `System` and `Folder`.
- Saves the cleaned dataset as `Dataset.json`.

### Interaction Counting
- Calculates the number of user interactions with each component per month.
- Creates a new `Count` column.
- Updates and saves the dataset.

### Pivot Tables
- Reshapes the data into a pivot table format.
- Summarises user activity across different learning components.

### Correlation Analysis
- Creates a correlation matrix using interaction counts.
- Displays results as a heatmap using Seaborn and Matplotlib.
- Helps identify relationships between different components.

### Graphical User Interface
- Built using Tkinter.
- Provides a simple and user-friendly interface.
- Includes error handling and user feedback messages.

## Technologies Used

- Python
- Tkinter
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Installation

Install the required libraries before running the application:

```bash
pip install pandas numpy matplotlib seaborn

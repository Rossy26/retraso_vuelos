# Flight Delay Analysis and Prediction

## Overview
The main objective of this project is to explore and analyze flight data to uncover the primary factors that contribute to flight delays. Based on these insights, we aim to build and train a Machine Learning model capable of predicting the estimated delay time for future flights.

## Repository Structure

The project is structured as follows:

- **`notebook.ipynb`**: The core Jupyter Notebook of the project. It includes:
  - **Data Import & Cleaning**: Loading the raw flight data and preparing it for analysis.
  - **Exploratory Data Analysis (EDA)**: Visualizing the impact of different variables (such as airline, aircraft type, whether the flight is Schengen or non-Schengen, holidays, etc.) on flight delays.
  - **Machine Learning Modeling**: Training and evaluating predictive models to estimate delay times.
- **`flights.csv`**: The dataset used for the analysis. It contains around 71,000 records of flights with features like airline, airplane type, origin, departure/arrival times, and the target variable (`delay`).
- **`champion.pkl`**: The serialized (pickled) version of the best-performing Machine Learning model derived from our experiments, ready for deployment or future inference without retraining.
- **`requirements.txt`**: A list of all the Python libraries and dependencies required to successfully run the notebook.

## Dataset Features

A quick look at the main features included in `flights.csv`:
- `flight_id`: Unique identifier for each flight.
- `airline`: The operating airline.
- `aircraft_type`: The model of the aircraft.
- `schengen`: Indicates whether the flight is within the Schengen area or not.
- `origin`: Origin airport code.
- `arrival_time` & `departure_time`: Scheduled times.
- `day`, `year`: Date features.
- `is_holiday`: Boolean feature indicating if the flight is during a holiday.
- `delay`: The target variable to be predicted (in minutes).

## Requirements

To run this project on your local machine, you need Python installed, along with the following libraries:

- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `yellowbrick`

## How to Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```

2. **Create a virtual environment (Optional but Recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. **Install the dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
5. **Open `notebook.ipynb`** and run the cells to reproduce the analysis and model training!

## Model 
The most successful model during our iteration process has been saved as `champion.pkl`. You can load this file using `joblib` or `pickle` in Python to make instant predictions on new, unseen flight data.


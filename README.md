# Job Analytics API

## Overview
This is a Flask-based API for job analytics, allowing users to retrieve job statistics and insights from a MongoDB database. It provides endpoints to query job counts by various parameters such as year, month, and country, as well as to obtain the most frequent skills associated with a particular job track.

## Features
- Retrieve job counts by year, month, and country.
- Get the most frequent skills associated with a specific job track.

## Setup
1. Clone this repository to your local machine.
2. Install the required dependencies using `pip install -r requirements.txt`.
3. Ensure MongoDB is installed and running on your system.
4. Set up the MongoDB connection URI in the `app.py` file.
5. Run the Flask application by executing `python app.py`.

## Usage
### Endpoint 1: Get Job Counts
- **URL:** `/Jobs`
- **Method:** `GET`
- **Parameters:**
  - `year`: Year filter (optional)
  - `month`: Month filter (optional)
  - `country`: Country filter (optional)
- **Response:** JSON object containing job counts based on the provided filters.

### Endpoint 2: Get Most Frequent Skills
- **URL:** `/Jobs/Skill/<track_name>`
- **Method:** `GET`
- **Parameters:**
  - `track_name`: Job track name
- **Response:** JSON object containing the most frequent skills associated with the specified job track.

## Example
To retrieve job counts for the year 2023 in the United States, you can make a GET request to `/Jobs?year=2023&country=Egypt`

## Notion Example
For an example of how this API can be used in conjunction with a dashboard, check out this [Notion Dashboard](https://www.notion.so/DashBoard-Notes-04c06059c7994616bf777d23949f0e57?pvs=4)
# Weather Data Project

## Overview
Automated ETL that extracts Casablanca's daily weather forecast  + observed data from an open source project _(wttr.in)_ and loads it into a live report. This ETL automatically runs at 6:00am EST and extracts the weather data for Casablanca for the following day.

## Features
* **Weather Data Retrieval:** The script extracts weather data from wttr.in and saves it with a corresponding timestamp
* **Data Logging:** Captures both the raw data and any errors encountered during execution from 'launchd' on macOS and 'crontab' on Linux
* **Scheduled Execution:** Uses launchd to run the script at a specified time each day for macOS and crontab for Linux


* **open source project used + credited:** [Github Repo](https://github.com/chubin/wttr.in#readme) <br>
* **example weather report:**

     <img width="508" alt="Screenshot 2024-07-26 at 2 35 54 PM" src="https://github.com/user-attachments/assets/68f4bd95-fa5c-464d-9c8f-4e04a732be55">

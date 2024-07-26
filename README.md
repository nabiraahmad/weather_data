# Weather Data Project

## Overview
Automated ETL that extracts Casablanca's daily weather forecast  + observed data from an open source project _(wttr.in)_ and loads it into a live report. This ETL automatically runs at 6:00am EST and extracts the weather data for Casablanca for the following day.

## Features
* **Weather Data Retrieval:** The script extracts weather data from wttr.in and saves it with a corresponding timestamp
* **Data Logging:** Captures both the raw data and any errors encountered during execution from 'launchd' on macOS and 'crontab' on Linux
* **Scheduled Execution:** Uses launchd to run the script at a specified time each day for macOS and crontab for Linux


## Setup

**1. Clone the repository** <br><br>
**2. _For macOS:_ Ensure the plist file is under /Library/LaunchAgents** <br><br>
**3. Set the correct permissions**
<br>
          `chmod 755 /usr/local/bin/weather_data_proj/rx_poc.sh`
<br><br>
**4. _For macOS:_ Edit the 'launchd' plist file to ensure the file path and schedule is correctly set**
<br><br>
**5. Launch the plist file** <br>
          `launchctl load ~/Library/LaunchAgents/com.your-name.weather_data_proj.plist`
          <br><br>
**6. For Linux systems, create a schedule using the steps below**<br> <br>
-    In your terminal, enter the crontab editor using `crontab-e` <br>
-    Add this line to the end of the crontab file to schedule the script to run at a specific time. The following code is to run it at 6:00am everyday. Make sure the filepath is correct to the script rx_poc.sh <br>
    -    `0 6 * * * /usr/local/bin/weather_data_proj/rx_poc.sh` <br><br>
     **Note:** the crontab uses syntax minute/hour/day of month/month/day of week <br>
-   Save and exit <br>
-   Use `crontab -l` to verify the cron job has been added <br><br>
          


**Open source project used + credited:** [Github Repo](https://github.com/chubin/wttr.in#readme) <br><br>
**Example weather report:**

  <img width="508" alt="Screenshot 2024-07-26 at 2 35 54 PM" src="https://github.com/user-attachments/assets/68f4bd95-fa5c-464d-9c8f-4e04a732be55">



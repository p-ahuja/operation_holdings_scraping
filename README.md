# operation_holdings_scraping

## Main file: loop.py 

### Purpose: scrapes data from https://agcensus.dacnet.nic.in/tehsilsummarytype.aspx with the following details: 

State: all states
District: all districts
Tehsil: all tehsils
Tables: Number and area of operation holdings by size groups
Social group: all social groups 
Gender:  Total
Table Unit: Number

### High level explanation: Loops through all states, districts, tehsils and submits the form on the website; fetches the resulting table as a csv file and downloads it to dropbox 

## Secondary file: interface_trackers.py 

### Purpose: includes three helper functions 

## Other files are either (1) unspecific to the website or (2) not imported in the main file, loop.py, so unused

## Requirements: refer to requirements.txt for necessary python libraries/installments; refer to the import statements in loop.py to understand while files are unused 

## Before you run: 
1. Create a directory called log_files and, inside it, a file called log_number.txt where the first line says 1; each time the code runs, a new log file will be created in log_files and the number in log_number.txt will be incremented
2. Create a directory called saved_tables; each time a file is downloaded from the website, a csv file with the information from the table will be created in saved_tables; you do not have to populate saved_tables with anything before running the code
3. Create a directory called state_trackers; each time an attempt is unsuccessful, it will be document in a file called <STATE>_unsucsessful.txt in state_trackers; you do not have to populate state_trackers with anything before running the code
4. No need to change the directory called trackers
5. Create a file called last_done.txt and input the first configuration in the form
YEAR
STATE
DISTRICT
TEHSIL; 
This file updates each iteration with the details of the most recently scraped table; if the code terminates unexpectedly, it will re-run and start from the year, state, district and tehsil listed in last_done.txt 

## To run: python3 loop.py 

## Dropbox folders for this data: 

### 2000: https://www.dropbox.com/scl/fo/9aae4gx1888ou1ywk8ybr/h?rlkey=y8rxzeb0vwxnkauv9vir6xhzx&dl=0

### 2005: https://www.dropbox.com/scl/fo/sx7jkoiovuxbhlga9psdf/h?rlkey=7s80i64u13g25027yscxqdy6h&dl=0

### 2010: https://www.dropbox.com/scl/fo/5ktaj5d82ei003f9a8x5d/h?rlkey=ywgg2cx94e3dn5rud6q7r8h5h&dl=0

### 2015: https://www.dropbox.com/scl/fo/wfa8rvj7crh4o7py146qf/h?rlkey=xswz490a2ot5b0h4b20cizq19&dl=0

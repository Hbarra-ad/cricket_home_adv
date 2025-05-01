# How Have Countries Fared at Home in Test Match Cricket and What Grounds Perform Best?

## Project Overview

This project explores home advantage in Test match cricket by examining historical match outcomes across countries and grounds. Using data scraped from HowSTAT, I analyze how countries have performed at home over the decades and identify which Test grounds deliver the strongest home team records.

The project culminates in a blog post discussing the analysis, visualizations, and conclusions, written for a general audience using HackMD.

## My Process

1. I began by scraping the India Test match data from HowSTAT, but encountered a challenge: **Table 5**, which contains all match results, is rendered via JavaScript and didn’t load with standard HTML scraping.
2. To access the table, I implemented **Selenium** to automate browser interaction and successfully scrape the uncleaned data.
3. I then adapted the code to work for **each individual Test-playing country**, modifying the URLs and identifiers as needed.
4. I considered making a loop for each country code but as I am only scraping 5 urls, it was easier to copy and paste the code.
5. Once the data was collected, I cleaned it to retain only the key columns: `Year`, `Ground`, `Home Team`, and `Winner`. Something to note is that New Zealand and South Africa are referenced as New and South in the Home Team and Winner columns as I cleaned the data to include only the first word from the original series column
6. I also considered making a loop for the cleaning process, however struggled to match the home teams across the files. The attempt can be seen in my notebook folder.
7. I generated **basic summary statistics** for each countrys' home win rate and visualized the results using a **bar chart**.
8. For ground-level analysis, I created **violin plots** by encoding match outcomes as `1` (home win) or `0` (loss).
9. To track performance over time, I grouped matches by **decade** and plotted home win percentages by country on a single line graph.
10. I presented my findings and insights in a blog post written in HackMD.

## Project Structure

cricket_home_adv/ | data/ Raw and cleaned CSV files | output/ Visualizations and results | Notebooks/ Juptyer Notebook files containing all my code | README.md This file | packages.txt Python dependencies | blog.txt Containing the git hub public repository and the HackMD link.
# Simplifying the Job Search  

Sifting through countless job postings is a challenge, especially when you’re trying to find roles that match your skills and experience. That’s what inspired me to create the **Indeed Scraper** – a Python-based tool designed to automate job searches and save time.  

In this blog post, I’ll walk you through the project, its features, and how it tackles the frustrations of modern job hunting.  

## Why I Built the Indeed Scraper  

Manually searching for jobs often involves wading through listings that aren’t relevant or don’t meet key criteria. I wanted a solution to streamline this process, filter out irrelevant postings, and provide clean, actionable data that I could analyze further.  

The **Indeed Scraper** is that solution. It’s a lightweight tool that simplifies job hunting by automatically gathering job data from Indeed and presenting it in a structured format.  

## How It Works  

The tool is split into two main components:  

### `scraper.py`  

This script interacts directly with Indeed’s job search pages. It sends requests, parses the HTML content, and extracts useful information such as:  
- Job Title  
- Company Name  
- Location  
- Job Description  

All of this data is stored in JSON format for further analysis.  

### `app.py`  

While `scraper.py` focuses on gathering data, `app.py` brings everything together. It provides an easy-to-use interface for setting up your searches, managing parameters, and executing the scraping process. Whether you’re searching for specific keywords, targeting a particular location, or running multiple searches back-to-back, `app.py` acts as the central hub.  

## Handling Inconsistent Results  

One challenge I encountered was the variability in results. Running the same query multiple times would yield vastly different results – sometimes 900 postings, other times only 200. This inconsistency could stem from changes in job availability or fluctuations in Indeed’s data delivery.  

To address this, I created an additional script that combines results from multiple runs and removes duplicates. This way, you can perform several scrapes and merge the data into a single, clean dataset. This script ensures you capture as much information as possible without redundancy.  

## Features of the Indeed Scraper  

1. **Automated Searches**: Input your search parameters and let the tool handle the rest.  
2. **Handles Pagination**: Ensures all result pages are scraped for comprehensive data collection.  
3. **Data Merging**: Combines results from multiple runs and removes duplicates, giving you a consistent dataset to work with.  

## What’s Next?  

The Indeed Scraper has already saved me countless hours of job searching, and I hope it can do the same for others. Future plans include supporting other job boards like LinkedIn or Glassdoor.  

## Conclusion  

The **Indeed Scraper** is my way of turning a frustrating manual process into an automated solution. With its ability to handle searches, inconsistencies, and data merging, it’s a powerful tool for anyone looking to simplify their job hunt.  

If you’re curious about the tool or want to try it yourself, check out the project on GitHub: [https://github.com/n0hats/indeed_scraper](https://github.com/n0hats/indeed_scraper).  

Feel free to share your feedback or ideas for improvement – I’d love to hear them!  

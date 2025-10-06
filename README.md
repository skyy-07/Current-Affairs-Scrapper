# Advanced Current Affairs Web Scraper

A powerful, comprehensive web scraper optimized for Google Colab, designed to aggregate, filter, categorize, and analyze current affairs articles from a wide range of global, regional, and national sources.

## Features

- Scrapes news from over 25+ reputable sources including BBC, CNN, Reuters, Times of India, NDTV, The Hindu, Al Jazeera, and more.
- Filters relevant current affairs content using a keyword-based relevance matching system.
- Categorizes articles into Politics, Economy, International, Social, Legal, Environment, and General topics.
- Eliminates duplicate articles through similarity checks.
- Supports asynchronous and multi-threaded scraping for efficiency.
- Extracts full article content using the Newspaper3k library.
- Outputs data in multiple formats: Text, JSON, and CSV.
- Filters articles within a user-defined time frame (last 7, 14, or customizable days).
- Provides source-wise statistics and comprehensive summaries.

## Installation

Install the required libraries (for local machines or Google Colab):

For Selenium support on Google Colab:

!apt update
!apt install chromium-chromedriver

text

## Usage

### Basic Example

from scraper import scrape_comprehensive_current_affairs

Scrape current affairs from the last 7 days with a maximum of 15 articles per source
summary = scrape_comprehensive_current_affairs(daysback=7, maxarticlespersource=15)
print(summary)

## Supported News Sources

- **Global English**: BBC, CNN, Reuters, Guardian, Al Jazeera, Associated Press, NPR
- **Indian English**: Times of India, The Hindu, Indian Express, NDTV, Firstpost
- **US**: NY Times, Washington Post, Politico
- **Regional**: France24, DW

## Current Affairs Keywords for Filtering

Keywords include but are not limited to: politics, government, election, policy, economy, GDP, inflation, diplomacy, war, conflict, crisis, law, justice, environment, climate, energy.

## How It Works

- The core `CurrentAffairsScraper` class manages:
  - Configuring sources
  - Scraping RSS feeds asynchronously
  - Parsing full articles
  - Filtering based on relevance keywords
  - Categorizing articles
  - Deduplicating articles
  - Generating summaries and statistics
  - Saving results in various formats

## License

This project is open-source under the MIT License.

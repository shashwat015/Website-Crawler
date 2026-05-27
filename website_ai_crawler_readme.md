# AI Website Crawler & PDF Report Generator

## Overview

This project is a website crawler that:

- Crawls webpages from a given website
- Extracts important page content
- Generates AI summaries using a local LLM
- Creates a professional PDF report automatically

The system uses:

- Selenium for dynamic website crawling
- BeautifulSoup for HTML parsing
- Ollama + Llama 3 for AI analysis
- ReportLab for PDF generation

The project runs completely on your local machine.

---

# Features

## Website Crawling

- Crawls multiple pages automatically
- Handles dynamic JavaScript websites
- Extracts:
  - Titles
  - Main content
  - Internal links

## AI-Powered Analysis

Each webpage is analyzed using AI to generate:

1. Main Purpose
2. Important Information
3. Products/Services Mentioned
4. Technologies Mentioned
5. Business Value
6. Final Summary

## PDF Report Generation

Automatically creates a professional PDF report containing:

- Crawled page URLs
- Extracted content
- AI summaries
- Structured analysis

---

# Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Selenium | Dynamic web crawling |
| BeautifulSoup | HTML parsing |
| Requests | API communication |
| Ollama | Running local LLMs |
| Llama 3 | AI content analysis |
| ReportLab | PDF generation |
| webdriver-manager | ChromeDriver management |

---

# Project Structure

```bash
project/
│
├── crawler.py
├── complete_website_report.pdf
├── requirements.txt
└── README.md
```

---

# Installation

## 1. Clone the Repository

```bash
git clone <your-repo-url>
cd <project-folder>
```

---

## 2. Install Python Dependencies

```bash
pip install selenium
pip install beautifulsoup4
pip install requests
pip install reportlab
pip install webdriver-manager
```

Or using requirements.txt:

```bash
pip install -r requirements.txt
```

---

# Install Ollama

Download and install Ollama:

urlOllama Official Websitehttps://ollama.com

After installation:

```bash
ollama run llama3
```

This downloads and starts the Llama 3 model locally.

---

# Chrome Requirements

Make sure Google Chrome is installed.

The project automatically downloads the required ChromeDriver using:

```python
webdriver_manager
```

---

# How It Works

## Step 1 — Open Website

Selenium launches a headless Chrome browser.

## Step 2 — Crawl Pages

The crawler:

- Visits internal links
- Avoids duplicate pages
- Limits crawl size using:

```python
MAX_PAGES = 50
```

## Step 3 — Extract Content

BeautifulSoup extracts webpage text and important information.

## Step 4 — Generate AI Summary

The extracted content is sent to:

```bash
http://localhost:11434/api/generate
```

using the Llama 3 model running through Ollama.

## Step 5 — Generate PDF

A structured PDF report is created using ReportLab.

---

# Running the Project

## Start Ollama First

```bash
ollama run llama3
```

---

## Run the Python Script

```bash
python crawler.py
```

---

# Output

The project generates:

```bash
complete_website_report.pdf
```

The PDF includes:

- Website analysis
- AI summaries
- Extracted content
- Business insights

---

# Example Use Cases

## Business Website Analysis

Analyze company websites for:

- Services
- Business model
- Technologies used

## Competitor Research

Generate AI reports for competitor websites.

## SEO Research

Understand website structure and content.

## AI Data Collection

Create datasets from website content.

## Automated Documentation

Generate structured reports automatically.

---

# Limitations

- Some websites block automated crawlers
- Very large websites may take time
- AI summaries depend on the LLM quality
- JavaScript-heavy sites may require longer load times

---

# Future Improvements

Possible upgrades:

- Better AI prompts
- Multi-threaded crawling
- Website screenshot support
- Charts & analytics in PDF
- Export to DOCX/HTML
- Vector database integration
- RAG-based website chatbot
- Semantic search
- Technology stack detection
- SEO scoring
- Sentiment analysis

---

# Troubleshooting

## ChromeDriver Errors

Update Chrome browser to the latest version.

---

## Ollama Connection Error

Make sure Ollama is running:

```bash
ollama run llama3
```

---

## Selenium Timeout

Increase page wait times:

```python
time.sleep(5)
```

---

# Requirements.txt Example

```txt
selenium
beautifulsoup4
requests
reportlab
webdriver-manager
```

---

# Author

Created as an AI-powered website crawling and analysis project using Python, Selenium, Ollama, and Llama 3.

---

# License

This project is open-source and can be modified for educational and research purposes.


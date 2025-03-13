# Amazon Price Tracker with Django, Selenium & Celery

## Overview
This project demonstrates how to use Django, Celery, and Selenium with Bright Data to scrape Amazon product price fluctuations. The goal is to automate web scraping while handling captchas and login restrictions, efficiently store the data using Django models, and schedule tasks using Celery.

## Features
- **Django & Celery Integration**: Background and scheduled task processing for scraping automation.
- **Selenium with Bright Data Proxies**: Overcome Amazon captchas and access data efficiently.
- **Jupyter Notebook for Testing**: Live browser automation using Selenium in Jupyter.
- **BeautifulSoup4 for Data Parsing**: Extract and process product pricing information.
- **Django Models for Data Storage**: Store scraped data in an organized structure.
- **Celery Task Management**: Offload scraping tasks for better application performance.
- **Django Admin Integration**: Schedule and monitor scraping tasks within Django Admin.

## Installation
### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- Django 3.2+
- Celery
- Selenium
- BeautifulSoup4
- Redis (for Celery backend)
- Bright Data account

### Setup
1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-repository-url.git
   cd your-project-folder
   ```
2. **Create a virtual environment and activate it:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
4. **Setup Django project:**
   ```bash
   python manage.py migrate
   python manage.py createsuperuser  # Create an admin user
   ```
5. **Run Redis for Celery:**
   ```bash
   redis-server
   ```
6. **Start Celery worker:**
   ```bash
   celery -A your_project_name worker --loglevel=info
   ```
7. **Run Django server:**
   ```bash
   python manage.py runserver
   ```

## Usage
1. **Access Django Admin:** `http://127.0.0.1:8000/admin/`
2. **Schedule scraping tasks in Django Admin** using Celery.
3. **Monitor and retrieve scraped data** in Django models.

## Recommended Resources
- [Try Django 3.2](https://www.youtube.com/playlist?list=PLlrATfBNZ98fB7i7wX9uB4fA5XyJ6E7W2)
- [30 Days of Python](https://www.youtube.com/playlist?list=PLlrATfBNZ98_NWwATcK3XfMoZl1A60wxD)
- [Django Official Docs](https://djangoproject.com)
- [Bright Data](https://brdta.com/justin)

## Next Steps
- Expand functionality by integrating AI for smarter scraping.
- Implement more robust logging and error handling.
- Deploy the scraper using Docker and cloud services.

---
🚀 **Explore More**: Check out our free Udemy course on [Web Scraping with Python + AI](https://www.udemy.com/course/smarter-web-scraping/)!


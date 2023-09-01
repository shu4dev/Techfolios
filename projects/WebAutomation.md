---
layout: project
type: project
image: img/seleniumlogo.png
title: "Website Automation"
date: 2022
published: false
labels:
  - Python
  - Selenium
  - WebDriver
summary: "An automation script for particular website"
---
# Introduction
I created this Python script for my dad to help him reserve a badminton court. At the gym he frequents, court reservations must be made online through their website. The reservation for next week becomes available at midnight. My dad had difficulty operating the computer quickly enough to secure a court, so this script is designed to assist him.

This script is written in Python and utilizes a library called Selenium, which can detect elements in HTML and interact with them.
<hr>

```python
from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.chrome.options import Options
from twocaptcha import TwoCaptcha
import time
import os 
import calendar
from datetime import datetime

options = Options()
service = Service( executable_path="your_path")
options.add_experimental_option("detach", True)
driver = webdriver.Chrome( 
service = service,
options = options)
```
Source: <a href="https://github.com/jogarces/ics-313-text-game"><i class="large github icon "></i>jogarces/ics-313-text-game</a>

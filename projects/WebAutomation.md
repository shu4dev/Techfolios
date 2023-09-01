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

To ensure this script runs at the time we want I write another getTime() function

```python
def getTime():
    now        = datetime.now()
    year       = int(now.strftime("%Y"))
    month      = int(now.strftime("%m"))
    TodayDay   = now.strftime("%d")
    day        = int(now.strftime("%d"))
    monthrange = calendar.monthrange(year, month)
    if day + 8 > monthrange[1]:
        month = str(month + 1).zfill(2)
        day   = str(day + 8 - monthrange[1]).zfill(2)
    elif day + 8 > monthrange[1] and month == 12:
        year  = str(year + 1) 
        month = str(1).zfill(2)
        day   = str(day + 8 - monthrange[1]).zfill(2)
    else:
        year  = str(year).zfill(4)
        month = str(month).zfill(2)
        day   = str(day + 8).zfill(2)
    print("Today is ", year, "/", month,"/", TodayDay, 
          "\nIntend to reserve for ", year, "/", month,"/", day)
    return str(year), str(month), str(day)
```
Source: <a href="https://github.com/jogarces/ics-313-text-game"><i class="large github icon "></i>jogarces/ics-313-text-game</a>

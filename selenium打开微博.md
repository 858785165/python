```python
from selenium import webdriver
from selenium.webdriver.chrome.options import Options
import time

opt = Options()
opt.add_argument('--disable-blink-features=AutomationControlled')
opt.add_experimental_option('excludeSwitches', ['enable-automation'])
web = webdriver.Chrome(options=opt)
web.get('https://weibo.com')
time.sleep(4)
print(web.title)
```
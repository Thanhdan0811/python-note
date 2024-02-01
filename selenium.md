# install 
py -3.12 -m pip install -U selenium
download chromedriver and placein : C:\Program Files\chromedriver

# EX 1

```
from selenium import webdriver
from selenium.webdriver.common.by import By
PATH = r"C:\Program Files\chromedriver\chromedriver.exe"
driver = webdriver.Chrome()
driver.get("https://www.like4like.org/login/")
username = driver.find_element(By.ID, 'username')
username.send_keys("Hello")
###
passw = driver.find_element(By.TAG_NAME, 'label') and driver.find_element(By.CLASS_NAME, 'bold') and driver.find_element(By.ID, 'password_text')
print(passw.text)
```

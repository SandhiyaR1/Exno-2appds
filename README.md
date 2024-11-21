# EX-02 PERFORMING DATA COLLECTION THROUGH WEB SCRAPING
**AIM:**

To Perform Data Collection through web scraping using python.

**ALGORITHM:**

Step 1: Include the Necessary python libraries.<br>
Step 2: Use the requests library to send HTTP requests to a web page.<br>
Step 3: Retrieve the HTML content and use BeautifulSoup to parse it.<br>
Step 4: Navigate and extract the necessary data.<br>
Step 5: Handle the Java script content and retrieve the data using the html tags.<br>
Step 6: Check with the website permission and scrap the content.<br>

**CODING:**
``` python
import requests
from bs4 import BeautifulSoup
import pandas as pd
url = 'https://www.w3schools.com/html/html_table_sizes.asp'
response = requests.get(url)
response
soup = BeautifulSoup(response.content, 'html.parser')
headings = soup.find_all('h2')
headlist=[x.text for x in headings]
print(headlist)
df=pd.DataFrame(headlist,columns=['Headings'])
df.to_csv('newdata.csv', index=False)
df
```
**OUTPUT**

![image](https://github.com/user-attachments/assets/2b591c2c-3cef-4bfd-ab4e-298530a04c64) 

![image](https://github.com/user-attachments/assets/4f6ae323-1d52-4d6b-994c-6a2b620d9888).


**RESULT:**
 
Thus , data Collection through web scraping using python is successfully performed.


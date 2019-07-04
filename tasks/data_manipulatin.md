# Data Fetching And Processing (Individual Work)

Amoung many potential options on how to get data for ML we can put to a special place data scrapping and fetching over the API

### Data Scrapping
* Read about [scrapy](https://scrapy.org/) 
* Read about [headless browsers](https://github.com/dhamaniasad/HeadlessBrowsers) in general and [selenium](https://www.seleniumhq.org/) in particular

Try to understand and run the code (you will also need to download a [webdriver](https://www.seleniumhq.org/projects/webdriver/) - learn more about this please):
```python
import sys
import json
import time

from selenium import webdriver


def listener(user_url, user_name):
    user_url = "https://www.messenger.com/t/" + user_url

    with open('secret') as f:
        secret = json.loads(f.read())

    options = webdriver.ChromeOptions()
    options.add_argument('headless')
    driver = webdriver.Chrome('chromedriver', chrome_options=options)
    # driver = webdriver.Chrome()

    driver.set_window_size(1024, 768)
    driver.get("https://www.messenger.com/")

    email = driver.find_element_by_name("email")
    email.clear()
    email.send_keys(secret["email"])

    password = driver.find_element_by_name("pass")
    password.clear()
    password.send_keys(secret["password"])

    driver.find_element_by_name("login").click()

    driver.get(user_url)
    driver.find_element_by_class_name("_1mf").click()

    while True:
        user_messages = []
        messages = driver.find_elements_by_class_name("_41ud")
        for message in messages:
            user = message.find_element_by_tag_name('h5').get_attribute('aria-label')
            for data in message.find_elements_by_class_name("_aok"):
                time.sleep(2)
                if user == user_name:
                    user_messages.append(data.text)

        # print(json.dumps(result, sort_keys=False, indent=4, ensure_ascii=False, separators=(',', ': ')))

        try:
            if set(user_messages) != set(result['user_messages']):
                output = {'new_messages': [y for y in user_messages if y not in result['user_messages']]}
                # output = list(set(recent_messages) - set(result[user_check]))
                print(json.dumps(output, sort_keys=False, indent=4, ensure_ascii=False, separators=(',', ': ')))
        except UnboundLocalError:
            pass

        time.sleep(2)

        result = {'user_url': user_url, 'user': user_name, 'user_messages': user_messages}

    driver.close()


if __name__ == "__main__":
    param1 = str(sys.argv[1])
    param2 = str(sys.argv[2])
    listener(param1, param2)
```


### Fetch Data From Public Resources Using API
For learning about practical aspects of this, you will go through the process of consuming Twitter API


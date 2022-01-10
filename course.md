from selenium import webdriver

try:
    link = "http://suninjuly.github.io/get_attribute.html"
    browser = webdriver.Chrome()
    browser.get(link)
    import math
    def calc(x):
        return str(math.log(abs(12 * math.sin(int(x)))))
    new1 = browser.find_element_by_id("treasure")
    x_element = new1.get_attribute("valuex")
    x = x_element
    y = calc(x)
    input1 = browser.find_element_by_id("answer")
    input1.send_keys(y)
    option1 = browser.find_element_by_id("robotCheckbox").click()
    option2 = browser.find_element_by_id("robotsRule").click()
    option2 = browser.find_element_by_xpath("/html/body/div/form/div/div/button").click()
    
    
  
    

    


finally:
    # успеваем скопировать код за 30 секунд
    time.sleep(30)
    # закрываем браузер после всех манипуляций
    browser.quit()
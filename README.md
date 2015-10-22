#sel_python_test
from selenium import webdriver
#create a new Firefox session
driver = webdriver.Firefox()
driver.implicitly_wait(30)
driver.maximize_window()
#TASK_1 - navigate to the application home page
driver.get("http://demo.opencart.com/")
#TASK_2 - change currency
listCurrency = driver.find_element_by_xpath("//form[@id='currency']").click()
currency = driver.find_element_by_name("GBP").click()
#TASK_3 - search for iPods (partial success)
search_field = driver.find_element_by_name("search")
search_field.clear()
search_field.send_keys("ipod")
#search_field.submit()
#click on search button
#click_button = driver.find_element_by_class("btn btn-default btn-lg")
#NoSuchElementException: Message: u"Element was not in a form so couldn't submit"
#click_button.click()
#click_button = driver.find_element_by_css_selector('.button.btn.btn-default.btn-lg')  
#NoSuchElementException:
#click_button = driver.find_element_by_xpath('//button[@class="btn.btn-default.btn-lg"]').click() #NoSuchElementException:
#driver.get("http://demo.opencart.com/index.php?route=product/search&search=ipod")
#TASK_4 find 'add to comparison button and click
#driver.find_element_by_xpath('//button[@data-original-title="Compare this Product"]').click()
#find_compare = driver.find_element_by_xpath("//div[@class='product-thumb.transition']/div/div/div/button[3]")  #NoSuchElementException:
#driver.find_element_by_xpath('//button[@onclick="compare.add*"]') 
#NoSuchElementException (class,id, name, etc only)
#.find_element_by_css_selector(".button-group[value='Update']").click()
#add_to_cp.click()
#button = driver.find_element_by_xpath("//button[@onclick='compare.add*']") - NoSuchElementException
#lose the browser window
#driver.quit(

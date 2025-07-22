from selenium import webdriver
from selenium.webdriver.common.by import By
import csv
import time

# Set up Chrome driver (make sure chromedriver is in your PATH)
driver = webdriver.Chrome()

# Search Flipkart for "laptops"
search_url = "https://www.flipkart.com/search?q=laptops"
driver.get(search_url)

# Close login popup if it appears
try:
    close_button = driver.find_element(By.XPATH, "//button[contains(text(),'✕')]")
    close_button.click()
except:
    pass  # If popup doesn't appear, continue

time.sleep(3)  # Wait for page to load

# CSV setup
with open("flipkart_laptops.csv", mode="w", newline="", encoding='utf-8') as file:
    writer = csv.writer(file)
    writer.writerow(["Product Name", "Price", "Rating"])

    # Scrape data
    products = driver.find_elements(By.CLASS_NAME, "_1AtVbE")
    for product in products:
        try:
            name = product.find_element(By.CLASS_NAME, "IRpwTa").text
            price = product.find_element(By.CLASS_NAME, "_30jeq3").text
            rating = product.find_element(By.CLASS_NAME, "_3LWZlK").text
            writer.writerow([name, price, rating])
        except:
            continue  # Skip products with missing info

driver.quit()
print("✅ Data saved to flipkart_laptops.csv")

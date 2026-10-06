# Selenium WebDriver – Registration Form Automation

## 📌 Project Overview

This project automates the **Registration Form** available on the Vinoth QA Academy Demo Site using **Selenium WebDriver with Python**.

The automation script fills in the registration form, selects the required options, enters address and contact details, dynamically extracts the verification code, and submits the form.

## 🌐 Demo Website

**Vinoth QA Academy – Demo Site**

https://vinothqaacademy.com/demo-site/

## 🎯 Objective

The objective of this project is to demonstrate basic Selenium WebDriver automation concepts such as:

* Opening a web page
* Locating web elements using XPath
* Entering text into input fields
* Selecting radio buttons
* Selecting checkboxes
* Handling dropdowns using `Select`
* Using explicit waits
* Extracting text dynamically
* Submitting a form
* Handling exceptions
* Closing the browser after execution

---

## 📝 Form Fields Automated

The following fields are automated in the registration form:

| Field             | Automation                   |
| ----------------- | ---------------------------- |
| First Name        | ✅                            |
| Last Name         | ✅                            |
| Gender            | ✅ Female                     |
| Course Interested | ✅ Selenium WebDriver, TestNG |
| Street Address    | ✅                            |
| City              | ✅                            |
| State             | ✅                            |
| Postal / Zip Code | ✅                            |
| Country           | ✅ India                      |
| Email             | ✅                            |
| Date of Demo      | ✅                            |
| Convenient Time   | ✅                            |
| Mobile Number     | ✅                            |
| Query             | ✅                            |
| Verification Code | ✅ Dynamic                    |
| Submit            | ✅                            |

---

## 🛠️ Technologies Used

* **Python**
* **Selenium WebDriver**
* **Google Chrome**
* **ChromeDriver**
* **XPath**
* **WebDriverWait**
* **Expected Conditions**

---


## ⚙️ Prerequisites

Before running the project, make sure the following are installed:

### 1. Python

Install Python from:

https://www.python.org/

Check the installation:

```bash
python --version
```

### 2. Selenium

Install Selenium using pip:

```bash
pip install selenium
```

### 3. Google Chrome

Install Google Chrome on your system.

Recent Selenium versions can automatically manage the required browser driver through Selenium Manager.

---

## ▶️ How to Run

### Step 1: Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

### Step 2: Open the project folder

```bash
cd Selenium-Registration-Form-Automation
```

### Step 3: Install Selenium

```bash
pip install selenium
```

### Step 4: Run the Python script

```bash
python registration_form.py
```

The Chrome browser will open automatically and the script will perform the registration workflow.

---

## 🔄 Automation Workflow

```text
Open Demo Website
        ↓
Enter First Name
        ↓
Enter Last Name
        ↓
Select Gender
        ↓
Select Courses
        ↓
Enter Address
        ↓
Select Country
        ↓
Enter Email
        ↓
Enter Demo Date
        ↓
Select Hour & Minute
        ↓
Enter Mobile Number
        ↓
Enter Query
        ↓
Extract Verification Code
        ↓
Enter Verification Code
        ↓
Click Submit
        ↓
Display Success Message
        ↓
Close Browser
```

---

## 🔍 Selenium Concepts Used

### 1. WebDriver

```python
driver = webdriver.Chrome()
```

Launches the Chrome browser using Selenium WebDriver.

### 2. Navigating to a Website

```python
driver.get("https://vinothqaacademy.com/demo-site/")
```

Opens the Vinoth QA Academy demo website.

### 3. XPath Locator

Example:

```python
driver.find_element(By.XPATH, "//input[contains(@id, 'vfb-7')]")
```

XPath is used to locate elements on the webpage.

### 4. Sending Data

```python
last_name.send_keys("Sarisha")
```

Enters text into an input field.

### 5. Radio Button

```python
gender_female.click()
```

Selects the Female radio button.

### 6. Checkbox

```python
course_selenium.click()
```

Selects the Selenium WebDriver course.

### 7. Dropdown

```python
country_dropdown = Select(
    driver.find_element(
        By.XPATH,
        "//select[contains(@id, 'vfb-13-country')]"
    )
)

country_dropdown.select_by_visible_text("India")
```

The Selenium `Select` class is used to handle dropdown menus.

### 8. Explicit Wait

```python
wait = WebDriverWait(driver, 15)
```

Waits up to 15 seconds for an element to become available.

Example:

```python
wait.until(
    EC.element_to_be_clickable(
        (By.XPATH, "//input[@value='Female']")
    )
)
```

### 9. Dynamic Verification Code

The verification example displayed on the webpage is extracted dynamically.

```python
verification_label = driver.find_element(
    By.XPATH,
    "//label[contains(text(), 'Example:')]"
).text

verification_code = "".join(
    filter(str.isdigit, verification_label)
)
```

This extracts only the digits from the verification label.

For example:

```text
Example: 33
```

The script extracts:

```text
33
```

and enters it into the verification field.

### 10. Exception Handling

```python
try:
    ...
except Exception as e:
    print(f"An error occurred: {e}")
```

This prevents the program from terminating without displaying the error.

### 11. Finally Block

```python
finally:
    time.sleep(15)
    driver.quit()
```

The browser remains open for 15 seconds and then closes automatically.

---

## 🧪 Test Data Used

| Field          | Test Data                                                 |
| -------------- | --------------------------------------------------------- |
| First Name     | Marino                                                    |
| Last Name      | Sarisha                                                   |
| Gender         | Female                                                    |
| Courses        | Selenium WebDriver, TestNG                                |
| Street Address | 123 Automation Lane                                       |
| City           | Chennai                                                   |
| State          | Tamil Nadu                                                |
| Postal Code    | 600001                                                    |
| Country        | India                                                     |
| Email          | [marino.test@example.com](mailto:marino.test@example.com) |
| Date           | 10/15/2026                                                |
| Time           | 10:30                                                     |
| Mobile         | 9876543210                                                |
| Query          | Automation testing request for registration workflow      |

> **Note:** The data above is sample test data used only for automation testing.

---

## 📸 Expected Result

After running the script:

1. Chrome browser opens.
2. The demo registration page loads.
3. All required fields are populated.
4. Gender is selected.
5. Selenium WebDriver and TestNG courses are selected.
6. Country, date, and time are selected.
7. Verification code is extracted dynamically.
8. The verification code is entered.
9. The form is submitted.
10. The browser remains open for 15 seconds and then closes.

---

<img width="1892" height="1042" alt="image" src="https://github.com/user-attachments/assets/d5a585bf-89d0-46ca-be85-ca485bd7c46d" />


**Completed – Selenium Registration Form Automation**

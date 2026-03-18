
# Myntra Automation Framework

A Selenium + TestNG based automation framework for Myntra, designed using the Page Object Model (POM) to ensure scalability, reusability, and maintainability.

---

# Project Structure

```
Myntra-Automation-Framework/
├── pom.xml                          # Maven dependencies & plugins
├── testng.xml                       # Test suite configuration
│
├── src/main/java/com/myntra/project/
│   ├── pages/
│   │   ├── HomePage.java            # Myntra home page actions & locators
│   │   ├── SearchResultsPage.java   # Product listing, filters, sorting
│   │   ├── ProductPage.java         # Product details, size selection
│   │   └── CartPage.java            # Add to bag, price validation
│   │
│   ├── drivers/
│   │   ├── DriverFactory.java       # WebDriver initialization
│   │   └── DriverManager.java       # Thread-safe driver handling
│   │
│   ├── listeners/
│   │   ├── TestListener.java        # Logs and screenshot on failure
│   │   ├── RetryAnalyzer.java       # Retry failed tests
│   │   └── RetryListener.java       # Apply retry globally
│   │
│   └── utils/
│       ├── ConfigReader.java        # Read config.properties
│       ├── WaitUtils.java           # Explicit wait handling
│       ├── ScreenshotUtils.java     # Capture screenshots
│       └── ExcelUtils.java          # Test data handling
│
├── src/test/java/com/myntra/project/tests/
│   ├── BaseTest.java                # Setup and teardown
│   ├── SearchTest.java              # Product search test cases
│   ├── ProductTest.java             # Product validation
│   └── CartTest.java                # Cart and price validation
│
├── src/test/resources/
│   ├── config/config.properties     # URL and browser config
│   └── testdata/TestData.xlsx       # Input test data
│
├── reports/screenshots/             # Failure screenshots
├── test-output/                     # TestNG reports
└── target/                          # Build output
```

---

# Configuration

Update configuration file:

```
src/test/resources/config/config.properties
```

```
url=https://www.myntra.com/
browser=chrome
implicit.wait=10
explicit.wait=15
```

---

# How to Run Tests

Run full test suite:

```
mvn test
```

Run specific test classes:

```
mvn test -Dtest=SearchTest
mvn test -Dtest=ProductTest
mvn test -Dtest=CartTest
```

---

# Reports

Screenshots are automatically saved in:

```
reports/screenshots/
```

TestNG report is generated at:

```
test-output/index.html
```

Open this file in a browser to view execution results.

---

# Test Coverage

* Product search functionality
* Product selection from listing
* Size selection validation
* Add to cart functionality
* Price validation in cart
* Handling dynamic UI elements

---

# Tech Stack

| Tool       | Version |
| ---------- | ------- |
| Java       | 8+      |
| Selenium   | 4.x     |
| TestNG     | 7.x     |
| Maven      | 3.x     |
| Apache POI | 5.x     |
| Log4j      | 2.x     |

---

# Key Features

* Page Object Model (POM) design
* Data-driven testing using Excel
* Screenshot capture on failure
* Retry mechanism for failed tests
* TestNG reporting
* Modular and scalable framework

---

# Challenges Handled

* Dynamic product loading and scrolling
* Size availability handling
* Price consistency validation
* Handling popups and overlays
* Synchronization with dynamic elements

---

# Conclusion

This framework provides a structured and reliable automation solution for Myntra. It validates key e-commerce workflows such as product search, selection, and cart functionality while ensuring maintainability and scalability.

---


# Android Mobile Test Automation Framework

**A portfolio project demonstrating mobile test automation, framework design, and QA engineering practices.**

## Project Overview

This project aims to build a maintainable and scalable mobile test automation framework for an Android demo application using Python, Appium, and Pytest.

The goal is to automate realistic mobile user journeys, validate application behavior, and demonstrate practical QA automation skills through a documented, version-controlled project.

This repository will evolve progressively, from the first automated test to a complete framework with reporting and CI/CD integration.

> **Project status:** In Progress

## Objectives

- Build an Android mobile test automation framework from scratch.
- Automate functional test scenarios for a demo shopping application.
- Apply the Page Object Model (POM) design pattern.
- Use reliable locators and explicit waits.
- Organize tests, fixtures, configuration, and test data.
- Generate readable test reports and capture failure evidence.
- Integrate automated checks into a CI/CD pipeline.
- Document test coverage, execution instructions, and known limitations.

## Tech Stack

| Technology | Purpose |
|---|---|
| Python | Automation programming language |
| Appium | Mobile automation framework |
| Appium UiAutomator2 | Android automation driver |
| Pytest | Test execution and fixtures |
| Appium Inspector | Element inspection and locator identification |
| Git & GitHub | Version control and portfolio |
| Allure Reports | Test reporting |
| GitHub Actions | CI/CD automation |

*Additional tools will be introduced when the project reaches the corresponding stage.*

## Application Under Test

**Application:** Sauce Labs My Demo App for Android

**Source:** https://github.com/saucelabs/my-demo-app-android

The application will be used to practice automated testing of shopping-related user journeys.

The APK will be stored locally and excluded from Git when appropriate, according to repository size and distribution considerations.

## Planned Test Scenarios

### 1. Application Launch
- Verify that the application launches successfully.
- Verify that the expected screen is displayed.
- Check that the application session is initialized correctly.

### 2. Product Catalog
- Verify that products are displayed.
- Validate product information.
- Open a product details screen.
- Verify navigation between screens.

### 3. Shopping Cart
- Add a product to the cart.
- Verify the selected product and quantity.
- Validate the cart total when applicable.
- Remove a product and verify the updated cart.

### 4. Checkout
- Validate required checkout fields.
- Test valid and invalid input data.
- Verify the checkout flow and confirmation screen when supported.

### 5. Negative and Edge Cases
- Submit incomplete forms.
- Validate error messages.
- Test boundary conditions where applicable.
- Verify behavior after navigation or repeated actions.

*Test scenarios will be adjusted to match the actual application's features and behavior.*

## Framework Architecture

The framework will separate test scenarios, page interactions, setup, and configuration.

```text
android-mobile-qa-automation/
├── apps/
├── pages/
├── tests/
├── test_data/
├── utils/
├── reports/
├── screenshots/
├── conftest.py
├── pytest.ini
├── requirements.txt
├── .gitignore
└── README.md
```

### Directory Responsibilities

- `apps/`: local APK files, excluded from Git when appropriate.
- `pages/`: Page Object classes and reusable UI interactions.
- `tests/`: automated test cases and business assertions.
- `test_data/`: test data separated from test logic.
- `utils/`: reusable helper functions.
- `reports/`: generated test reports, excluded from version control when appropriate.
- `screenshots/`: failure screenshots, excluded from version control when appropriate.
- `conftest.py`: Pytest fixtures and Appium driver lifecycle.
- `pytest.ini`: Pytest configuration.
- `requirements.txt`: Python dependencies.
- `.gitignore`: files and folders that should not be committed.

## Design Principles and Best Practices

- Follow the Page Object Model to separate UI interactions from test logic.
- Prefer stable accessibility IDs and resource IDs over fragile XPath locators.
- Use explicit waits instead of unnecessary fixed delays.
- Keep test cases independent and readable.
- Use meaningful assertions that validate expected business behavior.
- Manage the Appium session through Pytest fixtures.
- Capture screenshots and useful logs when tests fail.
- Avoid hardcoded credentials and sensitive information.
- Keep the framework modular and easy to maintain.

## Execution Guide

### Prerequisites

- Python
- Node.js and npm
- Appium Server
- Appium UiAutomator2 driver
- Android SDK and ADB
- Android emulator or connected Android device

### Install Dependencies

```bash
python -m venv .venv
python -m pip install --upgrade pip
python -m pip install Appium-Python-Client pytest
```

### Start Appium

```bash
appium
```

### Verify the Connected Device

```bash
adb devices
```

### Run Tests

```bash
pytest
```

*Execution commands and configuration will be updated as the framework evolves.*

## Reporting and CI/CD Roadmap

Planned improvements:

- Integrate Allure reporting.
- Capture screenshots and logs on failure.
- Add smoke and regression test suites.
- Configure GitHub Actions for automated checks.
- Publish test reports when the execution environment supports it.
- Document execution results and known limitations.

Android UI tests in CI will require an appropriately configured emulator or device environment.

## Quality Metrics

The project may track:

- Number of automated test cases.
- Passed, failed, and skipped tests.
- Test execution duration.
- Defects or unexpected behaviors identified.
- Regression coverage of key user journeys.

Metrics will be reported only when supported by actual test executions.

## Project Roadmap

- [ ] **Phase 1 — Environment setup:** Verify Python, Appium, UiAutomator2, ADB, and device connectivity.
- [ ] **Phase 2 — Application setup:** Download and install the demo APK.
- [ ] **Phase 3 — First automated test:** Launch the application and validate the initial screen.
- [ ] **Phase 4 — Framework foundation:** Configure fixtures, driver lifecycle, and Pytest.
- [ ] **Phase 5 — Page Object Model:** Create reusable page classes.
- [ ] **Phase 6 — Functional coverage:** Automate catalog, cart, and checkout scenarios supported by the application.
- [ ] **Phase 7 — Reliability:** Add explicit waits, failure screenshots, and logging.
- [ ] **Phase 8 — Reporting:** Integrate Allure and organize smoke/regression suites.
- [ ] **Phase 9 — CI/CD:** Add GitHub Actions and document execution constraints.
- [ ] **Phase 10 — Portfolio publication:** Add architecture documentation, real execution evidence, and a LinkedIn project announcement.

## What This Project Demonstrates

This project is designed to demonstrate practical skills in:

- Mobile test automation with Appium and Python.
- Test design and functional validation.
- Framework architecture and maintainability.
- Debugging and failure analysis.
- Test reporting and CI/CD fundamentals.
- Technical documentation and version control.



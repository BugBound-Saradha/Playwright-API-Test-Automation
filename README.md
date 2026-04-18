# 📘 Playwright API Test Automation

A robust and scalable **API Test Automation Framework** built using **Playwright** and modern JavaScript/TypeScript practices.
This project demonstrates how to design, execute, and maintain API tests efficiently with reusable utilities and structured test architecture.

---

## 🚀 Overview

This repository provides a complete setup for **automated API testing** using Playwright.

Playwright is a powerful automation framework that supports API testing alongside UI automation, enabling teams to maintain **end-to-end and API tests in a single ecosystem** ([Playwright][1]).

---

## ✨ Features

* 🔹 API automation using Playwright request context
* 🔹 Support for REST APIs (GET, POST, PUT/PATCH, DELETE)
* 🔹 Modular and scalable framework structure
* 🔹 Reusable helper functions for API requests
* 🔹 Centralized configuration and environment management
* 🔹 Assertions and response validation
* 🔹 Easy integration with CI/CD pipelines
* 🔹 Logging and reporting support (extendable to Allure or similar tools)

---

## 🏗️ Project Structure

```
Playwright-API-Test-Automation/
│── src/
│   ├── tests/            # Test specs
│   ├── utils/            # Utility/helper functions
│   ├── core/             # API clients / base methods
│── config/               # Environment & config files
│── playwright.config.ts  # Playwright configuration
│── package.json          # Dependencies & scripts
```

---

## ⚙️ Prerequisites

Make sure you have the following installed:

* Node.js (>= 16 or 18+ recommended)
* npm or yarn
* Git

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/BugBound-Saradha/Playwright-API-Test-Automation.git
cd Playwright-API-Test-Automation
```

Install dependencies:

```bash
npm install
```

Install Playwright browsers:

```bash
npx playwright install
```

---

## ▶️ Running Tests

Run all tests:

```bash
npx playwright test
```

Run a specific test file:

```bash
npx playwright test tests/api.spec.ts
```

Run in headed mode:

```bash
npx playwright test --headed
```

---

## 🧪 Example API Test

```javascript
import { test, expect } from '@playwright/test';

test('GET API Test', async ({ request }) => {
  const response = await request.get('/api/users');
  expect(response.status()).toBe(200);

  const body = await response.json();
  expect(body).toHaveProperty('data');
});
```

---

## 🔧 API Helper Methods (Example)

Reusable helper methods simplify API interactions:

```javascript
export async function getRequest(request, url) {
  return await request.get(url);
}

export async function postRequest(request, url, payload) {
  return await request.post(url, { data: payload });
}
```

These helpers promote **clean, reusable, and maintainable test code** ([GitHub][2]).

---

## 📊 Reporting

You can integrate reporting tools like:

* Allure Reports
* HTML Reports (default Playwright)
* CI/CD dashboards

---

## 🔄 CI/CD Integration

This framework can be integrated with:

* GitHub Actions
* Jenkins
* Azure DevOps

Typical pipeline steps:

1. Install dependencies
2. Run tests
3. Publish reports

---

## 🧠 Why Playwright for API Testing?

* Fast execution without browser overhead
* Built-in request handling
* Unified framework for UI + API testing
* Powerful assertions and debugging tools

Many teams use Playwright API testing to **prepare test data and support end-to-end flows efficiently** ([Reddit][3]).

---

## 📌 Future Enhancements

* ✅ Data-driven testing
* ✅ Environment-based configuration
* ✅ Authentication handling (OAuth, JWT)
* ✅ Schema validation
* ✅ Mocking APIs

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repo
2. Create a feature branch
3. Commit your changes
4. Submit a pull request

---

## 📄 License

This project is licensed under the MIT License.

---

## 👤 Author

**Saradha (BugBound)**
GitHub: [https://github.com/BugBound-Saradha](https://github.com/BugBound-Saradha)

# Nykaa-style Storefront UI Testing

## Project Description

A software-testing coursework project for a Nykaa-style storefront clone. It combines Cypress UI test scripts with manual test planning, cases and reports. The target is a learning site, not the official Nykaa website.

## Tech Stack Used

JavaScript, Cypress and XPath selectors, with a page-object-style class. Manual artifacts are PDF and Excel files.

## Setup & Installation

The repository does not include a package manifest or Cypress configuration. The following is a proposed setup for running the existing files in a **separate local working copy**; exact compatible versions and results have not been verified.

1. Install Node.js/npm and clone the repository:

   ```bash
   git clone https://github.com/abhijeet2829/Nykaa-e2e-testing.git
   cd Nykaa-e2e-testing
   npm init -y
   npm install --save-dev cypress @cypress/xpath
   ```

2. Create `cypress.config.js` at the repository root with:

   ```js
   const { defineConfig } = require("cypress");
   module.exports = defineConfig({
     e2e: {
       specPattern: "e2e/**/*.cy.js",
       supportFile: "cypress/support/e2e.js"
     }
   });
   ```

3. Create `cypress/support/e2e.js` containing:

   ```js
   require("@cypress/xpath");
   ```

4. Run `npx cypress open` for interactive execution or `npx cypress run` for a headless run. The page class targets `https://sweet-donut-1ca8e9.netlify.app/product.html`; network access and availability of that external site are required.

## Key Features

- Verify visibility of the first 3 product cards and their images.
- Select sorting and category filters, and exercise adding 3 products to a cart with a cart-count assertion.
- Keep reusable selectors and actions in [the product page class](./e2e/POM/Product.js); test cases live in [the Cypress spec](./e2e/spec.cy.js).
- Review the [test plan](./test%20Plan.pdf), [test scenarios and cases](./test%20Scenarios%20and%20Cases.xlsx), [bug report](./Bug%20report.pdf), [summary report](./Summary%20report.pdf).

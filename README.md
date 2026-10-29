# Nykaa-style Storefront UI Testing

A software-testing coursework project containing Cypress UI tests and manual testing documents for a Nykaa-style storefront. The tests use a reusable page class and target a storefront clone, not the official Nykaa website.

## Scope

- Check product and image visibility.
- Exercise product selection and add 3 products; assert that the cart contains 3 items.
- Review the included [test plan](./test%20Plan.pdf), [test cases](./test%20Scenarios%20and%20Cases.xlsx), [bug report](./Bug%20report.pdf), [summary report](./Summary%20report.pdf) and [mind map](./Mind%20map.png).

## Technology

JavaScript, Cypress and XPath-based selectors. The test file is [e2e/spec.cy.js](./e2e/spec.cy.js); its reusable page class is [e2e/POM/Product.js](./e2e/POM/Product.js).

## Setup and execution

1. Clone the repository:

   ```bash
   git clone https://github.com/abhijeet2829/Nykaa-e2e-testing.git
   cd Nykaa-e2e-testing
   ```

2. Set up a compatible Cypress project with the XPath support used by the page class, and include the existing `e2e` files.
3. Open or run the tests using your Cypress project's configuration. The repository does not currently contain a package manifest or Cypress configuration, so exact dependency versions and a one-command setup are not provided.

## Limitations

This is a coursework repository. Some test blocks are incomplete, and the availability or structure of the external storefront may change. Tests have not been rerun for this documentation update.

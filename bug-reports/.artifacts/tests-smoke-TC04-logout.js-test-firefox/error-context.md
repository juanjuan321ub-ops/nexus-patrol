# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: tests\smoke\TC04-logout.js >> test
- Location: automation-scripts\tests\smoke\TC04-logout.js:14:1

# Error details

```
Error: expect(locator).toContainText(expected) failed

Locator: locator('#flash')
Expected substring: "You logged into a secure area! ×"
Timeout: 5000ms
Error: element(s) not found

Call log:
  - Expect "toContainText" with timeout 5000ms
  - waiting for locator('#flash')

```

# Test source

```ts
  1  | // ============================================
  2  | // ⚠️  IMPORTS MANAGED AUTOMATICALLY
  3  | // Do not modify these imports manually.
  4  | // Sentinel Automation Core System Engine
  5  | // ============================================
  6  | import { test }         from '../../utils/base-fixture.js';
  7  | import { expect }       from '@playwright/test';
  8  | import { HomePage }     from '../../pages/HomePage.js';
  9  | import { AuthPage }     from '../../pages/AuthPage.js';
  10 | import { SignupPage }   from '../../pages/SignupPage.js';
  11 | import { generateUser } from '../../data/generators.js';
  12 | 
  13 | // @qa-ops-adapted
  14 | test('test', async ({ page }) => {
  15 |   await page.goto('https://the-internet.herokuapp.com/login');
  16 |   await page.getByRole('textbox', { name: 'Password' }).click();
  17 |   await page.getByRole('textbox', { name: 'Password' }).press('ControlOrMeta+V');
  18 |   await page.getByRole('textbox', { name: 'Password' }).fill('SuperSecretPassword! ');
  19 |   await page.getByRole('textbox', { name: 'Username' }).click();
  20 |   await page.getByRole('textbox', { name: 'Username' }).press('ControlOrMeta+V');
  21 |   await page.getByRole('textbox', { name: 'Username' }).fill('tomsmith');
  22 |   await expect(page.locator('h2')).toContainText('Login Page');
  23 |   await page.getByRole('button', { name: ' Login' }).click();
  24 |   await page.getByRole('textbox', { name: 'Username' }).click();
  25 |   await page.getByRole('textbox', { name: 'Username' }).press('ControlOrMeta+V');
  26 |   await page.getByRole('textbox', { name: 'Username' }).fill('tomsmith');
  27 |   await page.getByRole('textbox', { name: 'Password' }).click();
  28 |   await page.getByRole('textbox', { name: 'Password' }).press('ControlOrMeta+V');
  29 |   await page.getByRole('textbox', { name: 'Password' }).fill('SuperSecretPassword!');
  30 |   await page.getByRole('button', { name: ' Login' }).click();
> 31 |   await expect(page.locator('#flash')).toContainText('You logged into a secure area! ×');
     |                                        ^ Error: expect(locator).toContainText(expected) failed
  32 |   await page.getByRole('link', { name: 'Logout' }).click();
  33 |   await expect(page.locator('#flash')).toContainText('You logged out of the secure area! ×');
  34 | });//fghtt
```
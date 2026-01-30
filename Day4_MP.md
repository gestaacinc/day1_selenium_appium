# Machine Problem: 

**Objective:** Combine all the basic concepts you've learned (Navigation, Locators, Dropdowns others elements will be done using AI tools) into a single, cohesive automation script.

**Scenario:**
You are testing the "The Internet" web application. You need to navigate through various features to ensure the site is functioning correctly.

---

## Instructions

Create a new Java class named `BasicMachineProblem` (or use your own name) and implement the following steps in a single `@Test` method:

### Phase 1: The Setup & Validation
1.  Launch Chrome and navigate to `https://the-internet.herokuapp.com/`.
2.  **Verification:** Assert that the page title is exactly `"The Internet"`.

### Phase 2: The Login (Interaction & Locators)
3.  Find and click the **"Form Authentication"** link.
4.  Enter Username: `tomsmith`
5.  Enter Password: `SuperSecretPassword!`
6.  Click the **Login** button.
7.  **Verification:** Assert that the green success message contains `"You logged into a secure area!"`.
8.  Click the **Logout** button.
9.  **Navigation:** Return to the main homepage (`https://the-internet.herokuapp.com/`).

### Phase 3: The Dropdown (Select Class)
10. Find and click the **"Dropdown"** link.
11. Select **"Option 2"** from the dropdown menu.
12. **Verification:** Assert that "Option 2" is indeed selected.
13. **Navigation:** Go back to the homepage.

### Phase 4: The Checkboxes (State Validation)
14. Find and click the **"Checkboxes"** link.
15. **Logic:** If "Checkbox 1" is *not* checked, check it.
16. **Verification:** Assert that **both** Checkbox 1 and Checkbox 2 are currently checked.
17. **Navigation:** Go back to the homepage.

### Phase 5: The Alert (Pop-ups)
18. Find and click the **"JavaScript Alerts"** link.
19. Click the button **"Click for JS Confirm"**.
20. **Action:** Switch to the alert and click **OK** (Accept).
21. **Verification:** Assert that the result text on the page says `"You clicked: Ok"`.
22. **Navigation:** Go back to the homepage.

### Phase 6: The Patience Test (Explicit Waits)
23. Find and click the **"Dynamic Loading"** link.
24. Click **"Example 1: Element on page that is hidden"**.
25. Click the **"Start"** button.
26. **Wait:** Use an *Explicit Wait* for the loading bar to finish and the text `"Hello World!"` to appear.
27. **Verification:** Assert that the text `"Hello World!"` is visible.

---

## Technical Requirements
*   Use `WebDriverManager` for setup.
*   Use `WebDriverWait` for synchronization (Step 26).
*   Use `Assert` (TestNG) for all verifications.
*   Use `Thread.sleep()` **ONLY** if you want to visually slow it down for your own demo (optional), but not for synchronization logic.

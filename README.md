# Day 2 Machine Problem: "The Unstable UI Suite"

**Role:** Automation Architect Candidate
**Time Limit:** 45 Minutes

## The Scenario
You have been hired by a legacy software company. Their application has three specific "flaky" features that manual testers hate checking because they are tedious.

Your task is to write a **single Java Test Class** named `MachineProblem.java` that automates these three challenges.

---

## Challenge 1: The "Dynamic" Audit Table
**Topic:** XPath Axes & Relative Locators
**Target URL:** `https://the-internet.herokuapp.com/tables`

**The Problem:**
The "Due" amount for users changes frequently, and the rows sort randomly. You cannot use row numbers (e.g., `tr[2]`).

**Requirements:**
1.  Locate the row for user **"Jason"** (Last Name).
2.  Use **XPath Axes** (`following-sibling` or `parent`) to find the **"Due"** amount in that same row.
3.  **Print** the amount to the console.
4.  **Assertion:** Verify the amount is `$100.00`.
5.  **Bonus Constraint:** Locate the "Edit" button for Jason using a **Relative Locator** (e.g., "The link to the right of the cell containing '$100.00'").

---

## Challenge 2: The "Hidden" Config
**Topic:** Shadow DOM
**Target URL:** `http://watir.com/examples/shadow_dom.html`

**The Problem:**
The configuration text is hidden inside a Shadow DOM component to prevent scraping. Standard locators fail here.

**Requirements:**
1.  Penetrate the **Shadow Host**.
2.  Locate the internal text element.
3.  **Assertion:** Verify the text displayed is exactly `"some text"`.
4.  *Hint:* Remember which locator strategy is forbidden inside the Shadow DOM.

---

## Challenge 3: The "Isolated" Editor
**Topic:** iFrames & CSS Selectors
**Target URL:** `https://the-internet.herokuapp.com/iframe`

**The Problem:**
The text editor is actually a separate website embedded in an iFrame. Your driver cannot "see" the text box initially.

**Requirements:**
1.  Switch context into the iFrame.
2.  Clear the existing text.
3.  Type: `"I have conquered the iFrame!"`.
4.  **Critical Step:** Switch context *back* to the main page.
5.  **Assertion:** Find the main page heading ("An iFrame containing...") using a **CSS Selector** and verify it is displayed.

---

## Submission Checklist
* [ ] All 3 tests pass with `mvn test`.
* [ ] No `Thread.sleep()` was used.
* [ ] Code handles the driver setup and teardown automatically.

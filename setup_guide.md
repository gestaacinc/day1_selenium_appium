# Setup and Execution Guide

This guide will help you set up your machine and run the automation exercises individually.

## 1. Prerequisites
Ensure you have the following installed on your machine:
*   **Java Development Kit (JDK)**
*   **Apache Maven** (For building and running the project)
*   **An IDE** (VS Code, IntelliJ, or Eclipse)

## 2. Project Configuration (pom.xml)
This project uses **Maven** to manage libraries. Ensure your `pom.xml` contains the following dependencies:

```xml
<dependencies>
    <!-- Selenium 4.28.1 (Latest Stable) -->
    <dependency>
        <groupId>org.seleniumhq.selenium</groupId>
        <artifactId>selenium-java</artifactId>
        <version>4.28.1</version>
    </dependency>

    <!-- TestNG (The Test Runner) -->
    <dependency>
        <groupId>org.testng</groupId>
        <artifactId>testng</artifactId>
        <version>7.9.0</version>
        <scope>test</scope>
    </dependency>

    <!-- WebDriverManager (Auto-downloads drivers) -->
    <dependency>
        <groupId>io.github.bonigarcia</groupId>
        <artifactId>webdrivermanager</artifactId>
        <version>5.9.2</version>
    </dependency>

    <!-- Logger (Fixes "Failed to load class" error) -->
    <dependency>
        <groupId>org.slf4j</groupId>
        <artifactId>slf4j-simple</artifactId>
        <version>1.7.36</version>
        <scope>test</scope>
    </dependency>
</dependencies>
```

### How to Install/Update Dependencies
If you have just cloned the project or made changes to `pom.xml`, run the following command in your terminal (at the project root) to download the required libraries:

```bash
mvn clean install
```
*Alternatively, if you are using an IDE like VS Code or IntelliJ, you can look for a "Reload Maven Project" button.*

---

## 3. How to Run a Specific Test File
You do not need to run all tests at once. You can execute a single test file using the command line.

### Command Syntax:
```bash
mvn -Dtest=TestClassName test
```

### Examples:
To run the **Navigation Commands** exercise:
```bash
mvn -Dtest=Exercise2_NavigationCommands test
```

To run the **Locators and Interaction** exercise:
```bash
mvn -Dtest=Exercise3_LocatorsAndInteraction test
```

**Note:**
*   Make sure you are running the command from the **root directory** of the project (where the `pom.xml` file is located).
*   Do not include the `.java` extension in the command (e.g., use `Exercise1_LaunchBrowser`, NOT `Exercise1_LaunchBrowser.java`).

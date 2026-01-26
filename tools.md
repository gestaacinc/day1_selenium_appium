# Bootcamp Pre-requisites: Selenium & Appium

**Goal:** Configure your local machine for Java, Web, and Mobile Automation.

This guide covers the essential tools required for the 10-day bootcamp. Please install these **before** Day 1 to ensure a smooth start.

## 1. The Core Stack (Required for Everyone)

Regardless of your OS, you need these three core components:

1. **Code Editor:** Visual Studio Code (Recommended) or IntelliJ IDEA.
2. **Language:** Java Development Kit (JDK) 11 or higher.
3. **Build Tool:** Maven (Apache Maven).

## 2. Windows Installation Guide

### Option A: The "Manual" Way (Standard)

1. **Install Java (JDK 11+)**
   * Download **OpenJDK 17** (LTS) from [Adoptium.net](https://adoptium.net/).
   * Run the installer and ensure you check the box: **"Set JAVA_HOME variable"**.
   * *Verify:* Open Command Prompt -> `java -version`.

2. **Install Maven**
   * Download the **Binary zip archive** from [maven.apache.org](https://maven.apache.org/download.cgi).
   * Extract it to `C:\Maven`.
   * Add to Path:
     * Search "Edit the system environment variables".
     * Click **Environment Variables** -> System Variables -> **Path** -> Edit -> New.
     * Paste: `C:\Maven\apache-maven-x.x.x\bin`.
   * *Verify:* Open Command Prompt -> `mvn -version`.

3. **Install VS Code**
   * Download from [code.visualstudio.com](https://code.visualstudio.com/).
   * **Crucial Extension:** Open VS Code, go to Extensions (`Ctrl+Shift+X`), and install **"Extension Pack for Java"** by Microsoft.

### Option B: The "Power User" Way (Chocolatey)

If you have [Chocolatey](https://chocolatey.org/) installed, run this in PowerShell (Admin):

```powershell
choco install openjdk17 maven vscode -y

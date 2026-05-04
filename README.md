# ITPM--Assignment-1-P# Playwright Test Automation Project

## 📌 Overview

This project automates testing of a web-based chat translator using **Playwright (Python)**.
Test cases are read from an Excel file, executed on the web application, and results are written back to the same file.

The automation simulates user interaction by:

* Entering input text
* Waiting for translation output
* Comparing actual vs expected results
* Updating execution status (PASS / FAIL)

---

## ⚙️ Technologies Used

* Python 3.x
* Playwright
* OpenPyXL (Excel handling)

---

## 📁 Project Structure

```
test_automation/
│
├── test_automation.py          # Main automation script
├── Assignment 1_testcases.xlsx # Test case file
├── README.md                   # Project documentation
```

---

## 🚀 Setup Instructions

### 1. Install Python

Download and install Python (3.11 or above)
Make sure to enable **"Add Python to PATH"**

---

### 2. Install Dependencies

Open terminal (PowerShell or CMD) and run:

```
pip install -U pip
pip install playwright openpyxl
playwright install
```

---

### 3. Navigate to Project Folder

```
cd D:\test_automation
```

---

## ▶️ How to Run

Run the automation script using:

```
python test_automation.py --excel "Assignment 1_testcases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 60000 --type-delay-ms 80 --slow-mo-ms 500 --save-every 1 --keep-open
```

---

## 📊 Excel Test Case Format

The Excel file must contain the following columns:

* TC ID
* Input length type
* Input
* Expected output
* Actual output *(auto-filled)*
* Status *(auto-filled)*

⚠️ Do NOT manually fill "Actual output" and "Status"

---

## 🔍 How It Works

1. Reads test cases from Excel
2. Opens browser using Playwright
3. Navigates to the translator web application
4. Inputs text into the chat field
5. Waits for translation output
6. Compares expected vs actual output
7. Writes results back to Excel

---

## ⚠️ Known Limitations

* The target website may respond slowly due to:

  * Network latency
  * External API delays
  * Advertisements

* Fixed wait time (`--wait-ms`) may not always be reliable

* Some test cases may fail due to inconsistent website behavior

---

## 💡 Improvements (Future Work)

* Implement dynamic wait (wait until output appears)
* Add retry mechanism for failed translations
* Improve selector stability
* Add logging and error handling

---

## 📌 Notes

* Ensure Excel file is **closed** before running the script
* Use correct file paths to avoid execution errors
* Do not manually interrupt the browser during execution

---

## 👨‍💻 Author

* Name: [Your Name Here]

---

## 📄 License

This project is for academic purposes only.
lay-Wright-Project

# EWB Phishing URL Awareness Checker

## Overview

Phishing is a type of online fraud where attackers use fake links or websites to trick people into sharing personal information such as passwords, OTPs and bank details.

The Phishing URL Awareness Checker is a simple project that checks a URL for some common warning signs. It helps users identify suspicious URL patterns and reminds them to be careful before opening unknown links.

The project includes a Python-based checker and a simple HTML webpage. The Python program runs in the command line, while the HTML page provides a basic user-friendly interface.

**Note:** The two versions work independently. The webpage does not connect to the Python program.

## Features

- Detects the use of an @ symbol in a URL.
- Identifies unusually long URLs (over 100 characters).
- Detects IP addresses used as hostnames (Python version).
- Identifies URLs with many hostname segments (Python version).
- Detects punycode-style hostnames (Python version).
- Flags URLs that use HTTP instead of HTTPS.
- Displays warning messages for suspicious patterns.
- Allows users to check URLs easily.

## Requirements

- Python 3.10 or later.
- Any modern web browser (Google Chrome recommended).
- No additional Python packages required.

## Project Files

- `checker.py` – Python program for checking URL warning signs.
- `index.html` – Webpage version of the checker.
- `.gitignore` – Specifies files and folders Git should ignore.

## How to Run

### Python Version

1. Open the project folder.
2. Open `checker.py` using Python IDLE.
3. Click Run → Run Module.
4. Enter a sample URL when prompted.
5. Type `q` to exit.

### Webpage Version

1. Open the project folder.
2. Double-click `index.html`.
3. The webpage opens in Google Chrome.
4. Enter a URL in the input box.
5. Click the CHECK URL button to see the result.

## Example Output

**Sample Input:**

`http://192.0.2.10/account`

**Expected Python Output:**

- Uses an IP address instead of a familiar domain.
- Uses HTTP. HTTPS alone does not prove trust.

**Result:** REVIEW CAREFULLY!

## Testing

| # | Sample URL | Expected Result |
|---|---|---|
| 1 | `https://google.com` | No listed warning signs |
| 2 | `http://192.0.2.10/account` | IP address and HTTP warnings (Python) |
| 3 | `http://example.com@sample.invalid/login` | @ symbol and HTTP warnings |
| 4 | `https://a.b.c.d.e.example.invalid/path` | Many hostname segments warning (Python) |
| 5 | `http://example.com` | HTTP warning |

## Improvements

1. **Easy URL Checking:** Users can enter a URL and view possible warning signs.
2. **Simple Interface:** An HTML webpage makes the checking process easy to understand.
3. **Multiple URL Checking:** The Python program allows users to check multiple URLs without restarting.
4. **Warning Messages:** The program displays messages to help users review suspicious links.

## Limitations

- This project checks only selected URL warning signs.
- It does not open or visit any website.
- It does not scan for malware.
- It does not use online security or reputation services.
- A URL without warning signs is not guaranteed to be safe.

## Ethical Use

This project is developed for educational purposes and cybersecurity awareness. Use sample URLs for testing. Do not collect personal information or passwords.

## Author

**Asima Hussain**  
EWB Project – Phishing URL Awareness Checker
# 💱 Exchange Rates from the National Bank of Moldova

This project is a self-contained HTML + JavaScript web page that displays official exchange rates from the National Bank of Moldova (BNM) for a selected date, and compares them to the previous day’s rates.
It fetches live data from [bnm.md](https://bnm.md/) via the `allorigins.win` proxy service to bypass CORS restrictions.

## 🔧 Features

* Manual date input (format: `YYYY-MM-DD`)
* Loads and displays exchange rates for: USD, EUR, RUB, RON, UAH
* Compares today's rates with yesterday’s
* Generates dynamic textual summaries for rate changes
* Builds Markdown-compatible tables
* Copy-to-clipboard functionality for Markdown output
* Dual language support: 🇷🇺 Russian and 🇷🇴 Romanian

## 📦 Technologies Used

* Vanilla HTML, CSS, and JavaScript
* `DOMParser` for parsing XML
* `fetch()` with retry logic
* `allorigins.win` for CORS bypass
* Markdown-friendly output formatting

## 🚀 How to Use

1. Open the `curs.html` file in your browser.
2. Click the **“📥 Get Rates”** button.
3. Enter a desired date (e.g., `2025-06-23`).
4. Wait for the data to load and view the results.
5. Click **📋 Copy** to copy the generated summary and table in Markdown format.

## 📝 Example Markdown Output

```markdown
# Exchange Rate Dynamics from the National Bank of Moldova on 2025-06-23

According to official data from the National Bank of Moldova on 23.06.2025:

• The US dollar slightly increased  
• The Euro remained unchanged  
• ...

| Currency | Rate (MDL) | Change     |
|----------|------------|------------|
| USD      | 17.9500    | +0.0500    |
| EUR      | 19.2300    | 0.0000     |
```

## 📁 Files

* `curs.html` — the main HTML file containing both interface and logic
* No external libraries required (everything is vanilla JS)

## ⚠️ Notes

* Data source: [bnm.md](https://bnm.md)
* If `allorigins.win` is offline or blocked, the data will not load
* Supported currency codes: `USD`, `EUR`, `RUB`, `RON`, `UAH`

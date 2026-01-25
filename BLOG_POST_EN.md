# 🚀 Stop Stressing Over CouchDB Imports: Load CSV & JSON in Seconds

*"I'll just quickly import some test data..."* – every developer has said this. And every developer knows it often turns into an hour of frustration: broken JSON formats, encoding errors in CSVs, or endless `curl` commands that are impossible to remember.

We – **Team Wanju & KI Gemini** – had enough. That's why we built a tool that just works.

## The Problem

CouchDB is great, but getting data into it can be a pain.
*   **Fauxton** (the web UI) is okay for single documents, but tedious for bulk uploads.
*   **Curl** is powerful, but heaven help you if you forget a quote on Windows.
*   **Custom scripts** are rewritten every time and break at the first special character.

## The Solution: CouchDB-Importer

Our [CouchDB-Importer](https://github.com/wanjus/couchdb-importer) is a "Swiss Army Knife" for data imports, written in Python. It's pragmatic, robust, and open source.

### What can it do?

1.  **CSV & JSON Support:** Whether it's an Excel export or an API dump, the tool handles both.
2.  **Intelligent:** JSON list? `docs` wrapper? Single object? The script detects the format automatically.
3.  **Auto-DB:** If the target database doesn't exist, it's created automatically. No more manual `PUT` requests.
4.  **Fault Tolerant:** Simple strings in a list are automatically wrapped in objects so CouchDB accepts them.
5.  **Feedback:** A clean progress bar shows you exactly what's happening.

## Quick Start

All you need is Python.

```bash
# 1. Clone the repo
git clone https://github.com/wanjus/couchdb-importer.git
cd couchdb-importer

# 2. Install dependencies
pip install -r requirements.txt

# 3. Import data (Example)
python CouchDB-Importer.py --file my_data.csv --db testdb --user admin --password secret
```

That's it. Your data is in.

## Join in!

The project is **Open Source (MIT License)**. We welcome GitHub stars, issues, or pull requests.

👉 **[Go to GitHub Repository](https://github.com/wanjus/couchdb-importer)**

---
*Developed with ❤️ and Python by Jürgen (Wanju) and Gemini.*

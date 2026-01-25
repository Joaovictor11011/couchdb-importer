# CouchDB-Importer

A versatile Python script for easily importing CSV and JSON data into CouchDB.

## Features

*   **CSV Support**: Includes column validation and a progress indicator.
*   **JSON Support**: Supports various structures (CouchDB standard `{"docs": [...]}` or simple lists).
*   **Fault Tolerant**: Automatically wraps simple data types (strings/numbers) into objects.
*   **Auto-DB Creation**: Automatically creates the target database if it doesn't already exist. 🚀

![CouchDB Importer Demo](demo_screenshot.png)

## Installation

```bash
git clone https://github.com/wanjus/couchdb-importer.git
cd couchdb-importer
pip install -r requirements.txt
```

## Usage

The script is controlled via the command line:

```bash
python CouchDB-Importer.py --file <FILEPATH> --db <DB_NAME> [OPTIONS]
```

### Parameters:
*   `--file`: Path to the source file (`.csv` or `.json`). **(Required)**
*   `--db`: Name of the target database. **(Required)**
*   `--url`: CouchDB URL (Default: `http://localhost:5984`).
*   `--user`: CouchDB username.
*   `--password`: CouchDB password.
*   `--id-column`: Column or field name to be used as the document ID (`_id`).

## Examples

### Importing a JSON file:
```bash
python CouchDB-Importer.py --file test.json --db test --user admin --password admin
```

### Importing a CSV file:
```bash
python CouchDB-Importer.py --file test.csv --db test --user admin --password admin
```

### With a specific ID column:
```bash
python CouchDB-Importer.py --file data.csv --db my_db --id-column customer_id
```

## Credits

Developed by **Team Wanju & KI Gemini**.

## License

This project is released under the MIT License. See [LICENSE](LICENSE) for details.
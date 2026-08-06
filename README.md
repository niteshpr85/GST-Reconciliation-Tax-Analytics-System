# GST Reconciliation & Tax Analytics System

A beginner-friendly, industry-style GST reconciliation system built with Streamlit, Python, Pandas, Plotly, SQLite, and ReportLab.

## Project Overview

This system compares company GST purchase/sales records with government GSTR-2B data to identify: missing invoices, duplicate invoices, taxable value mismatches, GST mismatches, and reconciliation gaps. It also supports corrections, dashboard analytics, and exportable Excel/PDF reports.

## Features

- Clean and validate GST invoice data
- Reconcile company invoices against GSTR-2B government data
- Detect missing invoices and duplicate records
- Identify taxable value and GST component mismatches
- Correction workflow stored in SQLite
- Interactive Streamlit dashboard with Plotly charts
- Excel and PDF report generation

## Project Structure

```
GST-Reconciliation-System/
│
├── app.py
├── requirements.txt
├── README.md
│
├── data/
│   ├── company_gst.xlsx
│   └── gstr2b.xlsx
│
├── modules/
│   ├── data_cleaning.py
│   ├── reconciliation.py
│   ├── correction.py
│   ├── database.py
│   ├── dashboard.py
│   └── reports.py
│
├── database/
│   └── gst_reconciliation.db
│
└── reports/
```

## Installation

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

## Windows Quick Start

Double-click `run_app.bat` or run it from PowerShell / Command Prompt:

```bat
run_app.bat
```

This will create a `venv`, install required packages, and launch the Streamlit app on `http://localhost:8501`.

## Manual Run

If you want to run it manually, use:

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
streamlit run app.py --server.port=8501 --server.address=0.0
```

## Usage

1. Upload your company GST Excel file and GSTR-2B Excel file, or use the bundled sample data.
2. Click **Run Reconciliation**.
3. Review dashboard KPIs and charts.
4. Use the Corrections tab to fix mismatches.
5. Export reports from the Reports tab.

## Sample Data

The app includes sample files in the `data/` folder:
- `data/company_gst.xlsx`
- `data/gstr2b.xlsx`

Use **Load Sample Data** from the sidebar to populate the app quickly and begin testing immediately.

If you want to use your own files, upload them using the sidebar upload widgets.

## Future Enhancements

- Upgrade SQLite storage to MySQL or PostgreSQL
- Add authentication and role-based access
- Add invoice upload history and audit trails
- Add automated reconciliation scheduling
- Add email export and approval workflows

## Notes

- The sample data includes realistic Indian GST records and built-in mismatch scenarios.
- The app is modular and easy to extend for enterprise deployments.

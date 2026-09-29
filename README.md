[![python](https://img.shields.io/badge/Python-3.9-3776AB.svg?style=flat&logo=python&logoColor=white)](https://www.python.org)

# PDF reporting for HDAB id project

This Python script generates PDF reports for specimens submitted to the University of Hawaii Insect Museum (UHIM) for identification by the Hawaiian Department of Agriculture and Biosecurity (HDAB). The script pulls the identification information from a postgresql database and adds a specimen image from a local folder. Individual reports are then merged into a combined report with size reduction.

The script is available in a Jupyter notebook: "psql_pdf_reporter.ipynb"

The only file not provided is a (hidden) .connectstring_databasename text file that has the postgres connection information in the SQLalchemy format:

```bash
dialect+driver://username:password@host:port/database
```

The dialect is postgresql and the driver is psycopg2. In the filename, change 'databasename' for the name of your database.

Dependencies (all are available through conda):
- PyPDF, v5.0 or higher (lower versions don't support functions to reduce PDF file size) for combining the individual reports
- PsycoPG, for connecting with the postgresql database
- Pandas, for moving the postgresql table data into a dataframe
- ReportLab, for building the PDF page
- Pillow, for resizing specimen images
- SQLalchemy, for a secure connection with the postgresql database
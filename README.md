# PDF reporting for HDAB id project

This script will read data from a postgresql database and create PDF reports for each row (morphospecies) and include an image for that morphospecies, if available. Optionally, all PDFs are merged as well to create a single report.

Each PDF page is about .5 MB if an image is available, 0.3 MB without an image.

Dependencies: the script uses Python and the ReportLab toolkit https://www.reportlab.com/, the PyPDF module https://pypdf.readthedocs.io/en/stable/ to merge generated PDF files, and some basic modules. All are available through Anaconda.
# PDF reporting for HDAB id project

This script will read data from a postgresql database and create PDF reports for each row (morphospecies) and include an image for that morphospecies, if available. This script uses Python and the ReportLab toolkit https://www.reportlab.com/, the PyPDF module https://pypdf.readthedocs.io/en/stable/ to merge generated PDF files, and some basic modules. 

Dependencies:
- PyPDF v5.0 or higher (lower versions don't support functions to reduce PDF file size)
- PsycoPG
- Pandas
- ReportLab
- Pillow


To do:
- Reduce image file sizes
- Add argpase to run as a script
    - include wishlist option to supply a csv with list of morphospeciescodes to generate report for
    - include argument to set directory with images
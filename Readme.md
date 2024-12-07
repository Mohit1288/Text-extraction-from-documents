

---

# Text Extraction from Documents

This project automates the extraction of structured data from unstructured documents, primarily resumes in **PDF** and **DOCX** formats. It identifies and extracts key information such as personal contact details (e.g., phone numbers, email addresses), work experience, and relevant dates using various Python libraries like `pdfminer`, `docx2txt`, `re` (regular expressions), and `dateparser`.

## Project Overview

The **Text Extraction from Documents** project is designed to streamline the process of extracting meaningful information from documents. It can be used for processing resumes, job applications, and any text-based documents where structured data needs to be extracted from unstructured text.

The core functionalities of this project include:
- **Extracting contact details** (mobile number, email, GitHub, LinkedIn)
- **Extracting professional experience** and **experience dates**
- **Parsing and converting PDFs and DOCX documents** to text

## Features

- **PDF and DOCX Parsing**: Extract text from PDF and DOCX files using `pdfminer` and `docx2txt` respectively.
- **Data Extraction**:
  - **Mobile number**: Extracts phone numbers in various formats (e.g., +1-123-456-7890).
  - **Email address**: Identifies and extracts email addresses.
  - **Experience details**: Extracts work experience, including job titles, companies, and descriptions.
  - **LinkedIn and GitHub**: Detects LinkedIn and GitHub profiles if they exist in the document.
- **Date Parsing**: Uses the `dateparser` library to extract and normalize date formats (e.g., experience dates).

## Installation

### Prerequisites

Ensure you have Python 2.7+ (for `cStringIO` compatibility) or Python 3.x installed. You will also need to install the necessary libraries to run this project.

### Step 1: Clone the repository

```bash
git clone https://github.com/your-username/text-extraction-from-documents.git
cd text-extraction-from-documents
```

### Step 2: Install the required libraries

Install the dependencies using `pip`:

```bash
pip install -r requirements.txt
```

The `requirements.txt` should contain the following libraries:

```
pdfminer.six
docx2txt
dateparser
```

### Step 3: Download or add a document

Place your PDF or DOCX file in the same directory as the script, or provide the path to the file in the script.

## Usage

### 1. **Data Extraction from PDF and DOCX Files**

To extract text from a document, use the **DataExtractionFromPdfDocx.py** script. The script will automatically detect whether the file is a PDF or a DOCX file and process it accordingly.

### 2. **Extracting Dates from Strings (Optional)**

You can also extract and normalize dates from a string using the **extract_date_from_string.py** script (this script was mentioned but not fully provided in the initial prompt). Ensure the date extraction is consistent and formats dates like "January 2020" or "12/2020" into a standard format.

## File Structure

```plaintext
text-extraction-from-documents/
│
├── DataExtractionFromPdfDocx.py      # Main script for extracting data from PDFs and DOCX
├── extract_date_from_string.py       # Optional script for extracting dates from strings
├── requirements.txt                  # Python dependencies
├── README.md                         # Project documentation
└── your-file.pdf                     # Example document (PDF or DOCX)
```

## Example Output

For a PDF or DOCX document, the script will output:

```plaintext
===MOBILE==
+1-123-456-789

===email==
example@email.com

===Exp date==
[datetime.datetime(2019, 6, 1, 0, 0), 'Present']

===experience==
Software Engineer at Example Corp. (2019–Present)
```

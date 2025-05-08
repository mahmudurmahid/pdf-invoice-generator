# 🧾 PDF Invoice Generator

The **PDF Invoice Generator** is a Python script that automatically generates structured PDF invoices from Excel files. The script processes invoice data stored in `.xlsx` files, generates a PDF with a table of items purchased, and adds company details and a logo to the final PDF. This tool is ideal for businesses and individuals who need to automate invoice creation from Excel data.

---

## 📑 CONTENTS

- [User Experience](#user-experience-ux)
  - [User Stories](#user-stories)
- [Design](#design)
  - [Page Structure](#page-structure)
  - [Typography](#typography)
- [Features](#features)
  - [Implemented Features](#implemented-features)
  - [Planned Improvements](#planned-improvements)
- [Technologies Used](#technologies-used)
  - [Languages](#languages-used)
  - [Libraries](#libraries-used)
- [Project Files](#project-files)
- [Installation & Usage](#installation--usage)
  - [How to Run](#how-to-run)
  - [Modifying the Input Files](#modifying-the-input-files)
- [Testing](#testing)
- [Credits](#credits)
  - [Code](#code)
  - [Acknowledgments](#acknowledgements)

---

## 🧠 User Experience (UX)

### User Stories

As a user, I want to:

- Convert Excel data into well-structured PDF invoices.
- Automatically generate PDFs with the invoice number and date from the filename.
- Customize the table with product details and totals easily.
- Include a company logo and footer for a professional appearance.

---

## 🎨 Design

### Page Structure

Each invoice PDF includes the following:

- **Invoice Header:** Displays the invoice number and date at the top.
- **Product Table:** Includes columns for product ID, name, amount, price per unit, and total price.
- **Total Sum:** Shows the sum of the total prices from all purchased items at the bottom of the table.
- **Footer:** Displays the total price sentence and company name with a logo.

### Typography

- **Font Family:** Times (classic serif font)
- **Invoice Header Font Style:** Bold, size 16
- **Table Font Style:** Regular, size 10
- **Footer Font Style:** Regular, size 10
- **Company Name Font Style:** Bold, size 14

---

## 🛠 Features

### Implemented Features

- ✅ Reads invoice data from `.xlsx` files in the `Invoices/` folder.
- ✅ Automatically generates PDF invoices with product details and totals.
- ✅ Displays the company name and logo on the invoice.
- ✅ Saves the generated PDFs in the `PDFs/` folder with names based on the original Excel file name.

### Planned Improvements

- 🔄 Add the option to include additional sections or custom notes on the invoice.
- 🔄 Enable dynamic date formatting for invoices.
- 🔄 Allow multiple languages for invoices.
- 🔄 Support for multiple file formats for input data (e.g., CSV, JSON).

---

## 💻 Technologies Used

### Languages Used

- Python 3.13

### Libraries Used

| Library    | Purpose                         |
| ---------- | ------------------------------- |
| `fpdf`     | PDF creation and formatting     |
| `pandas`   | Reading and parsing Excel files |
| `openpyxl` | Reading `.xlsx` Excel files     |
| `numpy`    | (Indirect via pandas)           |

---

## 📁 Project Files

```bash
.
├── main.py # Main script that creates the PDF
├── Invoices/ # Folder for input .xlsx invoice files
│ └── invoice123-2025-05-01.xlsx
├── PDFs/ # Folder where generated PDFs are saved
├── pythonhow.png # Company logo
├── requirements.txt # Python dependencies
└── README.md # Project documentation
```

## 🚀 Installation & Usage

### Prerequisites

Ensure Python 3 is installed. Then install required packages using:

```bash
pip install -r requirements.txt
```

### How to Run

Run the invoice generator by executing the main.py script:

```bash
python main.py
```

This will process all Excel files in the Invoices/ folder and generate corresponding PDF files in the PDFs/ folder.

### Modifying the Input Files

To customize the invoice:

- Place your .xlsx invoice files in the Invoices/ folder.
- Ensure the filename is in the format InvoiceNumber-Date.xlsx.
- Modify the contents of the Excel file:
- Columns: product_id, product_name, amount_purchased, price_per_unit, total_price.
- Save the file and rerun main.py to generate the updated PDF.

## ✅ Testing

Manual testing was conducted:

- Checked that the invoice header and footer render properly. ✔
- Validated that Excel input data is correctly parsed using pandas. ✔
- Verified the table displays product data correctly. ✔
- Ensured total prices are calculated and displayed correctly. ✔
- Confirmed the generated PDF opens correctly in standard PDF readers. ✔

## 🧾 Credits

### Code

- Built using open-source libraries fpdf, pandas, and openpyxl.

### Acknowledgments

- Thanks to the maintainers of fpdf, pandas, and openpyxl for their powerful and accessible libraries.

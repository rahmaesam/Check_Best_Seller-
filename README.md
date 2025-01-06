# Best Seller Validation Automation

This repository contains an RPA (Robotic Process Automation) project designed to automate the validation of "Best Seller" supplier information in a manufacturing dataset. The project uses UiPath to process Excel and PDF files and ensures accuracy by comparing data against a reference document.

## Features
- Reads data from an Excel file `Manufacturing_DATA_2024`.
- Calculates a new column `TOTAL` by multiplying `Price (USD)` and `Stock Quantity`.
- Reads the reference PDF file `ENG CODES` to validate "Best Seller" information.
- Compares the "Best Seller" status for each code in the Excel file with the reference PDF.
- Adds a `COMMENT` column in the Excel file to flag incorrect mappings with the note: "Incorrect Best Seller".

## Process Overview
1. Load the `Manufacturing_DATA_2024` Excel file.
2. Calculate the `TOTAL` column.
3. Extract data from the `ENG CODES` PDF file.
4. Compare the "Best Seller" status for each code.
5. Skip rows where the "Best Seller" is correct.
6. Add comments for rows where the "Best Seller" status is incorrect.

## Requirements
- UiPath Studio (Classic Activities enabled)
- Input Files:
  - `Manufacturing_DATA_2024.xlsx`
  - `ENG_CODES.pdf`

## Setup and Execution
1. Clone the repository.
2. Open the UiPath project in UiPath Studio.
3. Place the input files in the designated folder.
4. Run the process and review the updated Excel file.

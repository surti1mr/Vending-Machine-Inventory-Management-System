# Vending Machine Management System

ABAP Module Pool Program for Vending Machine Inventory Management

**Author:** Mayank Surti  
**Email:** surti1mr@cmich.edu  
**Course:** BIS657S ABAP Programming  
**Date:** December 8th, 2025

## Description

This is an ABAP module pool program (`Z129_PROJECT_PROGRAM`) that provides functionality for managing vending machines, products, students, stock levels, and usage logging. The system allows administrators to maintain machine data, product data, and student information, while also providing features for stock management, usage tracking, and reporting.

## Structure

```
├── Z129_PROJECT_PROGRAM          # Main module pool program
├── Includes/                      # Include files
│   ├── Z129_PROJECT_PROGRAM_TOP  # Global data declarations
│   ├── Z129_PROJECT_PROGRAM_O01  # PBO (Process Before Output) modules
│   ├── Z129_PROJECT_PROGRAM_I01  # PAI (Process After Input) modules
│   └── Z129_PROJECT_PROGRAM_F01  # Form routines
└── Screens/                       # Screen definitions
    ├── 0100                       # Initial screen
    ├── 0110                       # Screen 0110
    ├── 0120                       # Screen 0120
    ├── 0130                       # Screen 0130
    ├── 0140                       # Screen 0140
    ├── 0150                       # Screen 0150
    ├── 0160                       # Screen 0160
    └── 0170                       # Screen 0170
```

## Features

- Maintain Machine Data
- Maintain Product Data
- Maintain Student Data
- Update Stock Levels
- Log Student Usage
- Refill Report
- Stock Overview

## Requirements

- SAP ABAP Development Environment
- Required custom tables:
  - `Z129_STOCK`
  - `Z129_MACHINE`
  - `Z129_VEND_PROD`
  - `Z129_STUDENT`
  - `Z129_USAGE_LOG`

## Installation

1. Import the program and includes into your SAP system
2. Create the required custom tables if they don't exist
3. Activate the program

## Usage

### Execution

**T-code to execute the Project:** `Z129_PROJECT_PROGRAM`

**Pool module project name:** `Z129_PROJECT_PROGRAM`

Execute the program in transaction SE80 or SE38 using the T-code `Z129_PROJECT_PROGRAM`.

### Initial Screen

The initial screen displays 7 push buttons:

1. **Maintain Machine Data** - Displays all the data of Vending Machines
2. **Maintain Product Data** - Displays all the Products and includes an Add button to add products into the table
3. **Maintain Student Data** - Displays all available students and allows adding new entries
4. **Update Stock Level** - Allows updating stock levels for products in machines
5. **Log Student Usage** - Logs student purchases and updates stock
6. **Refill Report** - Generates reports for products that need refilling
7. **Stock Overview** - Displays stock overview for a specific machine

## Testing Documentation

### Test Case 1: Log Student Usage

**Objective:** Test the student usage logging functionality and stock update.

**Steps:**
1. Click on **Log Student Usage** button from the initial screen
2. This will redirect to a screen with input fields:
   - Student ID
   - Product ID
   - Machine ID
3. Enter `1` in every field (Student ID: 1, Product ID: 1, Machine ID: 1)
4. The readonly fields will automatically display:
   - Student Name
   - Product Name
   - Machine Building Name
   - Available stock in the machine
   - Price of the product
5. Click on **Log Usage** button
6. The system will:
   - Update the stock availability
   - Display a confirmation pop-up that the transaction was successful

**Expected Result:** Stock is updated and confirmation message is displayed.

---

### Test Case 2: Stock Overview

**Objective:** View stock availability for a specific machine with color-coded highlighting.

**Steps:**
1. Click on **Stock Overview** button from the initial screen
2. The screen will display a field for Machine ID
3. Enter Machine ID: `3` and hit Enter
4. The system will display:
   - Available stock of all products in that machine
   - Products highlighted based on availability (color-coded status)

**Expected Result:** All products in machine 3 are displayed with stock levels and appropriate highlighting based on availability.

---

### Test Case 3: Update Stock Level

**Objective:** Add stock to a machine for a specific product.

**Steps:**
1. Click on **Update Stock Level** button from the initial screen
2. Click on **Add Stock** button
3. A pop-up will appear asking for:
   - Machine ID
   - Product ID
   - Quantity
4. Enter the required information
5. Click **Check** button
6. The stock will be added to the system

**Expected Result:** Stock is successfully added to the specified machine and product.


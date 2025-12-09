# Z129 Project Program

ABAP Module Pool Program for Vending Machine Management System

## Description

This is an ABAP module pool program (`Z129_PROJECT_PROGRAM`) that provides functionality for managing vending machines, products, students, stock levels, and usage logging.

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

Execute the program `Z129_PROJECT_PROGRAM` in transaction SE80 or SE38.


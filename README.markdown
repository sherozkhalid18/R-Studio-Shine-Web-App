# Employee Data Management and Cleaning Tool

This repository contains a Shiny application designed for collecting and cleaning employee data. The application consists of two main components: an **Employee Information Form** for data collection and a **Data Cleaning Tool** for processing CSV files.

## Features

### Employee Information Form
- **Input Fields**: Collects employee details such as name, personal story, secret information, age, years of experience, contract duration, date of birth, vacation period, favorite programming languages, hobbies, and side job availability.
- **File Upload**: Allows uploading of resume or ID proof.
- **Interactive UI**: Includes submit, cancel, and home buttons with styled form sections.
- **Output**: Displays submitted data in a table format with a success message.

### Data Cleaning Tool
- **CSV Upload**: Supports uploading CSV files with customizable delimiter and row-skipping options.
- **Data Cleaning Options**:
  - Convert column names to snake_case.
  - Remove constant columns.
  - Remove rows with missing values (NAs).
- **Preview**: Displays raw and cleaned data previews with adjustable row counts.
- **Download**: Exports cleaned data as a CSV file.

## Prerequisites
- R (version 4.0 or higher)
- Required R packages:
  ```R
  library(shiny)
  library(tidyverse)
  library(readr)
  library(janitor)
  library(DT)
  library(shinyWidgets)
  ```

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/employee-data-tool.git
   ```
2. Install the required R packages:
   ```R
   install.packages(c("shiny", "tidyverse", "readr", "janitor", "DT", "shinyWidgets"))
   ```
3. Run the application:
   ```R
   shiny::runApp("app.R")
   ```

## Usage
1. **Employee Information Form**:
   - Fill in the form fields in the sidebar.
   - Upload a resume or ID proof if needed.
   - Click **Submit** to view the entered data in a table.
   - Use **Cancel** to reset the form or **Home** to return to the main page.

2. **Data Cleaning Tool**:
   - Upload a CSV file via the "Choose CSV File" input.
   - Specify a delimiter (leave blank to auto-detect) and rows to skip.
   - Adjust the number of preview rows using the up/down buttons.
   - Select cleaning options (snake_case, remove constant columns, remove NAs).
   - View raw and cleaned data previews in the respective tabs.
   - Download the cleaned data using the **Download Cleaned Data** button.

## File Structure
- `app.R`: Main Shiny application script containing both the Employee Information Form and Data Cleaning Tool.
- `README.md`: This file, providing an overview and instructions.

## Notes
- The application uses `shinyWidgets` for enhanced UI components like `prettyCheckbox`.
- The Data Cleaning Tool assumes CSV files are well-formatted; errors in file reading will trigger a notification.
- The Employee Information Form validates age input (18–55 years).

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing
Contributions are welcome! Please submit a pull request or open an issue for suggestions or bug reports.
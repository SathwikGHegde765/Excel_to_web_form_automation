# Excel_to_web_form_automation
# Excel Data to Web Form Automation with Power Automate Desktop

## Project Overview

This Power Automate Desktop project automates the process of transferring structured data from an Excel spreadsheet into a web-based form. It provides a robust solution for businesses or individuals who frequently need to input large volumes of data into online applications, surveys, or registration forms. By automating this repetitive task, the solution significantly enhances data entry speed, accuracy, and overall operational efficiency.

## Features

* **Automated Data Reading:** Reads input data from a specified Excel spreadsheet row by row.
* **Dynamic Web Form Population:** Automatically fills in fields on a target web form using data retrieved from Excel.
* **Browser Agnostic (Configurable):** Primarily configured for Google Chrome, but can be adapted for other browsers supported by Power Automate Desktop.
* **Form Submission:** Automates the clicking of submission buttons on the web form.
* **(Optional) Data Extraction:** Can be extended to extract confirmation messages or IDs from the web page after form submission.
* **(Optional) Excel Update:** Capability to write extracted data back to the original Excel file.

## Prerequisites

To run this automation, you will need:

* **Power Automate Desktop:** Installed on your Windows machine.
* **Microsoft Excel:** A valid license for Microsoft Excel (part of Microsoft 365 or stand-alone).
* **Web Browser:** Google Chrome (recommended for initial setup, but can be configured for Edge).
* **Source Excel File:** An Excel file (e.g., `InputData.xlsx`) containing the data to be input into the web form.
* **Target Web Form:** The URL of the web page with the form you intend to automate.

## Setup and Installation

1.  **Clone or Download:**
    ```bash
    git clone [https://github.com/YourUsername/excel-to-webform-automation.git](https://github.com/YourUsername/excel-to-webform-automation.git)
    cd excel-to-webform-automation
    ```
    (Replace `YourUsername` with your actual GitHub username and adjust the repository name if you change it.)

2.  **Open in Power Automate Desktop:**
    * Open Power Automate Desktop.
    * Go to `File` > `Import` > `Browse` and select the `.pad` file (e.g., `Excel_to_Web_Form_Automation.pad`) from the downloaded repository. Alternatively, you can simply double-click the `.pad` file to open it.

3.  **Prepare Excel Data:**
    * Locate the `InputData.xlsx` file (or your designated Excel file) in the repository.
    * Populate this file with your data. Ensure the column headers in your Excel file precisely match the names/labels of the fields on your target web form for easy mapping (e.g., if the web form has a field "Full Name", your Excel column could be "Full Name").
    * **Important:** Ensure the Excel file is **closed** before running the automation.

4.  **Configure Flow Paths and URLs:**
    * In Power Automate Desktop, open the `Excel_to_Web_Form_Automation` flow for editing.
    * **Excel File Path:** Review the "Launch Excel worksheet" action and update the path to your `InputData.xlsx` file if it's not in the same directory as the flow.
    * **Web Form URL:** Update the URL in the "Launch new Chrome" (or other browser) action to point to your specific target web form.
    * **UI Element Mapping:** For all "Populate text field on web page," "Select radio button on web page," "Press button on web page," and "Extract data from web page" actions, verify and re-capture the UI elements if the web form's structure has changed since the flow was last saved. This ensures the automation correctly interacts with the web elements.

## Usage

1.  **Ensure Prerequisites are Met:** Confirm Power Automate Desktop, Excel, and Chrome are installed, and your Excel data file is prepared and closed.
2.  **Run the Flow:** Click the "Run" (play) button in Power Automate Desktop.
3.  **Observe:** The automation will launch Chrome, navigate to the web form, read data from Excel row by row, fill the form fields, and submit the data.
4.  **Review Output:** If your flow is configured to write back to Excel or extract data, check the updated Excel file or the flow's variables for the output.

## File Structure

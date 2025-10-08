# n8n AI Prescription Processor

An n8n workflow that automates the processing of medical prescription images using AI and saves the structured data to Google Drive.

## Features

*   **Batch Processing:** Scans and processes all image files in a designated folder.
*   **AI Data Extraction:** Uses a Vision AI to extract prescription details into a structured JSON format.
*   **Dynamic Folder Creation:** Automatically creates `A-Z` and patient-specific folders in Google Drive.
*   **Duplicate Handling:** Creates numbered folders (e.g., `Patient_1`, `Patient_2`) if a folder already exists.
*   **Automatic Archival:** Moves processed images to an archive folder.

## Prerequisites

*   An n8n instance.
*   Google Account with API credentials.
*   Google Gemini (or other Vision AI) API credentials.
*   Three Google Drive folders: `Incoming`, `Processed`, and `Archive`.

## Setup

1.  **Import Workflow:** Import the `workflow.json` file into your n8n canvas.
2.  **Set Credentials:** Authenticate all Google Drive and AI nodes.
3.  **Update Folder IDs:** In the Google Drive nodes, replace the placeholder IDs with the actual IDs of your `Incoming`, `Processed`, and `Archive` folders.
4.  **Activate Workflow:** Save and activate the workflow.

## Usage

1.  **Upload:** Place one or more prescription images into your `Incoming` folder in Google Drive.
2.  **Execute:** Run the workflow manually or wait for its schedule to trigger.
3.  **Verify:** Check your `Processed` folder for the new JSON files and your `Archive` folder for the original images.

## Tech Stack

*   **Automation:** n8n
*   **AI Model:** Google Gemini (Vision)
*   **Storage:** Google Drive

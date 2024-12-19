# OCR-Based Medical Data Extraction Project

## Problem Statement
Health insurance companies must adhere to government regulations when processing claims. This requires extracting useful data from scanned images of patient details and prescriptions sent by hospitals or individual doctors.

Currently, companies like “Mr. X Data Analytics” rely on manual processes, leading to:

- Frequent errors.
- Inefficiency when handling a large volume of images, such as during a pandemic.
- Inability to meet the 24-hour turnaround requirement for data extraction.

## Solution
This project automates data extraction using Python, reducing manual effort while retaining human oversight for verification. This hybrid approach ensures both accuracy and efficiency.

## Technologies Used
- **Programming Language**: Python
- **Concepts**: OOP, Test-Driven Development
- **Libraries/Modules**:
  - pytesseract for OCR
  - OpenCV for image processing
  - pdf2image for converting PDFs to images
  - regex for pattern matching and data extraction
  - pytest for testing
- **Framework**: FastAPI (Backend API Hosting)
- **Frontend**: Streamlit (UI for interacting with the backend)

## Workflow
![Workflow](https://github.com/chaithra-03/OCR_data_extraction/raw/master/Resources/workflow.jpg)


### 1. PDF to Image Conversion
Using the pdf2image library, PDFs are converted into images for processing.

### 2. Image Processing
To improve data extraction accuracy, preprocessing is done using OpenCV:
- **Normal Thresholding**: Initial trials showed data loss in noisy images.
- **Adaptive Thresholding**: A better alternative, as it adjusts thresholds for sub-regions, resulting in higher accuracy.

<div style="display: flex;">
    <img src="https://github.com/chaithra-03/OCR_data_extraction/raw/master/Resources/filter_dark.jpg" width="300" style="margin-right: 40px;"/>
    <img src="https://github.com/chaithra-03/OCR_data_extraction/raw/master/Resources/adaptive_filter_dark.jpg" width="300"/>
</div>





### 3. Data Extraction
- **OCR**: Extracts raw data from images using pytesseract.
- **Regex**: Processes raw data to extract structured, meaningful information (e.g., names, addresses, medication details).

### 4. OOP Design
The program is structured using Object-Oriented Programming for modularity and maintainability.

### 5. Testing
Test-Driven Development (TDD) was followed, with pytest used to write and validate test cases for every functionality.

### 6. Frontend Integration
A user-friendly frontend was developed using Streamlit, allowing users to:
- Upload images or PDFs for data extraction.
- View and verify extracted data.
- Make corrections, if necessary, before submission.

## Benefits
- **Time Savings**: Automation reduces manual data entry time by 30 seconds per document, leading to significant cumulative savings.
- **Improved Efficiency**: Handles a larger workload without additional hiring.
- **Enhanced Accuracy**: A combination of automation and manual review minimizes errors.
- **Cost Effectiveness**: Reduces labor costs during high-demand periods.

## Result
The backend functionality, combined with the Streamlit frontend, allows for seamless integration into existing systems like those used by “Mr. X Analytics.” This solution automates data extraction, reducing manual effort while enabling human verification for accuracy.

[![Watch the demo](https://img.youtube.com/vi/VIDEO_ID/0.jpg)](https://github.com/chaithra-03/OCR_data_extraction/blob/master/Resources/Demo.mp4)




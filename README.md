# Production-Ready Rule-Based Data Extraction API

<img width="1536" height="1024" alt="ChatGPT Image Jan 14, 2026, 05_52_09 PM" src="https://github.com/user-attachments/assets/127ab7c7-720d-4694-a78f-1c256e41b025" />

## Problem Statement

Semi-structured lab report PDFs contain critical water quality data but arrive with inconsistent layouts and parameter naming. Manual copy-paste of 20+ values (pH, conductivity, dissolved solids, bacteria counts) into Excel is time-consuming, error-prone and doesn't scale as report volumes grow.

CLI-based automation tools require local environment setup and Python dependencies, limiting accessibility for non-technical users and creating deployment friction across teams.

## Technical Approach

* Converted existing CLI tool to end-to-end FastAPI REST endpoints: document upload, data extraction (JSON response) and Excel download  
* Supported batch upload with background task queuing for concurrent processing  
* Implemented rule-based parsers using pdfplumber and regex for semi-structured extraction  
* Stored synonym mapping rules in PostgreSQL for dynamic parameter normalisation  
* Defined field mapping for 20+ target parameters across varying report layouts  
* Enforced schema validation using Pydantic models with type checking and range constraints  
* Generated downloadable Excel files using openpyxl/pandas  
* Handled edge cases: multi-page reports, merged cells, inconsistent headers  
* Deployed to serverless cloud infrastructure with centralised log monitoring

## Skills

Python · FastAPI · PostgreSQL · pdfplumber · pandas · openpyxl · REST APIs · Background tasks · Batch processing · Rule-based extraction · Semi-structured data · Schema validation · Pydantic · SQLAlchemy · async/await · Serverless deployment · Log monitoring

## Challenges & Solutions

* Inconsistent semi-structured layouts → rule-based field detection with fallback patterns  
* Parameter name variations across labs → PostgreSQL synonym mapping for dynamic normalisation  
* Merged table cells breaking extraction → custom cell boundary detection logic  
* Invalid or out-of-range values → Pydantic schema validation with error reporting

## Quantifiable Business Impact

* 95% reduction in manual data entry time  
* 99% accuracy in data extraction  
* Batch upload with queuing enabling scalable multi-file processing  
* Dynamic synonym rules via database—no redeployment needed  
* One-click Excel download eliminating manual reformatting  
* Production-ready deployment with centralised log monitoring

## Client Review
<img width="655" height="292" alt="image" src="https://github.com/user-attachments/assets/2b96f9a6-ef61-4d68-852c-21a761329bda" />



# Workato Claims Intake Automation

## Project Overview

This project automates insurance claim processing using Workato.

The workflow reads new claim records from Google Sheets, validates the data, enriches records using a Lookup Table, parses claim details stored as JSON, creates records in a Workato Data Table, and updates the source sheet with processing results.

## Business Scenario

SecureLife Insurance receives claim submissions through a Google Sheet.

The objective is to:

* Validate submitted claims
* Assign claim adjusters automatically
* Parse incident information from JSON
* Store valid claims in a centralized data table
* Update the source sheet with processing status

## Technologies Used

* Workato
* Google Sheets
* Workato Lookup Tables
* Workato Data Tables
* JSON Parsing

## Workflow

Scheduler Trigger
↓
Read Claims from Google Sheet
↓
Validate Claim Data
↓
Parse Claim Details JSON
↓
Lookup Policy Information
↓
Create Record in Claims_Register Data Table
↓
Update Source Sheet Status

## Validation Rules

The claim is processed only when:

* Claim Status = Submitted
* Claimant Email exists
* Incident Date exists

Otherwise, the record is marked as Skipped.

## Error Handling

The workflow updates the source sheet with:

* Synced
* Skipped
* Failed

along with the appropriate remarks.

## Key Features

* Scheduled execution
* Data validation
* JSON parsing
* Lookup table enrichment
* Data table writeback
* Error handling
* Modular design using functions

## Learning Outcomes

* Workato Recipe Development
* Workato Functions
* Lookup Tables
* Data Tables
* JSON Parsing
* Automation Best Practices

## Author

Divya Borkar

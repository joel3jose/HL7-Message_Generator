# HL7 Message Generator Tool

A web-based tool designed to simplify HL7 message creation and testing for healthcare integration workflows.

## Purpose

This tool streamlines the process of creating HL7 messages for testing purposes, eliminating the need to manually construct complex HL7 message formats. It provides an intuitive interface for generating various HL7 message types used across different healthcare clients.

## Features

### Three Main Sections

1. **Menu Section**
   - Navigate between various client configurations
   - Quick access to different healthcare system integrations

2. **Input Section**
   - Fill in dynamic values for HL7 message fields
   - User-friendly forms for data entry
   - Supports multiple message types per client

3. **Output Section**
   - Multiple tabs displaying different HL7 message types
   - **Notes Tab**: Stores key values including:
     - Message Control Number
     - Patient ID
     - Patient Name
     - Location details
     - Useful for troubleshooting and tracking message details
   - **Network Tab**: Contains TCP/IP configuration details
     - IP addresses and port numbers for message delivery
     - Configuration for replicating client message flows

## Supported Clients

The tool currently supports the following healthcare system integrations:

1. AHS
2. Inspira IMG
3. Inspira UC
4. Inspira IMG & UC Covid Result Testing
5. Geisinger
6. Geisinger Merge
7. UPMC EU Inpatient Multicampus

## Example Workflow

**Inspira IMG Covid Result Testing**

This workflow demonstrates a typical use case requiring three HL7 message types:
- **SIU** (Scheduling Information Unsolicited)
- **ADT** (Admit, Discharge, Transfer)
- **ORU/MDM** (Observation Result/Medical Document Management)

## Message Delivery

Messages are sent using the **SmartHL7.Message.Sender** tool to the configured TCP/IP endpoints specified in the Network tab.

## Technologies Used

- HTML
- CSS
- JavaScript

## Known Limitations

The following improvements are planned for future development:

- Separate CSS, JS, and HTML files for better code organization
- Many HL7 segments are currently hardcoded
- Admit/discharge date-time calculation accuracy needs improvement
- Auto-complete functionality for field values
- Desktop application version (currently web-based)
- Database integration for value validation and duplicate checking
- Direct TCP/IP message sending without external tools
- JSON output generation for non-Mirth environments (Dev/QA)

## Installation

1. Clone this repository
2. Open the HTML file in a web browser
3. No additional dependencies required for basic functionality

## Usage

1. Select your client from the Menu Section
2. Fill in the required fields in the Input Section
3. Review the generated HL7 message in the Output Section
4. Use the Notes tab to verify key values
5. Reference the Network tab for TCP/IP configuration
6. Send messages using SmartHL7.Message.Sender tool

---

**Note**: This tool is designed for testing purposes. Ensure compliance with HIPAA and other healthcare data regulations when handling patient information.

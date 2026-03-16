# Hotel-Room-Booking-Automation-Using-n8n
This project explains how to create a Hotel Room Booking Form using n8n and automatically store the submitted booking details in Google Sheets.The automation collects booking information from users and records it in a spreadsheet for easy management.

Drive Link : https://drive.google.com/drive/folders/1QTV65v4JbnJChhw4R_pWJqlym8hrWT7E?usp=drive_link

## Introduction

This document explains how to create a Hotel Room Booking Form using n8n and automatically store the submitted booking details in Google Sheets.The automation collects booking information from users and records it in a spreadsheet for easy management.

## Workflow Overview

The workflow structure is:

On Form Submission
        ↓
   Google Sheets
   (Append Row)

 When a user submits the booking form, the data is automatically stored in Google Sheets.
 
## Step 1: Create a New Workflow

- Open your n8n dashboard.
- Click New Workflow.
- Rename the workflow as:
- Hotel Room Booking Automation
  
## Step 2: Create the Booking Form

- Add the On Form Submission node.
- Configure the form with the following fields:
- Field Name
- Field type
- Description
- Name
- Text
- Guest name
= Room Preference
- Dropdown
- Room type selection

-- Example room options:
Standard Room
Deluxe Room
Suite


This form allows guests to select their preferred room type.

## Step 3: Add Google Sheets Node

- Click the + button next to the On Form Submission node.
- Search for Google Sheets.
- Add the Google Sheets node.
- Set the operation to:
- Append Row
  
This will add a new row each time a booking form is submitted.

## Step 4: Connect Google Account

- In the Google Sheets node, create New Credentials.
- Log in using your Google account.
- Allow n8n to access your Google Sheets.

## Step 5: Create the Spreadsheet

Create a spreadsheet in Google Sheets with the following columns:

Name
Room Preference

## Step 6: Map the Fields

- Map the form fields to the spreadsheet columns.
- Form Field
- Google Sheets Column
  
Name
Name
Room Preference
Room Preference

## Step 7: Save and Publish the Workflow

Click Save.
Click Publish in the top right corner.
The workflow becomes Active.

Once active, the Production Form URL will work.

## Step 8: Test the Booking Form

Open the form URL and enter booking details.
Example:
Name
Room Preference
Alex
Deluxe Room

Click Submit.

## Step 9: Verify Data in Google Sheets

After submitting the form, open your spreadsheet.
You will see a new row added automatically.
Example result:
Name
Room Preference
Alex
Deluxe Room

Final Result
The hotel booking automation works as follows:
Guest fills booking form
       ↓
Form submitted to n8n
       ↓
n8n processes the data
       ↓
Booking stored in Google Sheets


## Conclusion

Using n8n, hotels can automate booking data collection efficiently. This automation ensures all booking information is stored safely in Google Sheets without manual entry.

# INTRODUCTION

I was asked by Microsoft to write a blog post on their Humans of IT series - https://techcommunity.microsoft.com/t5/humans-of-it-blog/guest-blog-6-ways-to-maintain-and-foster-your-tech-superpower/ba-p/1120971

At the end of this post, I decided that I needed to go further than write about it, I needed to do something.  This was my first foray into PowerApps and i had a vision of what it needed to do and I had the benefit of being on both sides of the coin.  Suffering from anxiety for the last 4 years or so and also having the ability to get up and running with Power Automate and PowerApps left me in a great position to be able to build this and share it for others.

Thanks for reading.

# mentalhealthcheckinpowerapp
This is a mental health check in application built in Microsoft PowerApps and Power Automate

Import the Power App ZIP file - MentalHealthCheckInApplication_20200126092403.zip

# Uploading and creating the Resources by Topic Area list:

1. Open the "resources by topic title.iqy" file and save as an XLSX document
2. Open IE as an administrator
3. Go to your sharepoint site
4. Go to Site Contents
5. Go to Settings Cog
6. Click Add an App
7. Search for "spreadsheet"
8. Click Import Spreadsheet
9. Name: "Resources by Topic Area" or Name: "Mental Health"
10. Choose file: resources by topic title.xlsx or mental health.xlsx
11. In the selcted range drop down select the only option avaialble
12. Click Import
13. The list will have been uploaded.

Do steps 1 - 13 above for "mental health.iqy" file

# Go to your Data Sources in the Power App

1. Remove the current Resources by Topic Area sharepoint connection
2. Click Connectors to expand
3. Click Sharepoint
4. Choose the Sharepoint connector for your tenant
5. Chose your Sharepoint in your tenant
6. Click the check box on "Resources by Topic Area"
7. Click Connect

# Go to the FurtherInformation page

1. Click on the 1st dropdown control "DropdownTopic" ensure Items object is set to "Sort(Distinct(ColResources,'Topic Name'),Result)"
2. Click on the 2nd dropdown control "DropdownOrganisation" ensure Items object is set to "Filter(ColResources,'Topic Name'=DropdownTopic.Selected.Result)"

# App Start

In the App Start config, remember to change the phone numbers for your Occupational Health and Third Party Support (if you have one.  They are currently set to 111111.

# THIS COMPLETES THE POWER APP SETUP


# Power Automate Setup:

1. Go to the Are you ok main flow
2. Select the Sharepoint site address for your tenant
3. Choose "Mental Health" for the list name
4. Associate the variables with the list columns




# TEST THE POWER APP

# AUTHOR DETAILS

Jon Russell

Https://Twitter.com/JonDoesFlow

Jon@jondoesflow.com

# USAGE

Anyone can use this application. You just need PowerApps, Power Automate as part of a Microsoft Office 365 subscription. 

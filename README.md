# AI-Automation-Portfolio
My AI Automation Projects 
AI Automations Portfolio
## Project 1: Autonomous AI Job Scout
Engineered a Python-based agent using Google Antigravity that orchestrates Google Gemini to evaluate and score scraped data against strict matching criteria.

Features: Telegram notifications and SQLite persistence.


## Project 2: Agentic RO Closure Agent
Developed two custom versions of automated auditors to handle high-volume maintenance records, enforcing complex business rules such as labor hour validation, automated parts-to-comment matching, and documentation of completed work order records.

1st Version: Perplexity Pro Browser
This initial workflow utilized the Perplexity Pro Browser to handle prompting and specific rule enforcement.

1.Workflow Steps:

Review All Sections: Check that each section/line is marked COMPLETE.

2.Validate Section Details: Confirm presence of comments and labor entries. Match parts to comments (with exceptions for "sending out for repair" or "good used parts").

3.Special Section Rule: For "TRAILER PM AND ANNUAL DOT INSPECTION," verify file attachments before closing.

4.Error Handling: Ignore informational popups and report missing items if requirements are not met.

5.Closure Action: Update Close Date to today and change status to CLOSED.


2nd Version: n8n Automation
Transitioned the logic to n8n to document closures and provide structured reporting for the company.

First Iteration: Mapping sections into individual nodes to ensure every rule is accounted for.

![AUDIT RO 1](<AI AUDIT 1.png>)


Second Iteration: Implementing an AI agent to handle the rules and logic more efficiently.

![Audit RO 2](<AI AUDIT 2.png>)


## Project 3: MCP Server Trigger
Created a Model Context Protocol (MCP) server from scratch that connects to Vapi. This system allows small businesses to manage appointments autonomously through a series of specialized tools.

![MCP Server Trigger](<MCP SERVER TRIGGER.png>)
Calendar Integration: Connects to Google Calendar API and google Sheets API to check availability, book events, and search for existing appointments.
Management Tools: Enables updating or deleting appointments directly via the scheduler.

## Core Tools:

Tool 1 : Call 'Client Lookup'
Client Lookup: Identifies new or existing customers to the database.

![TOOL 1 - CAll Client Look up](<TOOL 1.png>)

Tool 2 : New Client
CRM: Adds a new customer to the customer database.

![TOOL 2- New Client CRM](<TOOL 2.png>)

Tool 3 : Checking Availability
Uses a google calender API to check if a certain slot if free for a new appointment.

![TOOL 3- Checking Availability](<TOOL 3.png>)

Tool 4 : Book Event 
This tool is used to make the actual appointment and document it in the scheduler.

![TOOL 4 - Book Event](<TOOL 4.png>)

Tool 5 : Look up Appointment
This tool is called when needing to look up an existing appointment

![TOOL 5- Look up Appointment](<TOOL 5.png>)

Tool 6 : Update Appointment
This tool is used to update an existing appointment on the scheduler. If the caller wants to change a date or time it calls this tool.


![TOOL 6-Update Appointment](<TOOL 6.png>)


Tool 7 : Delete Appointment
This tool is called when the caller needs to delete an existing appointment. It finds it in the scheduler and then makes the deletion to it.

![TOOL 7- Delete Appointment](<TOOL 7.png>)


## Project 4: Digital Photo Automation
Automated a manual photo-processing workflow to handle resizing and watermarking, turning a manual 100-image task into an instantaneous process.

![PHOTO EDITOR](<PHOTO EDITOR.png>)

Workflow Logic:

Trigger: Monitor a Google Drive folder for new image uploads.

Processing: Automatically resize the image.

Branding: Apply custom logo and watermark.

Storage: Upload finished images to a dedicated "DONE" folder.

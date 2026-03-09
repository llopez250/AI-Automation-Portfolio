# AI-Automation-Portfolio
My AI Automation Projects 
AI Automations Portfolio
Project 1: Autonomous AI Job Scout
Engineered a Python-based agent using Google Antigravity that orchestrates Google Gemini to evaluate and score scraped data against strict matching criteria.

Features: Telegram notifications and SQLite persistence.

Repository: 

Project 2: Agentic RO Closure Agent
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
![AUDTI RO 1](AI AUDIT 1.PNG)
Second Iteration: Implementing an AI agent to handle the rules and logic more efficiently.

Project 3: MCP Server Trigger
Created a Model Context Protocol (MCP) server from scratch that connects to Vapi. This system allows small businesses to manage appointments autonomously through a series of specialized tools.

Core Tools:

Client Lookup & CRM: Identifies and adds new or existing customers to the database.

Calendar Integration: Connects to Google Calendar API to check availability, book events, and search for existing appointments.

Management Tools: Enables updating or deleting appointments directly via the scheduler.

Project 4: Digital Photo Automation
Automated a manual photo-processing workflow to handle resizing and watermarking, turning a manual 100-image task into an instantaneous process.

Workflow Logic:

Trigger: Monitor a Google Drive folder for new image uploads.

Processing: Automatically resize the image.

Branding: Apply custom logo and watermark.

Storage: Upload finished images to a dedicated "DONE" folder.

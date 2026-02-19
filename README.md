📌 TechChallenge

This repository TechChallenge-SKD-BK- contains an automated processing workflow titled TechChallenge defined as an n8n automation workflow. The workflow orchestrates file extraction from an AWS S3 bucket, processes them through an external API, and generates reporting—with email notifications and Google Sheets integration.

🚀 What This Project Does

The workflow in this repository automates the following high-level process:

Trigger Execution — Workflow starts manually or on schedule.

Fetch Files from S3 — Retrieves file metadata from a specified AWS S3 bucket.

Download Files — Downloads files for further processing.

Submit to External API — Calls an HTTP API to upload/extract data.

Write Results — Results are appended or updated to a Google Sheet.

Generate Email Report — Sends a summary of success/failure and performance metrics via email.

Manage Processing Logic — Includes logic nodes to track failures, compute throughput, and send notifications.

👉 The workflow components are implemented as n8n nodes, a low-code automation orchestration platform.

🧩 Main Files
File	Description
TechChallenge.json	The workflow definition for n8n (JSON export). Contains logic for processing S3 files, API calls, Google Sheets updates, and email notifications.
README.md	This documentation file.
📦 Architecture Overview

This automation uses the following systems:

n8n Workflow Engine – Orchestrates the end-to-end automation.

AWS S3 – Source bucket from which files are listed and downloaded.

External HTTP API – Processes each file and returns metadata about success/failure.

Google Sheets API – Stores results and metadata for tracking.

Gmail API – Sends email updates with processing summaries.

The workflow includes logic for batching, rate limiting, error breakdown, and performance metrics generation.
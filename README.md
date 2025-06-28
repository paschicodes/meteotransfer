# Data Transfer for iPhone Pythonista Scripts

## Overview
This repository is used to transfer a small animated GIF (`output.gif`) and a text string (`output.txt`) generated every minute by a Pythonista script running on an iPhone. The files are uploaded here via the GitHub API and fetched by another iPhone for real-time display and processing.

## Purpose
The repository acts as a free, cloud-based intermediary for transferring data between two iPhones over the internet, without requiring a local server or paid services.

## Files
- `output.gif`: A small animated GIF generated every minute.
- `output.txt`: A simple text string generated every minute.

## How It Works
1. A Pythonista script on the source iPhone generates `output.gif` and `output.txt` every minute and uploads them to this repository using the GitHub API.
2. A Pythonista script on the destination iPhone polls this repository every minute to download and display/process the latest files.
3. Files are publicly accessible via raw URLs (e.g., `https://raw.githubusercontent.com/<username>/data-transfer/main/output.gif`).

## Notes
- This is a public repository, so the GIF and text are visible to anyone. No sensitive data is stored here.
- The scripts run in Pythonista on iOS, using the `requests` module for API calls and `ui` module for displaying data.
- Updates occur every minute, ensuring near-real-time data transfer.

## Usage
- **Source iPhone**: Run a Pythonista script to generate and push files to this repository.
- **Destination iPhone**: Run a Pythonista script to fetch and display/process the files.
- See the respective scripts for implementation details (not stored in this repository).

## Limitations
- Files are overwritten every minute; no version history is maintained for old data.
- GitHub API rate limits apply (60 requests/hour unauthenticated, 5000/hour with a token), but usage stays well within these limits.
- Requires both iPhones to have internet access and Pythonista installed.

## License
This project is unlicensed and intended for personal use. The GIF and text files are generated dynamically and have no specific license.

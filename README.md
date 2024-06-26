# TCP Connections VirusTotal Query Script

This PowerShell script is designed to be used with Microsoft Defender for Endpoint Live Response Sessions. It queries TCP connections on an endpoint against the VirusTotal API to identify possible malicious addresses, including C2 servers and other unwanted connections.

## Features

- Retrieves active TCP connections on an endpoint.
- Queries each connection's IP address against the VirusTotal API.
- Logs results, indicating whether each IP is clean or potentially malicious.
- Includes the process ID (PID) associated with each connection.

## Prerequisites

- PowerShell
- VirusTotal API key

## Usage

1. Upload the script to the library in Microsoft Defender for Endpoint.

2. Use the script in Live Response sessions with the following command:
    ```sh
    run script-name.ps1 -parameters "-filePath <File Path>"
    ```

   Replace `<File Path>` with the path where you want to save the output file.

## Example

```sh
run script-name.ps1 -parameters "-filePath C:\path\to\output.txt"

# FTP (File Transfer Protocol)

## What is FTP?
FTP is a protocol used to transfer files between a client and a server over a network.

## Common Uses
- Uploading files to a web server
- Downloading files from a server
- Transferring large files within a network

## FTP in Wireshark
- FTP uses two ports:
  - **Port 21**: For control commands like login, upload, and download.
  - **Port 20**: For data transfer.

- FTP traffic can be filtered in Wireshark using the `ftp` or `ftp-data` display filters.<img width="564" alt="Capture" src="https://github.com/user-attachments/assets/49f3d675-9b71-42d1-996a-0bbf3409b95f">


## Wireshark Filters for FTP
- `ftp`: Show all FTP control traffic.
- `ftp-data`: Show data transfer packets.
- `ftp.request.command == "USER"`: Filter for username.
- `ftp.request.command == "PASS"`: Filter for password.

## Example
When capturing FTP traffic:
- Look for packets with commands like `USER`, `PASS`, `RETR`, and `STOR`.
- Example Info column: `USER admin` or `PASS 12345`.

## Useful Commands
1. Filter for FTP login attempts:

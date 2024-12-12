# FILE-SHARING-HTTP-SOCKET
This project demonstrates how to create a simple HTTP server using Python and generate a QR code for accessing the server. The QR code allows users to easily open the server's IP address in a browser by scanning it.

Features

HTTP Server: Hosts files on a specified port using Python's built-in HTTP server.

Dynamic QR Code Generation: Generates a QR code that encodes the server's IP address and port.

Cross-device Access: Access the server from any device by scanning the QR code.

Desktop Integration: Automatically serves files from the user's Desktop folder.

Prerequisites

Ensure you have the following installed:

Python 3.x

pyqrcode module

pypng module

You can install the required modules using:

pip install pyqrcode pypng

How It Works

The script determines the user's Desktop directory and serves files from there.

It identifies the local IP address of the machine and assigns a port number (default: 8010).

It generates a QR code containing the server's URL (e.g., http://192.168.1.100:8010).

The server runs continuously, allowing access to the files from the browser or by scanning the QR code.

How to Use

Clone the repository or copy the script to your local machine.

Run the script using Python:

python script_name.py

Open the generated QR code (saved as myqr.svg) to scan it using a mobile device or open the displayed URL in your browser.

The terminal will display the port and IP address information for manual access if needed.

Code Explanation

Modules Used:

http.server, socket, and socketserver: For handling the HTTP server and networking.

pyqrcode and png: For generating the QR code.

webbrowser: To open the generated QR code in a browser.

os: For accessing system paths and environment variables.

Key Variables:

PORT: Port number for the HTTP server (default: 8010).

desktop: The Desktop directory path where files are served.

IP: The server's URL with IP address and port.

Workflow:

Sets up the HTTP server to serve files from the Desktop.

Generates a QR code with the server's URL and saves it as myqr.svg.

Opens the QR code in the default browser for easy access.

Prints server details in the terminal.

Example Output

Terminal Output:

serving at port 8010
Type this in your Browser http://192.168.1.100:8010
or Use the QRCode

QR Code:

The generated QR code can be scanned to open the server's IP address directly.

Notes

Ensure that the PORT value is not being used by another application.

The script assumes you have OneDrive configured; adjust the Desktop path as needed for other systems.

Use the script on a network where devices can communicate with each other (e.g., same Wi-Fi network).

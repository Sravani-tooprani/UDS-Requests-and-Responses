# UDS-Requests-and-Responses
This script processes automotive diagnostic messages, handling service requests and responses.

# Variables:
msg_res (0x601): Stores responses.
msg_req (0x701): Stores requests.

# Functionality:

# Positive Responses:
Listens for 0x701 messages.
Handles 0x10 0x01, 0x10 0x02, 0x10 0x03 requests with 0x50 responses.
Sends 0x7F 0x10 0x12 for invalid subfunctions.
Sends 0x7F <Service ID> 0x11 for unknown service IDs.

# Negative Responses (Key Triggers):
'a': Default session (0x10 0x01).
'b': Programming session (0x10 0x02).
'c': Extended session (0x10 0x03).
'd': Invalid subfunction (0x10 0x07).
'e': Invalid Service ID (0x98 0x01).

# Usage:
Run the script.
Send 0x701 messages.
Use keys ('a' to 'e') to send diagnostic requests.

# pyprint
Start print jobs by sending an email to your raspberry pi. 
Pyprint uses the python library impaplib to cycle through the last 5 messages in your the inbox. 
Email attachments from trusted senders will be downloaded and printed using the CUPS printing service. 
After downloading the attachment, the email is moved to the ‘Deleted’ folder.
It is recommended to add pyprint.py to your crontab to run every minute.
 
Pyprint looks for the following files in the installation directory:
* credentials: Contains the credentials of the email account in the following format
    + line 1: host e.g. ‘Outlook.office365.com’
    + line 2: username
    + line 3: password (unencrypted) 
* whitelist: Contains a list of trusted email addresses

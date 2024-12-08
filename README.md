# Automated Email Sender with PDF Attachment

This Python script automates sending emails in bulk with a PDF attachment, using Gmail's SMTP service. It is designed to handle batching, delay management, and avoids triggering Gmail's spam detection by mimicking natural sending behavior.

---

## Features

- **Bulk Email Sending**: Send emails to multiple recipients in a single execution.
- **Customizable Email Content**: Define the email subject, body (HTML format), and a PDF attachment.
- **Batch Management**: Sends emails in configurable batches to avoid exceeding Gmail's sending limits.
- **Randomized Delays**: Adds random delays between emails and batches to mimic human behavior.
- **Error Handling**: Provides meaningful error messages and ensures resources are properly cleaned up.

---

## Prerequisites

- **Python Environment**: Ensure Python 3.6 or later is installed on your machine.
- **Required Libraries**:
  - `smtplib`
  - `email`
  - `time`
  - `random`
- **Gmail Account**:
  - Enable *App Passwords* and generate one for this script.
  - If unavailable, enable *Less Secure Apps* in your Gmail account settings.

---

## Setup Instructions

1. Clone or download this repository.
2. Open the script and update the **User Configuration** section:
   - Replace `SENDER_EMAIL` with your Gmail address.
   - Replace `APP_PASSWORD` with your Gmail App Password.
   - Customize the email body, subject, sender details, and the path to the PDF file you want to attach.
3. Add recipient emails to the `email_string` variable in a comma-separated format.
4. Run the script in your Python environment.

---

## Usage

1. **Run the script**:
```python email_sender.py```
2. The script will:
- Connect to Gmail's SMTP server.
- Send emails in batches with random delays between emails.
- Provide logs in the console for sent emails and any errors encountered.

---

## How to Generate a Gmail App Password

1. Log in to your Google Account.
2. Go to **Security** > **App Passwords**.
3. Select the app and device you’re generating the password for.
4. Copy the generated password and paste it into the `APP_PASSWORD` variable in the script.

---

## Notes

- **Email Limits**: Gmail has sending limits (e.g., 500 emails/day for regular accounts). Ensure your batch size and total email count comply with these limits.
- **Privacy**: Keep your Gmail credentials secure and do not share the script with sensitive information.

---

## Known Issues

- Some email addresses may reject the email if their servers identify the email as spam. To avoid this, use professional email-sending platforms if you need higher reliability.
- Ensure the PDF attachment path is valid; otherwise, the script will fail to attach the file.

---


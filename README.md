# 📧 AWS Lambda Email Sender with Amazon SES

This project is a minimal AWS Lambda function written in **Python 3.11** to send emails using **Amazon Simple Email Service (SES)**. It's ideal for basic notification tasks such as contact form submissions, booking confirmations, or admin alerts.

---

## 🚀 Features

- Sends plaintext email via Amazon SES
- Lightweight and minimal
- Works in SES sandbox mode
- Easily extendable for HTML emails, templates, or mass mailers

---

## 🧰 Prerequisites

Before deploying the Lambda function, ensure:

1. **AWS SES setup**
   - ✅ Your `Source` and `ToAddresses` emails are verified in SES (required in sandbox mode)
   - ✅ You are using the correct SES region

2. **IAM Permissions**
   - Your Lambda execution role must have permission to use SES:
     ```json
     {
       "Effect": "Allow",
       "Action": "ses:SendEmail",
       "Resource": "*"
     }
     ```

3. **Lambda Settings**
   - Runtime: Python 3.11
   - Timeout: at least 10 seconds
   - Environment: No special variables needed unless customising

---

## 📦 File Structure

```plaintext
send_email_lambda/
├── lambda_function.py  # Core Lambda handler code
├── README.md           # Project documentation

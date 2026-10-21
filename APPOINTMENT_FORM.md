# Appointment Form — How It Works

## Overview

The Book Appointment form on the website is connected to **Formspree** (`https://formspree.io/f/mwvyzora`). When a customer submits the form, you receive an email with all their details.

## What Happens When a Customer Submits

1. Customer fills out the form and clicks **Confirm Appointment**
2. A success message appears on the page
3. You receive an email from Formspree that looks like this:

```
Subject: New Appointment Request — Tabuco Dental Clinic

first_name:     John
last_name:      Doe
email:          john@example.com
phone:          (555) 987-6543
service:        Teeth Whitening
preferred_date: 2026-05-20
notes:          I'd like an afternoon slot please.
```

4. You **manually call the customer back** using the phone number in the email to confirm the appointment.

## Form Fields Collected

| Field | Description |
|---|---|
| First Name | Customer's first name |
| Last Name | Customer's last name |
| Email Address | Customer's email (required) |
| Phone Number | Customer's contact number |
| Service Needed | Type of dental service requested |
| Preferred Date | Date the customer prefers |
| Additional Notes | Any special requests or concerns |

## Formspree Details

- **Endpoint:** `https://formspree.io/f/mwvyzora`
- **Dashboard:** https://formspree.io (login to view all submissions)
- **Free plan limit:** 50 submissions/month

## Future Upgrades (Optional)

| Feature | How |
|---|---|
| SMS alert to your phone when someone books | Twilio integration |
| Auto-reply confirmation email to patient | Formspree paid plan |
| Save appointments to a spreadsheet | Formspree + Google Sheets integration |

## Troubleshooting

- **Not receiving emails?** Check your spam folder or log in to formspree.io to view submissions directly.
- **First submission** — Formspree sends a one-time verification email. Click the link to activate the form.
- **Form not submitting?** Make sure the server is running (`python3 -m http.server 8080`).

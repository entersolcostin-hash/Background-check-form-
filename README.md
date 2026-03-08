# Kennective Care - Background Check Form

A web-based background check form for Kennective Care applicants, hosted on GitHub Pages and powered by [Formspree](https://formspree.io) for email delivery.

## What the Form Collects

- **Personal Details** – First name, middle name(s), surname, date of birth, and National Insurance number
- **5-Year Address History** – Current address plus the ability to dynamically add previous addresses
- **Driving Licence Uploads** – Front and back of a valid UK driving licence (photo or PDF)
- **Declaration** – Applicant consent for DBS and right-to-work background checks

Completed submissions are emailed to **entersolcostin@gmail.com**.

---

## Setup Instructions

### 1. Set Up Formspree

1. Go to [https://formspree.io](https://formspree.io) and create a free account.
2. Click **New Form** and enter `entersolcostin@gmail.com` as the email address to receive submissions.
3. Copy the **Form ID** shown (e.g. `xabcdefg`).
4. Open `index.html` and replace `YOUR_FORM_ID` in the form `action` attribute with your actual form ID:

   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" ...>
   ```

   becomes, for example:

   ```html
   <form action="https://formspree.io/f/xabcdefg" ...>
   ```

5. Commit and push the change to GitHub.

### 2. Enable GitHub Pages

1. Go to your repository on GitHub.
2. Click **Settings** → **Pages**.
3. Under **Source**, select the **main** branch and click **Save**.
4. GitHub Pages will deploy the site automatically. This may take a minute or two.

### 3. Access the Live Form

Once Pages is enabled, the form is available at:

```
https://entersolcostin-hash.github.io/Background-check-form-/
```

Share this link with applicants to fill out the form.

---

## Security & Privacy Notes

- All form data is transmitted to Formspree over **HTTPS** (encrypted in transit).
- Formspree stores submissions on their servers. Review [Formspree's Privacy Policy](https://formspree.io/legal/privacy-policy) for data handling details.
- The **free Formspree tier allows up to 50 submissions per month**. If you expect more volume, consider upgrading to a paid plan at [formspree.io/pricing](https://formspree.io/pricing).

---

## File Structure

```
├── index.html       # Main background check form
├── thankyou.html    # Confirmation page shown after successful submission
└── README.md        # This file
```

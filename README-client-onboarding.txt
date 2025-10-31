
CLIENT ONBOARDING FORM — QUICK SETUP

Files:
1) onboarding-emailjs.html — Sends submissions (including signature image) via EmailJS. No server needed.
2) onboarding-formspree.html — Sends submissions to your email via Formspree. No server needed.

A) EMAILJS (recommended: rich email + embedded signature)
   1. Go to https://www.emailjs.com/ and create a free account.
   2. Add an Email Service (e.g., Gmail/Outlook/SMTP) and note your SERVICE ID.
   3. Create an Email Template:
      - Add variables: firstName, lastName, email, phone, service, notes, signature_png
      - In the email body, include {{signature_png}} inside an <img src="{{signature_png}}"> tag to see the signature.
   4. Get your PUBLIC KEY.
   5. Open onboarding-emailjs.html and replace:
        const EMAILJS_PUBLIC_KEY = "YOUR_PUBLIC_KEY";
        const EMAILJS_SERVICE_ID = "YOUR_SERVICE_ID";
        const EMAILJS_TEMPLATE_ID = "YOUR_TEMPLATE_ID";
   6. Open the file in your browser and submit a test.

B) FORMSPREE (fastest)
   1. Go to https://formspree.io/ and create a free account.
   2. Create a new form, copy its form ID (e.g., xwkgqyle).
   3. Open onboarding-formspree.html and replace:
        const FORMSPREE_ID = "YOUR_FORM_ID";
   4. Open the file in your browser and submit a test.
   *This version uploads the signature as signature.png alongside the other fields.

C) PUT ONLINE (optional)
   - Netlify: drag-and-drop the HTML file into a new site.
   - GitHub Pages: put the file in a repo and enable Pages.

D) GOOGLE FORM VERSION (steps)
   1. Create a new Google Form with fields: First name, Last name, Email, Phone, Service Required, Additional Notes.
   2. Install a signature add-on (search “Signature” in the add-ons store) and insert a Signature item.
   3. Turn on “Collect email addresses” and enable response notifications.
   4. Link responses to a Google Sheet (for record-keeping).
   5. (Optional) Use an add-on like Form Notifications to email you a copy of each submission automatically.

E) JOTFORM VERSION (steps)
   1. Create a new form > Start from scratch > Add fields for: First name, Last name, Email, Phone, Service Required, Additional Notes.
   2. Add the “E-Signature” widget.
   3. Settings > Emails > Add an “Email Notification” to receive submissions.
   4. Publish > Share the link. Jotform stores the signature image and responses automatically.

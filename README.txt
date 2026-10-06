# Masjid Sarkare Do Alam ﷺ — Imam Voting Portal

## Files
- index.html — public voting page
- admin.html — admin dashboard
- Code.gs — Google Apps Script backend
- README.txt — setup guide

## Google Sheets setup
1. Create a new Google Sheet.
2. Extensions → Apps Script.
3. Paste Code.gs into the editor.
4. Change ADMIN_PIN from 4826 to your own 4-digit PIN.
5. Run `setup()` once and authorize it.
6. Deploy → New deployment → Web app.
7. Execute as: Me
8. Who has access: Anyone
9. Copy the Web App URL.
10. Put the URL in both index.html and admin.html by replacing:
   PASTE_YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL_HERE

## Important voting logic
- Mohammad Chand: submitted directly as APPROVED.
- Dawate Islami Hazrat: requires a reason of at least 30 characters and is stored as PENDING_REVIEW.
- Only an authenticated admin can approve/reject those submissions.
- Only APPROVED votes appear in the public totals.
- A mobile number can submit only one non-rejected vote.
- The backend does not automatically decide whether a person's statement is "genuine"; an authorized human/admin reviews it.

## Security/privacy notes
- Replace the demo PIN immediately.
- Restrict access to the Google Sheet itself.
- The public page displays totals, not voter names/mobile numbers.
- For a real public deployment, consider adding HTTPS-only hosting, stronger admin authentication, rate limiting, CAPTCHA, and a clear privacy notice/consent statement.


## Branding
Public and admin pages are bilingual (Hindi + English) and include © 2026 All Rights Reserved, Designed by E-Tech, Founder: MOHD SOHAIL, Contact: 7240610313.

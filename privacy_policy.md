# Privacy Policy for JARVIS AI Assistant

**Effective Date:** November 16, 2026  
**Last Updated:** November 16, 2026  

---

## 1. Overview
JARVIS ("the Application", "we", "us") is an open-source, local autonomous AI desktop companion and system assistant. We prioritize your privacy above all else. This Privacy Policy details how JARVIS accesses, processes, and protects your data when integrating with third-party services, specifically Google APIs including Gmail.

---

## 2. Information We Access
When you connect your Google account to JARVIS, the application requests access to specific Google OAuth 2.0 scopes strictly to carry out your direct voice and chat instructions:

- **`https://www.googleapis.com/auth/gmail.readonly`**: Used solely to read and search emails from your inbox when you request email summaries or search queries.
- **`https://www.googleapis.com/auth/gmail.compose`**: Used solely to draft and prepare emails upon your command.
- **`https://www.googleapis.com/auth/gmail.send`**: Used solely to send emails that you have explicitly instructed JARVIS to dispatch.

---

## 3. How Your Data Is Stored and Handled

### 100% Local Storage
- **Local Credentials**: Your Google OAuth credentials (`credentials.json`) and access tokens (`token.json`) are stored exclusively on your local computer in the JARVIS project directory.
- **No Third-Party Transmission**: JARVIS does not operate any centralized backend, telemetry servers, or cloud databases. Your email contents, message snippets, recipient addresses, and authentication tokens are never transmitted to, stored on, or inspected by any third-party server or developer server. All API requests travel directly between your machine and official Google servers (`https://*.googleapis.com`).

### No AI Model Training on Private Data
- Your personal emails and Google account data are **never** used to train generalized artificial intelligence or machine learning models.
- Temporary email summaries injected into runtime prompts during active sessions exist only in volatile local memory during your request lifecycle.

---

## 4. Google API Services User Data Policy (Limited Use)
JARVIS’s use and transfer of information received from Google APIs adheres to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the **Limited Use** requirements:

1. **Human Oversight**: No human will read your email data unless:
   - You provide affirmative agreement for specific messages (such as reviewing email previews in the UI),
   - It is necessary for system security (e.g., investigating a bug locally),
   - It is required by applicable law.
2. **Advertising**: JARVIS does not use or transfer your email data for serving advertisements, retargeting, personalized advertising, or market research.
3. **Restricted Transfer**: JARVIS will not transfer your Google user data to any external parties, except as required to fulfill the local user-directed email functionality or comply with legal requirements.

---

## 5. User Control and Data Revocation
You retain total control over your Google integration:

- **Revoke via JARVIS**: Open **Settings** → **Gmail Integration** → click **Revoke Access**. This immediately deletes your local `token.json`.
- **Revoke via Google Account**: You can disconnect JARVIS at any time from your Google Account settings:
  [https://myaccount.google.com/permissions](https://myaccount.google.com/permissions)

---

## 6. Contact & Open Source Inquiries
If you have questions regarding this Privacy Policy or JARVIS's data practices, please create an issue on the project repository or contact the local system administrator.

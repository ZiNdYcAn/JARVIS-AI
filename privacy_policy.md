# Privacy Policy for JARVIS AI Assistant

**Effective Date:** November 19, 2026  
**Developer Version:** Current Developer Release  

---

## 1. Introduction and Core Philosophy

JARVIS ("the Application", "the Software", "we", "us") is an autonomous, local-first artificial intelligence assistant that operates directly on your personal computer.

We believe that your personal workstation is your most private space. JARVIS is architected from the ground up around **Local-First Data Sovereignty**:
* **No Developer Telemetry:** We do not operate developer tracking servers, centralized usage databases, or diagnostic telemetry collectors.
* **100% Local Storage:** Your personal notes, files, session memory, call logs, and credentials are saved directly on your local computer's storage drive.
* **No Public AI Model Training:** Your private documents, screen contents, emails, and conversation logs are never used to train generalized artificial intelligence models.

This Privacy Policy explains with exhaustive precision every category of data JARVIS collects, observes, records, processes, and transmits during its operation.

---

## 2. Exhaustive Categories of Data Collected & Processed

### 🎙️ A. Audio & Voice Data
1. **Computer Microphone Audio:**
   * **When Active:** JARVIS captures audio from your computer's microphone **only** when its visual desktop interface (HUD) is actively displayed on your screen, or when wake-phrase monitoring is enabled.
   * **Smart Privacy Muting:** When the visual interface is closed or minimized to the background, your computer's microphone input is **completely bypassed and muted**. JARVIS will not listen to or capture room audio while operating silently in the background.
2. **Mobile Companion Microphone Audio:**
   * During an active two-way phone call between your smartphone and JARVIS, audio from your phone's microphone is captured in real time to enable spoken dialogue.
3. **Voice Transcripts & Utterances:**
   * Spoken audio from your microphone or phone is processed into text solely to understand your commands.
4. **Wake-Phrase Detection:**
   * Listens in a temporary rolling audio buffer for activation phrases (such as *"Jarvis"* or *"Jarvis stop"*). Audio in this temporary buffer is immediately overwritten and never saved to disk.

---

### 👁️ B. Screen & Visual Data
1. **Monitor Screenshots & Visual Capture:**
   * When asked to assist with desktop workflows, inspect open documents, or verify that a task completed successfully, JARVIS captures visual screenshots of your active display monitors.
   * Visual elements (buttons, menus, input boxes, and displayed text) are analyzed to execute the requested automation.
2. **Real-Time Remote Screen Sharing:**
   * When you explicitly request screen sharing from your mobile companion app, JARVIS captures and streams a live video feed of your computer monitor directly to your paired phone.
   * Screen sharing is active only during your requested session and ceases immediately upon disconnection or when you command JARVIS to stop.

---

### 📷 C. Webcam & Facial Data (Optional)
1. **User Presence & Fatigue Detection:**
   * If enabled, JARVIS periodically inspects your connected webcam to detect whether a user is seated in front of the computer, adapting greetings and conversational tone accordingly.
2. **Biometric Face Recognition:**
   * When identity verification is enabled in settings, JARVIS uses facial geometric embeddings to match your face against your locally enrolled reference photographs.
   * **Complete User Disablement:** Face recognition can be completely disabled in the Settings menu at any time. When disabled, the camera vision system does not start, and voice commands are accepted without facial authentication.
   * **Zero Cloud Face Processing:** Facial feature vectors are processed entirely on your local CPU and are never sent over the internet.

---

### 👤 D. Personal Identity & Profile Data
1. **Username & Preferred Identity:**
   * Stored locally in `username.txt`. Used to customize greetings, voice prompts, and identity labels across the system.
2. **Personal Profile & Hardware Context:**
   * Stored locally in `user_personal_info.txt` (supports up to 5,000 words). Contains personal contact details, background notes, family member names, or system notes provided by the user to assist in filling forms or answering questions.
3. **User Preferences & Habits:**
   * Stored locally in `user_preferences.txt` and `user_preference.txt` (supports up to 5,000 words). Records your preferred software applications, operating habits, and conversational preferences.
4. **AI Personality Directives:**
   * Stored locally in `jarvis_personality.txt` (50 to 200 words). Defines the tone, brevity, and communication style of the assistant.

---

### 🧠 E. Long-Term Memory & Operational History
1. **Raw Session Memory (`memory.txt`):**
   * Records your past commands, actions executed, error retry counts, and final outcomes.
   * Used locally to maintain context across restarts so JARVIS remembers past actions and instructions.
2. **AI-Compressed Memory Summaries:**
   * When you choose to use the *"Compress memory"* feature, the raw contents of `memory.txt` are sent to your configured AI engine to produce a consolidated, high-signal narrative paragraph (between 100 and 500 words).
   * The compressed summary is presented in a preview window where you retain absolute discretion to either replace `memory.txt` or keep your full historical log.
3. **Memory Erasure:**
   * Clicking *"clear memory"* permanently wipes `memory.txt` from disk instantly.

---

### 📧 F. Electronic Mail & Communication Data (Gmail Integration)
When you connect your Google account to enable email automation, JARVIS accesses your email data strictly in accordance with your explicit voice and scheduled instructions:
1. **Inbox Search & Retrieval (`gmail.readonly`):**
   * Accesses email message subjects, sender names, recipient addresses, dates, and message body snippets to summarize your inbox or search for specific emails.
2. **Drafting Messages (`gmail.compose`):**
   * Creates draft emails upon your command.
3. **Dispatching Outbound Messages (`gmail.send`):**
   * Sends emails that you have explicitly verified and confirmed.
4. **Contact Aliasing:**
   * Maps colloquial names (such as *"Mom"*, *"Team Lead"*, or *"Alex"*) to verified email addresses stored in your local configuration.
5. **Local Authentication Tokens:**
   * Google OAuth client credentials (`credentials.json`) and authorized tokens (`token.json`) are stored exclusively on your local computer.

---

### 📞 G. Phone Calling & Mobile Companion Telemetry
1. **Call Records & Metadata:**
   * For every voice call between your phone and JARVIS, the system records:
     * Who initiated the call (Jarvis or User),
     * The reason or topic of the call,
     * Exact date and timestamp,
     * Call answer status and duration,
     * Who terminated the call.
2. **Spoken Dialogue Transcripts:**
   * Every turn spoken by the user and by JARVIS during a call is recorded verbatim in continuous local text files (`call_logs/<topic>.txt`).
   * A temporary working transcript (`temp_call_log.txt`) exists during active calls and is finalized immediately upon hangup.
3. **Device Pairing & Access Tokens:**
   * Stored in `trusted_devices.json`. Records paired mobile device names, cryptographic access tokens, and temporary 6-digit registration codes to ensure only your authorized smartphone can communicate with your PC.

---

### ⚙️ H. Hardware & System Telemetry
1. **Live Hardware Telemetry:**
   * Periodically monitors battery percentage, AC power connection status, master speaker volume, display brightness level, connected Wi-Fi network name (SSID), and paired Bluetooth devices.
2. **System Hardware Profile (`pc_analysis.txt`):**
   * Inspects CPU architecture, total RAM capacity, GPU models, disk space, and Windows operating system version to optimize local AI execution and answer system questions.
3. **Machine Identification:**
   * A cryptographic hash derived from local hardware components is used strictly to bind local licenses and device pairing tables to your physical machine.

---

### ⏰ I. Scheduled Tasks & Automation Triggers
1. **Task Schedules (`scheduled_tasks.json`):**
   * Records task titles, custom instruction prompts, target run dates and times, recurrence rules, and completion history.
   * Monitored 24/7 by the local background service to trigger automations even when the visual desktop overlay is hidden.

---

## 3. Data Storage, Transmission & Security Architecture

### Local-First Storage
* **Zero Cloud Databases:** Every log, transcript, audio recording, preference file, and credential token mentioned in this Policy resides strictly on your local PC storage drive within the application's root directory.
* **No Remote Analytics:** JARVIS does not include third-party advertising SDKs, tracking pixels, or diagnostic telemetry collectors.

### External Data Transmission
Data leaves your local computer **only** in the following strictly defined operational scenarios:
1. **Direct Communication with AI Providers:** Spoken text prompts, screen descriptions, memory compression requests, and email summary queries are transmitted directly from your computer to your configured AI service provider (e.g., Google Gemini API) over encrypted HTTPS/TLS channels using your personal API key.
2. **Direct Communication with Google Mail:** Email search and dispatch queries travel directly between your computer and official Google servers (`https://*.googleapis.com`) using your personal OAuth token.
3. **Direct Peer-to-Peer Mobile Connection:** Spoken voice call audio, text messages, and screen frames transmitted between your PC and your mobile phone travel over your local Wi-Fi network or an encrypted virtual peer-to-peer network connection. No intermediary server stores or inspects call audio.

---

## 4. Google API Services User Data Policy Compliance

JARVIS's access, use, and transfer of information received from Google APIs adheres strictly to the **Google API Services User Data Policy**, including the **Limited Use** requirements:

1. **No Human Reading:** No human will ever read your email data unless:
   * You provide explicit, affirmative agreement for specific messages (e.g., reviewing an email preview in the UI),
   * It is necessary for system security (investigating a bug locally on your own machine),
   * It is required by applicable law.
2. **No Advertising:** JARVIS never uses or transfers your email data for serving advertisements, retargeting, personalized advertising, or market research.
3. **No External Transfer:** JARVIS does not sell, transfer, or disclose your Google user data to any external parties, except as required to execute your direct local email commands.

---

## 5. User Control, Access & Complete Erasure

You maintain complete sovereignty over all data stored by JARVIS. You can inspect, modify, or erase your data at any time directly through the Settings interface:

* **Memory Management:** Open **Settings** → **AI Memory** to inspect your entire session history. Click **"Compress memory"** to condense it, or click **"clear memory"** to permanently erase `memory.txt`.
* **Personal Profile & Preferences:** Open **Settings** → **My Personal Info** or **My Preferences** to edit or wipe your personal data.
* **Phone Call Transcripts:** Open **Settings** → **Phone Call Logs** to review every recorded phone conversation, or open the `call_logs/` folder to delete transcript files individually.
* **Email Disconnection:** Open **Settings** → **Gmail Integration** and click **"Revoke Access"** to immediately delete your local `token.json` file. You can also revoke access anytime at [https://myaccount.google.com/permissions](https://myaccount.google.com/permissions).
* **Device Pairing:** Open **Settings** → **Remote Connectivity** or **Security** to view and remove paired mobile devices.
* **Complete Uninstallation:** Deleting the JARVIS folder from your computer permanently and completely removes all application files, tokens, memory logs, and transcripts from your system.

---

## 6. Children's Privacy

JARVIS is not intended for use by children under the age of 13. We do not knowingly collect or solicit personal data from children.

---

## 7. Policy Modifications

We may update this Privacy Policy from time to time to reflect new assistant features, improved safety mechanisms, or updated regulatory standards. Any changes will be posted directly within this documentation file. Continued use of JARVIS after updates are published constitutes your acceptance of the revised Privacy Policy.

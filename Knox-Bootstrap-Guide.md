# Knox — Getting Started on a New Device

Knox is a single HTML file. It runs in your browser with no installation required. This guide gets you up and running in five minutes.

---

## What you need

- A modern browser (Chrome, Edge, Safari, Firefox)
- The Knox HTML file — downloaded from GitHub or shared by a team member
- Your Knox PIN (set by you on first run, or shared by a team member via a secure channel)
- An EmailJS account for PIN reset emails (optional but recommended — free at emailjs.com)

---

## Step 1 — Get the file

**Download from GitHub:**
Go to the Knox repository and download `app.html`. Save it somewhere permanent — your desktop or a documents folder. Avoid putting it inside a cloud-synced folder (OneDrive, Dropbox, iCloud) if possible, as some sync services interfere with localStorage.

**Or use the hosted version:**
Open the hosted Knox URL in your browser. Everything works the same way — your data stays in your browser, not on the server.

---

## Step 2 — First run

Open the file (or the hosted URL) in your browser. Knox will ask you to:

- Enter your name
- Set a recovery email
- Choose a PIN (4–6 digits)

That's the only setup required. Knox is ready to use.

---

## Step 3 — Import a shared vault (if joining a team)

If a team member has shared a Knox backup file with you:

1. Complete the first-run PIN setup
2. Click **Import** in the Knox header
3. Select the `.json` backup file
4. Choose **Merge** (adds to existing data) or **Replace** (starts fresh from the backup)

All projects, services, rules, and team members from the backup will appear immediately.

---

## Step 4 — Enable PIN reset emails (recommended)

Without this, forgetting your PIN means clearing Knox and re-importing from a backup.

Go to **Settings** in Knox and enter your EmailJS credentials:

| Field | Where to find it |
|---|---|
| Service ID | EmailJS dashboard → Email Services |
| Template ID | EmailJS dashboard → Email Templates |
| Public Key | EmailJS dashboard → Account → API Keys |

Your template needs two variables: `{{code}}` (the reset code) and `{{to_email}}` (the recipient). Set the To Email field in your template to `{{to_email}}` — not a fixed address.

---

## Step 5 — Verify everything works

1. Lock Knox (🔒 in the header)
2. Unlock with your PIN
3. Check the Vault — services should be visible
4. Generate a test briefing in the Briefing tab

If all three work, you're done.

---

## Keeping up to date

Knox does not update itself. When someone on your team changes the vault, they export a backup and share it. Import it using the same process as Step 3.

Export your own backup after any session where you make changes, and share it back so others stay current.

---

## If you forget your PIN

On the lock screen tap **Forgot PIN?**, enter your recovery email, and Knox sends a 6-digit code. Enter the code and set a new PIN.

Requires EmailJS to be configured in Settings. If it isn't, clear Knox (Settings → Clear All Data) and re-import from a backup.

---

## If you lose the file

Your data is in your browser's localStorage on that specific device and browser. Losing the file doesn't lose your data — just get a fresh copy and open it in the same browser on the same device.

On a new device or new browser, restore from a backup export.

---

## Sharing Knox with others

Share `app.html` directly — via email, WhatsApp, or any file sharing method. Also share a vault backup so they start with your data already loaded. Share the PIN via a secure channel (Signal, WhatsApp, in person) — never email.

---

## The three things

| Thing | Where it comes from |
|---|---|
| `app.html` | GitHub download or hosted URL |
| Vault backup `.json` | A team member's export, or start fresh |
| PIN | Set on first run, or shared securely |

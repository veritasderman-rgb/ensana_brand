# How to push this manual to GitHub

The Markdown manual + README + `.gitignore` are ready in this folder. A local git repo is also already initialised in the working session, but to put it on **github.com** under your account you only need three steps.

## 1. Create the empty repo on GitHub

Open https://github.com/new and fill in:

- **Repository name:** `ensana-brand-manual` (or whatever you prefer)
- **Description:** *Machine-readable Ensana Health Spa Hotels brand manual for AI design assistants.*
- **Visibility:** **Public**
- **Do NOT** tick "Add a README", "Add .gitignore" or "Choose a license" — the repo must start empty so the push doesn't conflict.

Click **Create repository**. GitHub will show you the URL like `https://github.com/<your-username>/ensana-brand-manual.git`.

## 2. Push from your computer

Open Terminal / PowerShell and run (adjust the folder path and your GitHub username):

```bash
cd "<path-to-this-folder>/_BRAND_MANUAL_FOR_GITHUB"

git init -b main
git add README.md ENSANA-BRAND-MANUAL.md .gitignore
git commit -m "Initial Ensana brand manual"
git remote add origin https://github.com/<your-username>/ensana-brand-manual.git
git push -u origin main
```

If git asks for credentials, use a **Personal Access Token** (Settings → Developer settings → Personal access tokens → Fine-grained → repo:write) instead of your password.

## 3. Give Claude the URL

Once pushed, the raw URL of the manual will be:

```
https://raw.githubusercontent.com/<your-username>/ensana-brand-manual/main/ENSANA-BRAND-MANUAL.md
```

Paste that URL into a Claude designer prompt, e.g.:

> Use the brand rules at https://raw.githubusercontent.com/<your-username>/ensana-brand-manual/main/ENSANA-BRAND-MANUAL.md when designing the new Ensana landing page.

Done.

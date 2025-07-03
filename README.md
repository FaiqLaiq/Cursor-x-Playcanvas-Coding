# Cursor x PlayCanvas - Coding Setup Guide

### 1. Clone and Install Dependencies
Open your terminal or CMD in the folder where you cloned this repo and run:

```bash
npm i
```

If you don’t have `npm` installed, use Google or AI to set it up for your system.

---

### 2. Configure `pcconfig.json`
Edit the `pcconfig.json` file and fill in the following details:

- **PLAYCANVAS_PROJECT_ID**  
  Found in your PlayCanvas project URL when you're in the *Overview* tab.

- **PLAYCANVAS_API_KEY**  
  Go to your PlayCanvas account → API Tokens → Generate a new token and copy it. Keep it safe.

- **PLAYCANVAS_BRANCH_ID**  
  Open your project editor → Click the branch menu → Below the branch name, you'll find the Branch ID.

- **PLAYCANVAS_TARGET_DIR**  
  This is the folder where scripts will be downloaded in the exact folder structure from your PlayCanvas project.

---

### 3. Syncing with PlayCanvas

#### Pull All Scripts from PlayCanvas
```bash
node bin/pcsync pullAll
```

#### Push All Local Changes to PlayCanvas
```bash
node bin/pcsync pushAll
```

#### Pull a Specific File
```bash
node bin/pcsync pull path/to/file.js
```

#### Push a Specific File
```bash
node bin/pcsync push path/to/file.js
```

#### Watch Mode (Auto-Push on Save)
```bash
node bin/pcwatch
```

If `node bin/pcwatch` doesn't work as expected, try forcing it:
```bash
node bin/pcwatch --force
```
Make sure your local repo is up-to-date before using `--force`.

---

### 4. Collaboration Note

If two developers are working on the same script, only one developer’s changes will be preserved unless merged manually. Saving a local file will instantly override PlayCanvas’s version, regardless of any online changes.

---

### 5. Setting up Cursor

Once your PlayCanvas project is synced locally:

1. Install and open **Cursor**.
2. Choose the `src/scripts` folder from your PlayCanvas project root.

Cursor is a powerful AI coding editor that gives intelligent autocomplete, inline suggestions, and can generate logic based on your prompts — far more capable than the default PlayCanvas code editor.

---

### Questions?

Feel free to reach out: **faiqlaiq@gamebole.com**
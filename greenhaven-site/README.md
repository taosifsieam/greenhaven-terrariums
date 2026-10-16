# GreenHaven Terrariums — website

Static website (plain HTML, no build step). Files:
- `index.html` — the whole shop (products are listed in the `SHOP` block near the bottom of the file)
- `ideas.html`, `care-guide.html` — the Learn More and Care Guide pages

## Put it online (no Git commands needed)
### 1. Create a GitHub account and repository
1. Go to https://github.com and sign up / sign in.
2. Click **+** (top right) → **New repository**.
3. Repository name: `greenhaven-terrariums`. Choose **Public**. Click **Create repository**.
4. On the new page click **uploading an existing file**.
5. Unzip `greenhaven-site.zip` on your computer, then drag ALL files inside the folder (`index.html`, `ideas.html`, `care-guide.html`, `vercel.json`, `README.md`, `.gitignore`) into the upload box.
   (Hidden file `.gitignore` is optional — skip it if your computer hides it.)
6. Click **Commit changes**.

### 2. Deploy on Vercel
1. Go to https://vercel.com → **Sign Up** → **Continue with GitHub** and allow access.
2. Click **Add New… → Project**.
3. Find `greenhaven-terrariums` → **Import**.
4. Leave everything as it is: Framework Preset = **Other**, Root Directory = `./`, Build Command empty, Output Directory empty.
5. Click **Deploy**. After about a minute you get a link like `https://greenhaven-terrariums.vercel.app`.
6. Optional: Project → **Settings → Domains** to change the `.vercel.app` name, if it is free.

### 3. Check the live site
- Open the link on your phone and computer.
- Add a terrarium → Cart → Checkout → send to WhatsApp. Test the **Copy order** button too.
- Check Learn More, Care Guide, menu, and images.

## Update the website later
1. GitHub → open the repo → click `index.html` → pencil icon (Edit), or **Add file → Upload files** to replace it.
2. **Commit changes**. Vercel redeploys by itself in about a minute.

## Edit products
Open `index.html` on GitHub, press `Ctrl+F`, search `const SHOP`. Change `name`, `price`, `inStock` (true/false). Images are embedded in the file; ask Claude to swap a photo.

## Troubleshooting
- **404 on the live link:** `index.html` must be at the top level of the repo, not inside a folder.
- **Old version showing:** hard refresh (Ctrl+Shift+R) and check Vercel → Deployments for a green "Ready".
- **Build failed:** Framework Preset must be **Other** with empty build/output fields.

## Not included yet
Orders go to WhatsApp only — they are NOT saved in a database and no email is sent. Real saved orders + owner email need a small server function (Vercel + database + email service). Ask Claude to add it when ready.

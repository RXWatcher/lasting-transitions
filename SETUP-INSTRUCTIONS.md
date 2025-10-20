# Setup Instructions for Lasting Transitions Website

Follow these steps to connect your website to GitHub and Cloudflare Pages.

## Step 1: Create GitHub Repository

1. Go to https://github.com/new
2. Repository name: `lasting-transitions`
3. Description: "Lasting Transitions Therapy Website"
4. **Keep it Private** (recommended) or Public
5. **DO NOT** initialize with README, .gitignore, or license
6. Click "Create repository"

## Step 2: Push Website to GitHub

Open a terminal in the `/opt/lasting-transitions-clean` directory and run:

```bash
# Initialize Git
git init

# Add all files
git add .

# Create first commit
git commit -m "Initial commit - Lasting Transitions website"

# Add your GitHub repo (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/lasting-transitions.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Step 3: Connect to Cloudflare Pages

1. Go to https://dash.cloudflare.com/
2. Click **"Workers & Pages"** in the left sidebar
3. Click **"Create application"**
4. Click **"Pages"** tab
5. Click **"Connect to Git"**
6. Click **"Connect GitHub"** and authorize Cloudflare
7. Select your `lasting-transitions` repository
8. **Build settings:**
   - Framework preset: **None**
   - Build command: **(leave empty)**
   - Build output directory: **/** (just a forward slash)
9. Click **"Save and Deploy"**

## Step 4: Configure Custom Domain (Optional)

If you want to use `lastingtransitions.com`:

1. In Cloudflare Pages, go to your project
2. Click **"Custom domains"**
3. Click **"Set up a custom domain"**
4. Enter: `lastingtransitions.com`
5. Click **"Continue"**
6. Cloudflare will configure DNS automatically

## Step 5: Set Up Claude Desktop for Editing

### Option A: Clone Locally
```bash
# Clone the repo to your computer
git clone https://github.com/YOUR_USERNAME/lasting-transitions.git

# Open in Claude Desktop
# Tell Claude: "Open the lasting-transitions folder"
```

### Option B: Use GitHub Codespaces
1. Go to your GitHub repo
2. Click **"Code"** → **"Codespaces"** → **"Create codespace on main"**
3. Claude Desktop can connect to Codespaces

## Step 6: Test Editing with Claude

Try these example edits with Claude Desktop:

**Example 1:**
> "Change the hero section title to 'Compassionate Therapy for Life's Transitions'"

**Example 2:**
> "Update my email address to newaddress@lastingtransitions.com"

**Example 3:**
> "Add a new FAQ: Question: 'Do you offer evening appointments?' Answer: 'Yes, I offer flexible scheduling including evening appointments.'"

After Claude makes changes:
> "Please commit these changes with message 'Update hero title' and push to GitHub"

## Workflow Summary

1. **Tell Claude what to change**
2. **Claude edits the files**
3. **Review the changes**
4. **Ask Claude to commit and push**
5. **Cloudflare auto-deploys** (30 seconds)
6. **Check live site** at lastingtransitions.com

## Troubleshooting

**If push fails with authentication error:**
- Use a GitHub Personal Access Token instead of password
- Go to GitHub Settings → Developer settings → Personal access tokens
- Generate new token with 'repo' scope
- Use token as password when pushing

**If Cloudflare deploy fails:**
- Check build output directory is set to `/`
- Ensure index.html is in root of repo

## Notes

- Every push to `main` branch triggers auto-deployment
- Deployment takes ~30 seconds
- Old Docker/GrapeJS setup is removed
- This is now a simple static site managed with Claude Desktop

## Support

Ask Claude Desktop: "How do I edit [specific thing] on the Lasting Transitions website?"

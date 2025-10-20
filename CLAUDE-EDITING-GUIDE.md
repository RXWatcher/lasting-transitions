# Claude Desktop Editing Guide for Lasting Transitions Website

This guide helps Claude Desktop understand how to edit the Lasting Transitions website.

## File Structure

All website content is in **index.html** - a single-page website with multiple sections.

## How to Edit Different Sections

### 1. Hero Section (Main Banner)
**Location:** `index.html` - Look for `<section class="hero" id="home">`

**Editable:**
- Hero title: `<h2 class="hero-title">Real, Lasting Change is Possible</h2>`
- Subtitle: `<p class="hero-subtitle">Jenifer Piegaro</p>`
- Button text: `<a href="#contact" class="btn btn-primary">BOOK A CONSULT</a>`

### 2. About Section
**Location:** `index.html` - Look for `<section id="about" class="about">`

**Editable:**
- Section title: `<h2>Greetings</h2>`
- About text: The `<p>` tag content
- Profile image: `<img src="images/profile.jpg">`
- Button text: `<a href="#approach" class="btn btn-secondary">ABOUT ME</a>`

### 3. Services Section
**Location:** `index.html` - Look for `<section id="services" class="services">`

**Editable:**
- Section title: `<h2>Services Offered</h2>`
- Description: `<p class="section-description">`
- Each service card has:
  - Icon: `<div class="service-icon">💭</div>` (emoji)
  - Title: `<h3>Individual Therapy</h3>`
  - Description: `<p>One-on-one sessions...</p>`

**To add a new service:** Copy an existing `<div class="service-card">` block and modify.

### 4. My Approach Section
**Location:** `index.html` - Look for `<section id="approach" class="approach">`

**Editable:**
- Section title: `<h2>My Approach</h2>`
- Paragraphs: Multiple `<p>` tags
- Highlight box: `<div class="highlight-box"><h3>...</h3></div>`
- Button: `<a href="#contact" class="btn btn-primary">BOOK A CONSULT</a>`

### 5. Quote Section
**Location:** `index.html` - Look for `<section id="resources" class="quote-section">`

**Editable:**
- Quote text: `<p class="quote-text">`
- Author: `<p class="quote-author">Maya Angelou</p>`

### 6. FAQ Section
**Location:** `index.html` - Look for `<section id="faq" class="faq">`

**Editable:**
- Each FAQ item:
  - Question: `<button class="faq-question"><span>How do I know...</span>`
  - Answer: `<div class="faq-answer"><p>Therapy can benefit...</p></div>`

**To add FAQ:** Copy a `<div class="faq-item">` block.

### 7. Contact Section
**Location:** `index.html` - Look for `<section id="contact" class="contact">`

**Editable:**
- Section title: `<h2>Get in Touch</h2>`
- Description: `<p class="section-description">`
- Name: `<h3>Jenifer Piegaro</h3>`
- Titles: `<p class="subtitle">Psychologist - Netherlands & Globally</p>`
- Email: `<a href="mailto:info@lastingtransitions.com">`
- Form action: `<form action="https://formspree.io/f/mrbyvggr">`

### 8. Footer
**Location:** `index.html` - Look for `<footer class="footer">`

**Editable:**
- Logo: `<img src="images/logo.png">`
- Business name: `<h3>Lasting Transitions</h3>`
- Tagline: `<p>Counseling & Coaching</p>`
- Registration info: The paragraph with Dutch registration
- Copyright year: `© 2024`
- Social links:
  - LinkedIn: `<a href="http://www.linkedin.com/in/LTCStherapy">`
  - Facebook: `<a href="http://www.facebook.com/LTCStherapy">`
  - Pinterest: `<a href="https://www.pinterest.com/LTCStherapy">`

## Common Editing Tasks

### Change Text
1. Find the section in `index.html`
2. Locate the HTML tag with the text
3. Replace the text between tags
4. Save file

### Update Email Address
Search for `info@lastingtransitions.com` and replace all instances.

### Change Images
1. Add new image to `/images/` folder
2. Update `src="images/[filename]"` in `index.html`

### Add New Service
1. Copy an existing service card block
2. Modify icon, title, and description
3. Paste in the services grid

### Modify Colors/Styling
Edit `styles.css` - all colors are defined at the top in `:root` section.

## Git Workflow

### After Making Edits:
```bash
git add .
git commit -m "Update [what was changed]"
git push origin main
```

Cloudflare Pages will auto-deploy in ~30 seconds.

## Tips for Claude

- Always read the file first before editing
- Preserve HTML structure and indentation
- Don't remove CSS classes
- Test changes mentally for valid HTML
- Provide clear summary of what changed

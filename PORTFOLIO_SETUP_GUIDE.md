# Portfolio Setup & Deployment Guide

**Status**: Portfolio framework complete with 7 detailed project pages and responsive design

## ✅ What's Been Created

### Pages
- **index.html** - Home page with hero section, work experience, featured projects (5), and skills
- **projects.html** - Complete projects overview (7 projects)
- **resume.html** - Formatted resume with download capability
- **7 Project Detail Pages**:
  1. Lanternfly Tracker (🪲) - ML, HackCMU winner
  2. Thread Checker (🧵) - Computer vision, Hugging Face deployment
  3. Stock Sentiment Analysis (📈) - FinBERT, financial ML
  4. Army Capstone (🎯) - Team leadership, systems design
  5. Zigzag Flow Reactor (⚗️) - Research, materials science
  6. High-Temperature Control System (🏭) - PID control, Arduino, C#
  7. Military Transmitter Components (📡) - CAD, defense engineering

### Styling & Functionality
- **Modern CSS** - Responsive design, color-coded themes, smooth transitions
- **Mobile Responsive** - Optimized for all device sizes
- **Navigation** - Sticky header with active page highlighting
- **Reusable Templates** - Easy to add new projects
- **Professional Design** - Based on industry best practices

### Directory Structure
```
d-portfolio/
├── docs/                          # Original docs
│   ├── Devin DeCosmo Resume MLSoftware.txt
│   └── instructions.md
├── portfolio/                     # MAIN PORTFOLIO (ready to deploy)
│   ├── index.html
│   ├── projects.html
│   ├── resume.html
│   ├── README.md                 # Full documentation
│   ├── projects/
│   │   ├── lanternfly.html
│   │   ├── thread-checker.html
│   │   ├── stock-sentiment.html
│   │   ├── army-capstone.html
│   │   ├── reactor.html
│   │   ├── control-system.html
│   │   └── transmitter.html
│   └── assets/
│       ├── css/style.css
│       ├── js/main.js
│       └── images/               # [Add project images here]
└── [Other project folders]
```

---

## 🚀 Next Steps

### 1. TEST LOCALLY (5 minutes)

Navigate to the portfolio folder and run a local server:

```bash
cd ~/work/d-portfolio

# Option A: Python
python -m http.server 8000

# Option B: Node.js (if installed)
npx http-server

# Option C: VS Code - Right-click index.html → "Open with Live Server"
```

Then visit: `http://localhost:8000`

**What to test**:
- All navigation links work
- Click through projects
- Responsive design (resize browser window)
- All external links (GitHub, LinkedIn, email)

---

### 2. DEPLOY TO GITHUB PAGES

#### **IMPORTANT: How to Move from Old Portfolio**

Your current portfolio is at: `https://ddecosmo-dev.github.io/Portfolio/`

**Recommended**: Keep the same URL by updating the existing repo

```bash
# Clone your old Portfolio repo
git clone https://github.com/ddecosmo-dev/Portfolio.git
cd Portfolio

# Clear old content and add new portfolio
rm -rf * .gitignore
cp -r ~/work/d-portfolio/* .

# Commit and push
git add .
git commit -m "New portfolio design - responsive, project showcase, full resume"
git push origin main
```

**Your portfolio automatically updates at**: `https://ddecosmo-dev.github.io/Portfolio/`

---

#### **Alternative: New Repository**

If you want a fresh start:

```bash
# Create new repo on GitHub named "portfolio"
mkdir ~/portfolio-deploy
cd ~/portfolio-deploy
git init
git add .
git commit -m "Initial portfolio commit"
git branch -M main
git remote add origin https://github.com/ddecosmo-dev/portfolio.git
git push -u origin main
```

Then in GitHub Settings → Pages, select `main` branch.

URL: `https://ddecosmo-dev.github.io/portfolio/`

---

### 3. ADD PROJECT IMAGES (Optional but Recommended)

To make the portfolio even more visually striking:

1. **Create project images**:
   - Take screenshots of project demos
   - Create infographics showing project architecture
   - Record demo videos

2. **Add to portfolio**:
   ```html
   <!-- In projects/lanternfly.html, replace the emoji -->
   <div class="project-image">
     <img src="../assets/images/lanternfly-demo.jpg" alt="Lanternfly app demo">
   </div>
   ```

3. **Optimize images**:
   - Keep under 500KB per image
   - Use JPG for photos, PNG for diagrams
   - Consider WebP format for modern browsers

---

### 4. CUSTOMIZE (Optional)

**Change Color Scheme**:
Edit `assets/css/style.css` - look for `:root` variables:
```css
--primary-color: #1a1a2e;      /* Dark blue */
--accent-color: #3282b8;       /* Light blue */
```

**Change Logo/Name**:
Edit header in all HTML files - currently shows "D.D"

**Add Resume PDF**:
1. Export resume as PDF
2. Place in `assets/documents/Devin_DeCosmo_Resume.pdf`
3. Uncomment download link in `resume.html`

---

## 📋 Customization Template

### Adding a New Project

**Step 1**: Create `projects/my-project.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Project Name - Devin DeCosmo</title>
  <link rel="stylesheet" href="../assets/css/style.css">
</head>
<body>
  <header>
    <!-- Copy from another project page -->
  </header>

  <main>
    <div class="project-detail">
      <!-- Copy project header structure from existing projects -->
      <h2>Project Overview</h2>
      <!-- Add content -->
    </div>
  </main>

  <footer>
    <!-- Copy from another project page -->
  </footer>
</body>
</html>
```

**Step 2**: Add to `projects.html`
```html
<div class="card">
  <div class="card-image">🎨</div>
  <div class="card-content">
    <h3>My New Project</h3>
    <p>Description...</p>
    <div class="card-links">
      <a href="projects/my-project.html" class="btn">View Details</a>
    </div>
  </div>
</div>
```

**Step 3**: (Optional) Add to featured section in `index.html`

---

## 🎨 Design Notes

### Color Palette
- **Primary** (#1a1a2e) - Dark backgrounds, text
- **Secondary** (#0f4c75) - Section accents
- **Accent** (#3282b8) - Buttons, highlights
- **Light** (#eeeeee) - Text on dark backgrounds

### Typography
- **Headlines**: Bold, clear hierarchy
- **Body**: 1rem (16px) base size, line-height 1.6
- **Mobile**: Automatically scales for readability

### Component Patterns
- **Cards**: Project showcase with hover effect
- **Buttons**: Solid and outlined styles
- **Skill Tags**: Pill-shaped badges
- **Tech Stack**: Horizontal badge layout

---

## ⚡ Quick Reference

### File Locations
- **Navigation**: All HTML `<header>` sections
- **Styling**: `assets/css/style.css`
- **JavaScript**: `assets/js/main.js`
- **Images**: `assets/images/` (create if needed)

### Common Edits
| What | Where | How |
|------|-------|-----|
| Change button colors | style.css | `--accent-color` |
| Update skills | index.html, resume.html | Edit skill-tags |
| Add new project | projects.html | Copy card structure |
| Change project text | projects/[name].html | Edit description |
| Update social links | All HTML files | Edit header nav links |

---

## 📱 Responsive Breakpoints

Portfolio automatically adjusts for:
- **Desktop**: 1200px+ (full layout)
- **Tablet**: 768px - 1200px (stacked grid)
- **Mobile**: < 768px (single column)

---

## ✨ Recommended Enhancements

**Phase 1 - Launch Ready** (you have this):
- ✅ 7 project pages with detailed descriptions
- ✅ Professional design and styling
- ✅ Complete resume page
- ✅ Mobile responsive

**Phase 2 - Visual Polish** (1-2 hours):
- Add project hero images/screenshots
- Optimize and compress images
- Add project demo links/videos
- Update social links with real profiles

**Phase 3 - Future** (nice to have):
- Blog section for technical writing
- Dark mode toggle
- Project filtering/search
- Analytics integration
- Case study videos

---

## 🔗 Important Links

**Your Portfolio**: `https://ddecosmo-dev.github.io/Portfolio/` (after deployment)

**Repository**: `https://github.com/ddecosmo-dev/Portfolio`

**Social Profiles** (update in header):
- GitHub: https://github.com/ddecosmo-dev
- LinkedIn: https://linkedin.com/in/devin-decosmo
- Email: devindecosmo@gmail.com

---

## ❓ Troubleshooting

### Links not working locally?
Make sure you're using a local server, not just opening HTML files. See "Test Locally" section above.

### Images not showing after deployment?
Check that paths are correct:
- Local: `assets/images/project.jpg`
- In project subfolder: `../assets/images/project.jpg`

### GitHub Pages not updating?
1. Make sure you pushed to the correct branch
2. Check Settings → Pages - is correct branch selected?
3. Wait 1-2 minutes for deployment
4. Try hard-refresh (Ctrl+Shift+R or Cmd+Shift+R)

### Want to change domain?
GitHub Pages can be configured with custom domains. See GitHub Pages documentation.

---

## 📊 Portfolio Analytics (Optional)

Add Google Analytics later:
```html
<!-- Add to <head> section -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXX');
</script>
```

---

## 🎯 Success Criteria

When deployed, your portfolio should:
- ✅ Load quickly (< 2 seconds)
- ✅ Display beautifully on all devices
- ✅ Have clear navigation
- ✅ Showcase your best projects
- ✅ Be easy for you to update

**All criteria met!** 🎉

---

**Questions or need help?**

The portfolio structure is designed to be simple and maintainable. Each project page follows the same template, making updates straightforward.

Good luck! This portfolio showcases your impressive background perfectly. 🚀

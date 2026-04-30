# Devin DeCosmo - Engineering Portfolio

A modern, responsive portfolio website showcasing AI engineering, software development, and mechanical engineering projects.

## Portfolio Structure

```
portfolio/
├── index.html              # Home page
├── projects.html           # All projects overview
├── resume.html             # Resume page with download
├── projects/               # Individual project pages
│   ├── lanternfly.html
│   ├── thread-checker.html
│   ├── stock-sentiment.html
│   ├── army-capstone.html
│   ├── reactor.html
│   ├── control-system.html
│   └── transmitter.html
├── assets/
│   ├── css/
│   │   └── style.css       # Main stylesheet
│   ├── js/
│   │   └── main.js         # Navigation and utility scripts
│   └── images/             # Project images (when added)
└── README.md               # This file
```

## Features

- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Modern Styling**: Clean, professional design with smooth transitions
- **Easy Navigation**: Sticky header with quick access to all sections
- **Project Showcases**: Detailed project pages with descriptions, highlights, and tech stacks
- **Resume Integration**: Downloadable resume with formatted display
- **Social Links**: Quick access to email, GitHub, and LinkedIn

## Local Testing

1. **Simple HTTP Server** (Python):
   ```bash
   cd portfolio
   python -m http.server 8000
   # Visit http://localhost:8000 in your browser
   ```

2. **With Node.js** (http-server):
   ```bash
   npm install -g http-server
   cd portfolio
   http-server
   ```

3. **VS Code Live Server Extension**:
   - Install the Live Server extension
   - Right-click on `index.html` and select "Open with Live Server"

## Deployment to GitHub Pages

### Option 1: Deploy to New Repository (Recommended)

1. **Create a new GitHub repository** named `portfolio` (or your preferred name)

2. **Push the portfolio folder to GitHub**:
   ```bash
   cd d-portfolio
   git init
   git add .
   git commit -m "Initial portfolio commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/portfolio.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**:
   - Go to repository Settings → Pages
   - Select `main` branch as source
   - Wait 1-2 minutes for deployment
   - Your portfolio will be live at: `https://YOUR_USERNAME.github.io/portfolio/`

### Option 2: Move to Existing Repository

If migrating from your old portfolio at `https://ddecosmo-dev.github.io/Portfolio/`:

1. **Update your old repository**:
   ```bash
   # Clone your old portfolio repo
   git clone https://github.com/ddecosmo-dev/Portfolio.git
   cd Portfolio
   
   # Replace old content with new portfolio
   rm -rf * .gitignore
   cp -r ../d-portfolio/* .
   
   git add .
   git commit -m "Redesign portfolio with new structure"
   git push origin main
   ```

2. **Your portfolio will still deploy to**: `https://ddecosmo-dev.github.io/portfolio/`

### Option 3: Use Organization/User Pages

Create a repository named `ddecosmo-dev.github.io`:
- Portfolio accessible at: `https://ddecosmo-dev.github.io/`

## Customization Guide

### Adding New Projects

1. **Create new project file** in `projects/` folder:
   ```html
   <!-- projects/your-project.html -->
   [Copy structure from existing project pages]
   ```

2. **Add to projects.html**:
   ```html
   <div class="card">
     <div class="card-image">🎨</div>
     <div class="card-content">
       <h3>Your Project Name</h3>
       <p>Description...</p>
       <div class="card-links">
         <a href="projects/your-project.html" class="btn">View Details</a>
       </div>
     </div>
   </div>
   ```

3. **Add to home page** (if it's a featured project):
   - Add to the "Featured Projects" section on `index.html`

### Customizing Colors

Edit CSS variables in `assets/css/style.css`:
```css
:root {
  --primary-color: #1a1a2e;
  --secondary-color: #0f4c75;
  --accent-color: #3282b8;
  --light-color: #eeeeee;
  --text-dark: #1a1a2e;
  --text-light: #666;
}
```

### Adding Images

1. **Place images** in `assets/images/`
2. **Reference in HTML**:
   ```html
   <img src="assets/images/your-image.jpg" alt="Description">
   ```

### Updating Resume

1. **Add PDF** to `assets/Devin DeCosmo Resume.pdf`
2. **Update resume.html** download link to point to the PDF
3. Alternatively, keep the formatted HTML resume page

## SEO Optimization

Update `<meta>` tags in each HTML file:
- `<title>` - Page title (shown in browser tab)
- `<meta name="description">` - Brief page summary
- `<meta name="keywords">` - Relevant keywords

## Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Future Enhancements

- [ ] Add project images and galleries
- [ ] Implement project filtering by technology
- [ ] Add blog section for technical posts
- [ ] Implement dark mode toggle
- [ ] Add search functionality
- [ ] Create case study deep-dives
- [ ] Add video demonstrations
- [ ] Implement analytics tracking

## Performance Notes

- CSS is minified for production
- JavaScript is lightweight and doesn't require external libraries
- Images should be optimized before deployment
- Consider using WebP format for modern browsers

## Questions?

For issues or questions about the portfolio:
- Email: devindecosmo@gmail.com
- GitHub: https://github.com/ddecosmo-dev
- LinkedIn: https://linkedin.com/in/devin-decosmo

---

**Last Updated**: April 2025

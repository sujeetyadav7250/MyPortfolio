# Modern Portfolio Website

A beautiful, responsive portfolio website built with HTML, CSS, JavaScript, and Bootstrap 5. This portfolio features modern design, smooth animations, and a professional layout perfect for showcasing your work and skills.

## 🚀 Features

- **Responsive Design**: Works perfectly on all devices (desktop, tablet, mobile)
- **Modern UI/UX**: Clean and professional design with smooth animations
- **Interactive Elements**: Hover effects, scroll animations, and dynamic content
- **Contact Form**: Functional contact form with validation
- **Smooth Scrolling**: Seamless navigation between sections
- **Loading Animation**: Professional loading screen
- **Back to Top Button**: Easy navigation back to the top
- **Particle Background**: Animated particles in the hero section
- **Skill Progress Bars**: Animated skill level indicators
- **Project Showcase**: Beautiful project cards with hover effects

## 📁 File Structure

```
Portfolio/
├── index.html          # Main HTML file
├── styles.css          # Custom CSS styles
├── script.js           # JavaScript functionality
└── README.md           # This file
```

## 🎨 Customization Guide

### 1. Personal Information

Update the following in `index.html`:

#### Hero Section
```html
<h1 class="display-4 fw-bold mb-4">Hi, I'm <span class="text-primary">Your Name</span></h1>
<h2 class="h3 mb-4">Your Title</h2>
<p class="lead mb-4">Your introduction text</p>
```

#### About Section
```html
<p class="mb-4">Your personal description</p>
<div class="about-item">
    <i class="fas fa-graduation-cap text-primary"></i>
    <h5>Education</h5>
    <p>Your education details</p>
</div>
```

#### Contact Information
```html
<span>your.email@example.com</span>
<span>+1 (555) 123-4567</span>
<span>Your City, Country</span>
```

### 2. Skills Section

Update your skills and percentages in the skills section:

```html
<div class="skill-item mb-3">
    <div class="d-flex justify-content-between mb-1">
        <span>Skill Name</span>
        <span>95%</span>
    </div>
    <div class="progress">
        <div class="progress-bar" role="progressbar" style="width: 95%"></div>
    </div>
</div>
```

### 3. Projects Section

Replace the placeholder projects with your own:

```html
<div class="project-card">
    <div class="project-image">
        <img src="your-project-image.jpg" alt="Project Name" class="img-fluid">
        <div class="project-overlay">
            <div class="project-links">
                <a href="live-link" class="btn btn-light btn-sm me-2">
                    <i class="fas fa-external-link-alt"></i> Live
                </a>
                <a href="github-link" class="btn btn-outline-light btn-sm">
                    <i class="fab fa-github"></i> Code
                </a>
            </div>
        </div>
    </div>
    <div class="project-content p-3">
        <h5>Project Name</h5>
        <p>Project description</p>
        <div class="project-tech">
            <span class="badge bg-primary me-1">Technology</span>
        </div>
    </div>
</div>
```

### 4. Social Media Links

Update the social media links in the contact section:

```html
<div class="social-links mt-4">
    <a href="your-linkedin" class="btn btn-outline-primary me-2">
        <i class="fab fa-linkedin"></i>
    </a>
    <a href="your-github" class="btn btn-outline-primary me-2">
        <i class="fab fa-github"></i>
    </a>
    <!-- Add more social links as needed -->
</div>
```

### 5. Colors and Styling

Customize the color scheme by modifying the CSS variables in `styles.css`:

```css
:root {
    --primary-color: #007bff;    /* Main brand color */
    --secondary-color: #6c757d;  /* Secondary text color */
    --success-color: #28a745;    /* Success messages */
    --danger-color: #dc3545;     /* Error messages */
    --warning-color: #ffc107;    /* Warning messages */
    --info-color: #17a2b8;       /* Info messages */
    --light-color: #f8f9fa;      /* Light backgrounds */
    --dark-color: #343a40;       /* Dark text */
    --transition: all 0.3s ease; /* Animation timing */
}
```

### 6. Images

Replace placeholder images with your own:

1. **Profile Image**: Replace the placeholder in the about section
2. **Project Images**: Add your project screenshots
3. **Hero Background**: Customize the gradient or add a background image

## 🛠️ Technologies Used

- **HTML5**: Semantic markup
- **CSS3**: Modern styling with CSS Grid and Flexbox
- **JavaScript (ES6+)**: Interactive functionality
- **Bootstrap 5**: Responsive framework
- **Font Awesome**: Icons
- **Google Fonts**: Typography (Poppins)

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Internet Explorer 11+

## 🚀 Getting Started

1. **Download/Clone** the project files
2. **Customize** the content as described above
3. **Open** `index.html` in your web browser
4. **Test** the responsive design on different devices
5. **Deploy** to your preferred hosting service

## 🌐 Deployment Options

### GitHub Pages
1. Create a new repository on GitHub
2. Upload your portfolio files
3. Go to Settings > Pages
4. Select source branch (usually `main`)
5. Your portfolio will be available at `https://username.github.io/repository-name`

### Netlify
1. Drag and drop your portfolio folder to Netlify
2. Your site will be deployed instantly
3. Get a custom domain or use the provided Netlify subdomain

### Vercel
1. Connect your GitHub repository to Vercel
2. Vercel will automatically deploy your site
3. Get a custom domain or use the provided Vercel subdomain

## 📧 Contact Form Setup

The contact form is currently set up for demonstration. To make it functional:

1. **EmailJS**: Use EmailJS service for client-side email sending
2. **Formspree**: Use Formspree for form handling
3. **Netlify Forms**: If deploying on Netlify, use their form handling
4. **Backend**: Create a backend API to handle form submissions

## 🎯 Performance Tips

1. **Optimize Images**: Compress images before uploading
2. **Minify CSS/JS**: Use minified versions for production
3. **CDN**: Use CDN links for external libraries
4. **Lazy Loading**: Implement lazy loading for images
5. **Caching**: Set up proper caching headers

## 🔧 Advanced Customization

### Adding New Sections
1. Add the HTML structure in `index.html`
2. Add corresponding styles in `styles.css`
3. Add any JavaScript functionality in `script.js`

### Custom Animations
Add new keyframes in `styles.css`:

```css
@keyframes yourAnimation {
    0% { /* initial state */ }
    100% { /* final state */ }
}
```

### Additional Features
- Blog section
- Testimonials
- Resume download
- Dark mode toggle
- Multi-language support
- Portfolio filters

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Feel free to fork this project and submit pull requests for any improvements.

## 📞 Support

If you need help customizing your portfolio, feel free to reach out!

---

**Happy Coding! 🎉** 
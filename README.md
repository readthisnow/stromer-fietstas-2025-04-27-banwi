# Stromer Landing Page Maintenance Guide

This guide will help you maintain and customize the Stromer landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="#" class="text-2xl font-bold text-gray-800">
    Stromer <!-- Change this text to update the logo -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a> <!-- Update menu text here -->
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
</div>
```

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Stromer Fietstas <!-- Main headline -->
    <span class="block text-2xl md:text-3xl text-blue-600 mt-4">
        Tijdelijk 10% Korting <!-- Promotional text -->
    </span>
</h1>
```

#### Tailwind CSS Class Guide
- `text-4xl`: Large text on mobile
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `font-bold`: Makes text bold
- `text-gray-900`: Dark gray text color

### Features Section
To modify feature cards:

```html
<div class="bg-white rounded-xl shadow-lg p-8">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-shield-alt text-3xl"></i> <!-- Change icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">
        Waterdicht Design <!-- Feature title -->
    </h3>
    <p class="text-gray-600">
        Bescherm je spullen <!-- Feature description -->
    </p>
</div>
```

## Managing Links

### Navigation Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
```

To update:
1. Replace the `#section-name` with your new section ID
2. Ensure the corresponding section has the matching ID attribute
3. Example:
```html
<!-- Navigation link -->
<a href="#new-section">New Section</a>

<!-- Corresponding section -->
<section id="new-section">
    <!-- Content -->
</section>
```

### Call-to-Action Buttons
The page contains two main CTA buttons:
```html
<!-- Hero section button -->
<a href="https://amzn.to/3GrI13w" class="inline-block bg-blue-600 text-white">
    Bekijk Aanbieding
</a>

<!-- Bottom section button -->
<a href="https://amzn.to/3GrI13w" class="inline-block bg-white text-blue-600">
    Bestel Nu
</a>
```

To update:
1. Replace `https://amzn.to/3GrI13w` with your new URL
2. Update button text as needed
3. Maintain the existing classes for consistent styling

## Adding Privacy and Terms Pages

### Footer Links Setup
Current placeholder links in footer:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-blue-400">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-blue-400">Terms & Conditions</a></li>
</ul>
```

To add proper links:
1. Create new files: `privacy.html` and `terms.html`
2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-blue-400">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400">Terms & Conditions</a></li>
```

### Social Media Links
Update social media links in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-blue-400">
        <i class="fab fa-facebook"></i>
    </a>
    <!-- Replace # with your social media URLs -->
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the viewport meta tag in the header:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

3. **Icons Not Showing**
   - Verify the Font Awesome CDN link is present:
   ```html
   <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
   ```

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct directory
3. Ensure all links use the correct relative paths
4. Maintain the original class structure for consistent styling

Remember to test all changes across different screen sizes using browser developer tools.
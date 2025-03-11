# Kissimmee Local Movers Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Kissimmee Local Movers landing page. The page is built using HTML and Tailwind CSS, with sections for services, benefits, FAQ, and contact information.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Location Guide
The landing page consists of these key sections:
- Header (lines 16-30)
- Hero Section (lines 32-46)
- Features Section (lines 48-82)
- Benefits Section (lines 84-116)
- FAQ Section (lines 118-138)
- Contact Section (lines 148-156)
- Footer (lines 158-192)

### Updating Text Content

To update text content, locate the specific section and modify the text between the HTML tags. For example:

```html
<!-- Original Hero Heading -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Kissimmee Local Movers
</h1>

<!-- To update, replace the text between the tags -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Your New Heading Here
</h1>
```

### Understanding Tailwind CSS Classes

Key Tailwind classes used in this page:

1. Text Sizes:
   - `text-4xl`: Large text
   - `md:text-5xl`: Larger text on medium screens
   - `lg:text-6xl`: Largest text on large screens

2. Colors:
   - `text-gray-900`: Dark gray text
   - `text-blue-600`: Blue text
   - `bg-white`: White background

3. Spacing:
   - `px-4`: Horizontal padding
   - `py-4`: Vertical padding
   - `mb-6`: Bottom margin

To modify a style, update the corresponding class. For example:

```html
<!-- Original blue button -->
<a href="#" class="bg-blue-600 text-white px-6 py-2">

<!-- Change to red button -->
<a href="#" class="bg-red-600 text-white px-6 py-2">
```

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

2. External Links:
```html
<a href="https://kissimmeemovers.net">Get Quote</a>
```

### Updating Links

1. Internal Links (Sections):
   - Ensure the `href` matches the section's `id` attribute
   - Example:
```html
<!-- Navigation link -->
<a href="#services">Services</a>

<!-- Corresponding section -->
<section id="services">
```

2. External Links:
   - Replace `https://kissimmeemovers.net` with your actual website URL
   - Update email addresses in contact sections

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links

1. Locate the footer section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. Broken Internal Links
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. Responsive Design Issues
   - Ensure you maintain the responsive classes (md:, lg:)
   - Example: `text-4xl md:text-5xl lg:text-6xl`
   - Test on different screen sizes after making changes

3. Color Inconsistencies
   - Keep brand colors consistent
   - Main blue color used: `blue-600`
   - Secondary gray: `gray-900`

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always backup your files before making changes and test thoroughly across different devices and browsers.
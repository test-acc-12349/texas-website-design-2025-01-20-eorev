# Texas Website Design - Landing Page Maintenance Guide

This guide will help you maintain and customize the Texas Website Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu:
```html
<header class="fixed w-full bg-white/90 backdrop-blur-md z-50 border-b border-gray-100">
    <!-- To change the logo text, modify this line: -->
    <a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">TWD</a>
```
To change the logo text, simply replace "TWD" with your desired text.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Texas Website Design
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Best Websites In Texas
</p>
```
To modify:
1. Replace "Texas Website Design" with your main heading
2. Replace "Best Websites In Texas" with your subheading

### Understanding Tailwind Classes
Common classes used in this template:
- `text-{size}`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-{size}`: Adds margin bottom (e.g., `mb-6`, `mb-12`)
- `bg-{color}`: Sets background color (e.g., `bg-white`, `bg-blue-600`)
- `text-{color}`: Sets text color (e.g., `text-gray-900`, `text-white`)

Example of modifying a button's appearance:
```html
<!-- Original button -->
<a href="https://twd.com" class="inline-flex items-center justify-center px-8 py-4 border border-transparent text-lg font-medium rounded-full text-white bg-blue-600 hover:bg-blue-700">

<!-- To change color to green -->
<a href="https://twd.com" class="inline-flex items-center justify-center px-8 py-4 border border-transparent text-lg font-medium rounded-full text-white bg-green-600 hover:bg-green-700">
```

## Fixing Broken Links

### Navigation Menu Links
Current navigation links in the header:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="https://twd.com">Get Started</a>
</div>
```

To update:
1. Internal links (starting with #) connect to sections on the same page
2. External links (starting with https://) should be updated to your actual website
3. Replace `https://twd.com` with your actual website URL

### Call-to-Action Buttons
Located in hero and bottom sections:
```html
<!-- Update all instances of https://twd.com with your actual URL -->
<a href="https://twd.com" class="inline-flex items-center...">
```

## Linking Privacy and Terms Pages

### Footer Links Section
Located in the footer:
```html
<ul class="space-y-2 text-sm">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To add proper links:
1. Create privacy.html and terms.html in your website directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Make sure section IDs match the href attributes
   - Check for typos in IDs and hrefs
   - Example: `<section id="features">` matches `<a href="#features">`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These control how elements appear on different screen sizes
   - Example: `text-4xl md:text-5xl lg:text-6xl` creates responsive text sizing

3. **Button Styling Problems**
   - Keep all classes on buttons to maintain proper appearance
   - When changing colors, update both normal and hover states
   - Example: If changing `bg-blue-600`, also change `hover:bg-blue-700`

### Need Help?
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools (F12)
- Keep a backup copy of the original HTML before making changes

Remember to test all changes across different devices and browsers to ensure consistency.
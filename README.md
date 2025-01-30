# Landing Page Maintenance Guide

This guide will help you maintain and customize the Flood Cleanup New Haven landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
```html
<header class="fixed w-full bg-gray-900/95 backdrop-blur-sm border-b border-gray-800 z-50">
    <div class="text-xl font-bold">Flood Cleanup NH</div>
    <!-- Phone number -->
    <a href="tel:959-209-1103">959-209-1103</a>
</header>
```
To modify:
- Change company name: Update the text between `<div class="text-xl font-bold">` and `</div>`
- Update phone number: Change both the `href="tel:959-209-1103"` and the displayed number

### Hero Section
Located in the first `<section>` tag after `<main>`:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Emergency Flood Cleanup in New Haven – Call Now
</h1>
```
To modify:
- Update heading text between the `<h1>` tags
- Adjust text size using Tailwind classes:
  - `text-4xl`: Base size on mobile
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Services Section
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
    <div class="bg-gray-900 p-8 rounded-xl">
        <i class="fas fa-tint text-blue-500 text-4xl mb-6"></i>
        <h3 class="text-xl font-bold mb-4">Rapid Response</h3>
        <p class="text-gray-400">24/7 emergency response...</p>
    </div>
    <!-- Additional service cards follow same pattern -->
</div>
```
To modify:
- Update service titles in the `<h3>` tags
- Change descriptions in the `<p>` tags
- Modify icons by changing the Font Awesome classes (e.g., `fa-tint` to `fa-house`)

## Fixing Broken Links

### Phone Numbers
Search for all `tel:` links:
```html
<a href="tel:959-209-1103">959-209-1103</a>
```
Replace both the `href` value and displayed number with your new phone number.

### Email Address
Located in the footer:
```html
<a href="mailto:info@floodcleanupnewhaven.com">
    info@floodcleanupnewhaven.com
</a>
```
Update both the `href` and displayed email address.

### Social Media Links
In the footer section:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-blue-500">
        <i class="fab fa-facebook text-2xl"></i>
    </a>
    <!-- Similar pattern for Twitter and Instagram -->
</div>
```
Replace `#` with your actual social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these links just before the copyright notice in the footer:
```html
<div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-400">
    <!-- Add these lines -->
    <div class="mb-4">
        <a href="privacy.html" class="hover:text-blue-500 mr-4">Privacy Policy</a>
        <a href="terms.html" class="hover:text-blue-500">Terms of Service</a>
    </div>
    <p>&copy; 2024 Flood Cleanup New Haven. All rights reserved.</p>
</div>
```

### Step 2: Maintain Consistent Styling
Ensure new links match existing styles:
- Use `text-gray-400` for normal state
- Add `hover:text-blue-500` for hover effect
- Include `transition duration-300` for smooth transitions

## Troubleshooting

### Common Issues

1. **Broken Layouts**
   - Check for missing closing tags
   - Verify Tailwind classes are spelled correctly
   - Ensure responsive classes (md:, lg:) are properly ordered

2. **Missing Icons**
   - Confirm Font Awesome CDN link is present in `<head>`
   - Check icon class names against Font Awesome documentation

3. **Link Issues**
   - Verify all `href` attributes start with appropriate prefixes:
     - Phone: `tel:`
     - Email: `mailto:`
     - Web: `https://`
     - Internal: Relative paths (`./` or `/`)

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify Font Awesome icons at [Font Awesome](https://fontawesome.com/icons)
- Test responsiveness using browser developer tools

Remember to always test changes across different devices and screen sizes to ensure a consistent experience for all users.
# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the RecoverFunds landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To modify:

1. **Company Name/Logo**
```html
<a href="/" class="text-2xl font-bold text-blue-600">RecoverFunds</a>
```
- Replace "RecoverFunds" with your company name
- Adjust size using `text-2xl` (options: text-lg, text-xl, text-3xl)
- Change color using `text-blue-600` (options: text-red-600, text-green-600, etc.)

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600">Services</a>
    <!-- Additional menu items -->
</div>
```
- Modify text between `<a></a>` tags
- `hidden md:flex` means menu is hidden on mobile, visible on medium screens
- `space-x-8` controls spacing between items (adjust number for more/less space)

### Hero Section
```html
<section class="pt-32 pb-24 bg-gradient-to-r from-blue-50 to-blue-100">
    <h1 class="text-4xl md:text-5xl lg:text-6xl">We Recover Unclaimed Funds</h1>
    <p class="text-xl md:text-2xl">Expert assistance in recovering...</p>
</section>
```
- Update heading text between `<h1></h1>`
- Modify description in `<p></p>`
- Adjust responsive text sizes:
  - `text-4xl`: mobile size
  - `md:text-5xl`: tablet size
  - `lg:text-6xl`: desktop size

### Features Section
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-12">
    <div class="bg-white rounded-xl p-8 shadow-lg">
        <!-- Feature box content -->
    </div>
</div>
```
- Each feature box is contained in a `div`
- Update icons by changing `fas fa-clock` to other [Font Awesome icons](https://fontawesome.com/icons)
- Modify feature titles in `<h3>` tags
- Update descriptions in `<p>` tags

## Managing Links

### Internal Navigation Links
Current internal links use anchor tags (#):
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Ensure corresponding sections have matching IDs
2. Replace "#services" with new section IDs
3. Example adding new section:
```html
<section id="new-section">
    <!-- Content -->
</section>
<a href="#new-section">New Section</a>
```

### External Links
Current external links:
```html
<a href="https://www.efigueraspa.com/">Get Started Today</a>
```
To update:
1. Replace URL in `href` attribute
2. Maintain `https://` or `http://` prefix
3. Test links after updating

## Adding Privacy and Terms Pages

### Footer Link Updates
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html files
2. Update href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Responsive Design**
- Check for proper Tailwind breakpoint classes (md:, lg:)
- Ensure container class is present: `container mx-auto px-6`
- Verify grid classes match intended layout

2. **Missing Icons**
- Confirm Font Awesome CDN is loaded in `<head>`
- Check icon class names against Font Awesome documentation
- Use correct prefix (fas, far, fab)

3. **Navigation Issues**
- Verify ID attributes match href values
- Check for duplicate IDs (must be unique)
- Ensure smooth scroll behavior is working

### Best Practices
- Always test changes across multiple devices/screen sizes
- Maintain consistent spacing using Tailwind's spacing classes
- Keep color scheme consistent using Tailwind's color classes
- Back up files before making significant changes

Need additional help? Contact technical support or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).
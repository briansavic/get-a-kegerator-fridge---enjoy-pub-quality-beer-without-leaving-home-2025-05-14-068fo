# KegeratorPro Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the KegeratorPro landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold">KegeratorPro</a>
```
- Replace "KegeratorPro" with your desired company name
- The `text-2xl` class controls text size
- The `font-bold` class makes text bold

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
</div>
```
- Update text between `<a>` tags
- Keep the `href` attributes matching section IDs
- The `text-gray-600` class sets text color
- The `hover:text-gray-900` class changes color on hover

### Hero Section
```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight">Get a Kegerator Fridge & Enjoy Pub-Quality Beer Without Leaving Home</h1>
<p class="text-xl md:text-2xl text-gray-200 mb-8">Perfectly chilled, fresh draft beer to your kitchen or bar.</p>
```
- Update headline text between `<h1>` tags
- Modify subheading text between `<p>` tags
- `md:text-6xl` means text size changes on medium screens
- `mb-6` adds margin bottom spacing

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-gray-900 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-ruler text-2xl text-white"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Wide Range of Sizes</h3>
    <p class="text-gray-600">Find the perfect size for your space...</p>
</div>
```
To modify:
1. Change icon by updating `fa-ruler` to any [Font Awesome](https://fontawesome.com/icons) icon name
2. Update heading text between `<h3>` tags
3. Modify description text between `<p>` tags

## Managing Links

### Navigation Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```
To update:
1. Change `href="#sectionname"` to link to different sections
2. Ensure section IDs match (e.g., `id="features"` in target section)
3. For external links, use full URLs: `href="https://example.com"`

### Call-to-Action Buttons
Current shop links:
```html
<a href="https://briansavic.com" class="inline-flex items-center justify-center px-6 py-3 border border-transparent text-base font-medium rounded-md text-white bg-gray-900 hover:bg-gray-800 transition-all duration-300">
    Shop Now
</a>
```
To update:
1. Replace `https://briansavic.com` with your shop URL
2. Update button text between `<a>` tags
3. Maintain classes for consistent styling

### Footer Links
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-gray-300">About Us</a></li>
    <li><a href="#" class="hover:text-gray-300">Blog</a></li>
    <li><a href="#" class="hover:text-gray-300">Support</a></li>
</ul>
```
Replace `href="#"` with actual page URLs:
- Internal pages: `href="/about.html"`
- External links: `href="https://example.com"`

## Adding Privacy and Terms Pages

### Step 1: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h4 class="text-xl font-bold mb-4">Policies</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-gray-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-gray-300">Terms of Service</a></li>
        <li><a href="#" class="hover:text-gray-300">Shipping Policy</a></li>
    </ul>
</div>
```

Replace placeholder links:
```html
<li><a href="/privacy.html" class="hover:text-gray-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="hover:text-gray-300">Terms of Service</a></li>
```

### Step 2: Create Policy Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Use the same header and footer as `index.html`
3. Add policy content between header and footer

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Check that section IDs match href attributes
   - Ensure file names match exactly (case-sensitive)
   - Verify files are in the correct directory

2. **Styling Issues**
   - Confirm Tailwind CSS CDN link is working
   - Check for typos in class names
   - Verify responsive classes use correct breakpoints (e.g., `md:`, `lg:`)

3. **Icons Not Showing**
   - Verify Font Awesome CDN link is working
   - Check icon class names against Font Awesome documentation
   - Ensure proper icon style prefix (fas, far, fab)

Need additional help? Contact support at keg@me.com
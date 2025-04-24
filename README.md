# Albert Park Landing Page - Maintenance Guide

This guide will help you maintain and customize the Albert Park Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Albert Park <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a> <!-- Update text here -->
    <a href="#benefits">Benefits</a> <!-- Update text here -->
    <a href="#contact">Contact</a> <!-- Update text here -->
</div>
```

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Your financial success is our bottom line <!-- Update main headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Professional accounting services tailored to your business needs <!-- Update subheading here -->
</p>
```

### Tailwind CSS Class Guide
Common classes used throughout the page:

- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`
- Colors: `text-gray-100`, `text-gray-300`, `text-gray-400`
- Spacing: `mb-4`, `mt-8`, `py-24`, `px-6`
- Flex layout: `flex`, `items-center`, `justify-between`

Example of updating a button's appearance:
```html
<!-- Original button -->
<a href="#" class="px-6 py-2 bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">

<!-- To make button larger -->
<a href="#" class="px-8 py-3 bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">
```

## Managing Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
<a href="https://theaccountants.com">Get Started</a> <!-- External link to update -->
```

2. Call-to-Action Links:
```html
<a href="https://theaccountants.com">Get Started Now</a> <!-- Update this URL -->
<a href="mailto:support@example.com">Contact Us</a> <!-- Update email address -->
```

### Updating Links
To update any link:

1. Locate the `<a>` tag in the HTML
2. Modify the `href` attribute
3. For internal links (same page sections), use `#section-name`
4. For external links, use the full URL including `https://`

Example:
```html
<!-- Original -->
<a href="mailto:support@example.com">

<!-- Updated -->
<a href="mailto:contact@albertpark.com">
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new HTML files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Update the links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in IDs
   - Verify that section IDs are unique

2. **Responsive Design Issues**
   - Check that you've maintained the responsive classes (e.g., `md:`, `lg:`)
   - Test on different screen sizes
   - Don't remove the `container` class from main sections

3. **Gradient Text Not Showing**
   - Ensure these classes are present:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
     ```

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML using [W3C Validator](https://validator.w3.org/)
- Test all links after making changes
- Keep a backup of the original code before making modifications

Remember to always test your changes across different devices and browsers to ensure consistency in appearance and functionality.
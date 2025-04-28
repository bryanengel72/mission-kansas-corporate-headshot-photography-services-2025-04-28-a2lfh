# Landing Page Maintenance Guide
## For 101Headshots Website

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Name/Logo**
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    101Headshots <!-- Change this text to update company name -->
</a>
```

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a> <!-- Update text here -->
    <a href="#benefits">Benefits</a> <!-- Update text here -->
    <a href="#contact">Contact</a>   <!-- Update text here -->
</div>
```

### Hero Section
Located at the top of the page, featuring the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Mission, Kansas Corporate Headshot Photography Services <!-- Update main headline here -->
</h1>
```

#### Tailwind CSS Class Guide
- `text-4xl`: Large text on mobile
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `mb-8`: Adds margin bottom spacing
- `bg-gradient-to-r`: Creates right-flowing gradient

### Features Section
To modify feature cards:

1. Find the feature card container:
```html
<div class="bg-gray-900 rounded-2xl p-8 hover:scale-105 transition-transform duration-300 shadow-xl">
```

2. Update feature title and description:
```html
<h3 class="text-xl font-semibold mb-4">New Lights</h3> <!-- Feature title -->
<p class="text-gray-400">State-of-the-art lighting equipment...</p> <!-- Feature description -->
```

## Managing Links

### Navigation Links
All internal navigation links use anchor tags with hashtags (#) to scroll to specific sections:

```html
<!-- Current navigation links -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>

<!-- To update, ensure the href matches the section ID -->
<section id="features"> <!-- This ID must match the href above -->
```

### External Links
The main call-to-action buttons link to the booking website:

```html
<!-- Update this URL for the booking system -->
<a href="https://www.101headshots.com" class="inline-block px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">
```

### Email Links
Update email addresses in two locations:

```html
<!-- Contact section -->
<a href="mailto:bryan@101headshots.com">bryan@101headshots.com</a>

<!-- Footer section -->
<a href="mailto:bryan@101headshots.com">bryan@101headshots.com</a>
```

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Insert the following code in the footer's Quick Links section:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Add these new lines -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
        <!-- Existing links -->
        <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
    </ul>
</div>
```

### Step 2: Create New Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your privacy policy and terms content between them

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Ensure section IDs match exactly with href attributes
- Check for typos in IDs and hrefs
- Verify that section IDs are unique

2. **Responsive Design Issues**
- Check that you've maintained the responsive classes:
  - `md:` prefix for medium screens
  - `lg:` prefix for large screens
  - Don't remove `hidden md:flex` from navigation menu

3. **Gradient Text Not Showing**
- Ensure these classes remain together:
  ```html
  bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
  ```

### Need Help?
For additional assistance:
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML validity using [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always test changes across different devices and screen sizes before deploying to production.
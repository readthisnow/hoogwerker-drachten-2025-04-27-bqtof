# Hoogwerker Drachten Landing Page - Maintenance Guide

This guide will help you maintain and customize the Hoogwerker Drachten landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. **Company Name/Logo:**
```html
<a href="/" class="text-2xl font-bold text-blue-600">Hoogwerker Drachten</a>
```
- Replace "Hoogwerker Drachten" with your company name
- Adjust size using `text-2xl` (options: text-lg, text-xl, text-3xl)
- Change color using `text-blue-600` (options: text-red-600, text-green-600)

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Hoogwerker Drachten
    <span class="block text-blue-600 mt-2">Tijdelijk 10% Korting!</span>
</h1>
```

To modify:
1. Change main title text between the `<h1>` tags
2. Update promotional text in the `<span>` element
3. Adjust spacing using `mb-6` (margin-bottom) or `mt-2` (margin-top)

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-bold mb-4">Snelle Levering</h3>
    <p class="text-gray-600">Binnen 24 uur geleverd...</p>
</div>
```

To update:
1. Modify heading text in `<h3>` tags
2. Change description in `<p>` tags
3. Adjust padding using `p-8` (options: p-4, p-6, p-10)

## Managing Links

### Navigation Menu Links
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Kenmerken</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Voordelen</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Change `href="#section-name"` to point to your desired section
2. Update the link text between `<a>` tags
3. Ensure section IDs match your href values

### Call-to-Action (CTA) Links
Current CTA buttons point to "https://hansschuiling.nl". Update these:

```html
<a href="https://hansschuiling.nl" class="inline-block bg-blue-600 text-white font-semibold px-8 py-4 rounded-lg">
    Direct Reserveren
</a>
```

Replace the href value with your booking or contact page URL.

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the footer links section:

```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
</ul>
```

To add proper links:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Ensure section IDs match href values exactly
- Section IDs should not contain spaces
- Example: `href="#features"` matches `id="features"`

2. **Responsive Design Issues**
- Check responsive classes (md:, lg:) are properly set
- Example: `class="hidden md:flex"` hides on mobile, shows on medium screens
- Test on different screen sizes using browser dev tools

3. **Style Changes Not Working**
- Verify Tailwind CSS is properly loaded
- Check for typos in class names
- Use browser inspector to confirm styles are applied

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify all files are in the correct directory
3. Ensure all links use the correct relative or absolute paths
4. Test the page in multiple browsers

For additional support, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)

Remember to always backup your files before making significant changes!
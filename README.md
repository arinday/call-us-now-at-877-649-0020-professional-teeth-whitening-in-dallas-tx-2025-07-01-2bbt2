# Professional Teeth Whitening Landing Page - Maintenance Guide

This guide will help you maintain and customize the Professional Teeth Whitening landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your brand name and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<a href="/" class="text-blue-600 font-bold text-xl">BrightSmile</a>
```

To change the brand name:
1. Replace "BrightSmile" with your desired text
2. Adjust text size using Tailwind classes:
   - `text-xl` (current) - medium large
   - `text-2xl` - larger
   - `text-lg` - slightly smaller

### Hero Section
The main headline and call-to-action are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Professional Teeth Whitening in Dallas, TX
</h1>
```

To modify:
1. Replace the text between the `<h1>` tags
2. Responsive text sizes are defined as:
   - `text-4xl` - mobile devices
   - `md:text-5xl` - medium screens
   - `lg:text-6xl` - large screens

### Feature Cards
Each feature card follows this structure:

```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">15-Min Response</h3>
    <p class="text-gray-600">Quick response time to all your inquiries...</p>
</div>
```

To update:
1. Locate the feature section (search for `id="features"`)
2. Modify the `<h3>` text for titles
3. Update the `<p>` text for descriptions
4. Keep the existing classes for consistent styling

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600">FAQ</a>
    <a href="tel:8776490020" class="text-blue-600 font-semibold">...</a>
</div>
```

To update:
1. For internal links (same page):
   - Use `#section-id` format (e.g., `href="#services"`)
   - Ensure the referenced section has a matching `id` attribute
2. For external links:
   - Replace `href` with full URL (e.g., `href="https://example.com"`)
3. For phone numbers:
   - Use `tel:` format (e.g., `href="tel:1234567890"`)

### Call-to-Action Button
Update the appointment button link:

```html
<a href="https://professional-teeth-whitening-dallas-tx.netlify.app/" class="inline-block bg-blue-600...">
```

Replace the href with your actual booking page URL.

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

```html
<!-- Add this to the Quick Links section -->
<div>
    <h3 class="text-xl font-semibold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="/privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating New Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Check responsive classes start with:
     - `sm:` for small devices
     - `md:` for medium devices
     - `lg:` for large devices
   - Example: `class="text-xl md:text-2xl lg:text-3xl"`

3. **Missing Styles**
   - Verify Tailwind CDN is loaded:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```
   - Check for typos in class names
   - Tailwind classes must be exact matches

### Need Help?
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Check Tailwind documentation for [correct class names](https://tailwindcss.com/docs)
- Test responsiveness using browser developer tools

Remember to always test changes across different devices and browsers before publishing updates.
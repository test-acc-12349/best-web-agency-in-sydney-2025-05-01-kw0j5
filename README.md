# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the WebAgency landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu:

```html
<a href="/" class="text-2xl font-bold text-white hover:text-blue-400 transition duration-300">
    WebAgency
</a>
```

To update the company name:
1. Locate this code in the header section
2. Replace "WebAgency" with your desired text
3. Maintain the existing classes to preserve styling

### Hero Section
The main headline and subheading are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-400 to-purple-400 bg-clip-text text-transparent">
    Best Web Agency In Sydney
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Grow your business with clicks
</p>
```

To modify:
1. Replace the headline text while keeping the gradient effect classes
2. Update the subheading text within the paragraph tags
3. The responsive text sizes (text-4xl, md:text-5xl, lg:text-6xl) ensure proper scaling - maintain these unless you specifically want to change sizes

### Features Section
Each feature card follows this structure:

```html
<div class="bg-gray-700 rounded-2xl p-8 hover:transform hover:scale-105 transition duration-300">
    <div class="w-16 h-16 bg-blue-600 rounded-lg mb-6 flex items-center justify-center">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-bold mb-4">Easy to Use</h3>
    <p class="text-gray-300">Intuitive interface designed for seamless user experience and quick adoption.</p>
</div>
```

To update feature cards:
1. Locate the features section (`id="features"`)
2. Modify the h3 text for the feature title
3. Update the paragraph text for the description
4. Keep the existing classes for consistent styling and hover effects

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition duration-300">Benefits</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition duration-300">FAQ</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition duration-300">Contact</a>
</div>
```

To update links:
1. The `#` symbol indicates internal page links (anchors)
2. Ensure the href matches the corresponding section's id attribute
3. For external links, replace with full URLs (e.g., `href="https://example.com"`)

### Call-to-Action Links
Current CTA links point to "fixrr.online":

```html
<a href="https://fixrr.online" class="inline-flex items-center px-8 py-4 rounded-full bg-blue-600 hover:bg-blue-700 text-white font-bold text-lg transition duration-300 transform hover:scale-105">
```

To update:
1. Replace "https://fixrr.online" with your desired URL
2. Test the link after updating
3. Maintain the existing classes for proper styling

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - Check for typos in both the link and section ID
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These control how elements appear on different screen sizes
   - Test changes on mobile, tablet, and desktop views

3. **Style Inconsistencies**
   - Keep the existing color classes (e.g., `bg-gray-900`, `text-blue-400`)
   - Maintain hover effect classes (`hover:` prefixed classes)
   - Don't remove transition classes for smooth animations

Remember to:
- Always test changes in multiple browsers
- Check mobile responsiveness using browser dev tools
- Back up the original file before making changes
- Validate links after updating them

For additional help, refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.
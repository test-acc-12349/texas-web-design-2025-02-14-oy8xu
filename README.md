# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions to make common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>
```
- Change "TWD" to your desired text
- Adjust size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)

### Hero Section
The main banner section contains your primary heading and call-to-action buttons.

1. **Main Heading**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Best Websites In Texas
</h1>
```
- Replace "Best Websites In Texas" with your heading
- Size classes explained:
  - `text-4xl`: Default size on mobile
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

2. **Subheading**
```html
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Professional web design solutions tailored for Texas businesses
</p>
```
- Update the text while maintaining the classes
- `text-gray-600` controls text color (options: text-gray-400 through text-gray-900)

### Features Section
Each feature card uses consistent styling:

```html
<div class="p-8 bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-bold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included with every website package...</p>
</div>
```

To modify:
1. Change heading text inside `<h3>` tags
2. Update description text in the `<p>` tag
3. Keep classes intact for consistent styling

## Fixing Broken Links

### Navigation Menu Links
Current navigation links in the header:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Internal links (starting with #) connect to section IDs
2. Replace `href="#sectionname"` with your desired link
3. For external links, use complete URLs: `href="https://example.com"`

### Call-to-Action Links
Update the "Get Started" links:

```html
<!-- Find these instances -->
<a href="https://twd.com" class="...">Get Started</a>
```
Replace `https://twd.com` with your actual signup or contact page URL.

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:

```html
<div>
    <h4 class="text-lg font-semibold text-white mb-6">Legal</h4>
    <ul class="space-y-3">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html in your root directory
2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Ensure section IDs match exactly with href attributes
- Example: `href="#features"` must link to `<section id="features">`

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- These control how elements appear on different screen sizes

3. **Animation Problems**
- Check that AOS (Animate On Scroll) attributes are present:
```html
data-aos="fade-up"
data-aos-delay="100"
```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for class references
- Verify all scripts are loading properly in the browser console
- Test all links after making changes
- Maintain consistent spacing and indentation in your HTML

Remember to always backup your files before making changes, and test your updates across different devices and browsers.
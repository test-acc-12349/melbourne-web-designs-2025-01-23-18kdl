# Melbourne Web Designs - Landing Page Maintenance Guide

This guide will help you maintain and customize the Melbourne Web Designs landing page. Follow these instructions carefully to make updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text (MWD)**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">MWD</a>
```
- Replace "MWD" with your desired text
- Keep the classes to maintain the gradient effect

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <!-- More menu items -->
</div>
```
- Update text between `>` and `</a>` tags
- Keep `hidden md:flex` to maintain mobile responsiveness

### Hero Section
Located at the top of the page:
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">Best Websites In Melbourne</h1>
```
- Update heading text while maintaining the gradient classes
- The responsive text sizes are:
  - Mobile: `text-5xl`
  - Tablet: `md:text-6xl`
  - Desktop: `lg:text-7xl`

### Features Section
To modify feature cards:
```html
<div class="p-8 rounded-2xl bg-white border border-gray-100 hover:shadow-xl transition-all duration-300 group hover:-translate-y-1">
    <!-- Icon container -->
    <h3 class="text-xl font-semibold mb-4">Custom Designs</h3>
    <p class="text-gray-600">Unique, tailored designs...</p>
</div>
```
- Update headings and descriptions
- Maintain the hover effects with `hover:` classes
- Keep the `group` class for synchronized hover effects

## Fixing Broken Links

### Current Link Structure
1. **Navigation Links**
```html
<!-- Replace these href values -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
- Internal section links start with #
- Update href attributes to match your section IDs

2. **Call-to-Action Links**
```html
<!-- Find and replace all instances of -->
<a href="https://mwd.com">Get Started</a>
```
- Replace `https://mwd.com` with your actual website URL
- Maintain consistent URLs across all CTA buttons

3. **Footer Links**
```html
<!-- Services section -->
<ul class="space-y-2">
    <li><a href="#">Web Design</a></li>
    <!-- More services -->
</ul>
```
- Replace `#` with actual page URLs
- Ensure all footer links point to valid pages

## Linking Privacy and Terms Pages

### Adding Policy Links
1. **Locate the Legal Section in Footer**
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

2. **Update href attributes:**
```html
<!-- Change to -->
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Gradients**
- If gradients disappear, ensure these classes remain intact:
```html
bg-gradient-to-r from-purple-600 to-blue-500
```

2. **Mobile Menu Issues**
- Check that `hidden md:flex` is present on the navigation menu
- This hides the menu on mobile and shows it on larger screens

3. **Hover Effects Not Working**
- Verify the presence of:
  - `transition-all`
  - `duration-300`
  - `hover:` classes

4. **Responsive Design Problems**
- Maintain responsive classes:
  - `md:` for tablet
  - `lg:` for desktop
  - Base classes for mobile

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify all links using your browser's developer tools
- Test the page across different devices and screen sizes

Remember to always backup your files before making changes and test thoroughly after updates.
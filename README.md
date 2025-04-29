# Texas Websites Landing Page - Maintenance Guide

This README provides detailed instructions for maintaining and customizing your Texas Websites landing page. This guide is designed for beginners with no prior coding knowledge.

## Table of Contents

1. [Introduction](#introduction)
2. [File Structure](#file-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Managing Navigation Links](#managing-navigation-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Customizing the Hero Section](#customizing-the-hero-section)
8. [Modifying Feature Cards](#modifying-feature-cards)
9. [Updating Benefits Section](#updating-benefits-section)
10. [Customizing the CTA Section](#customizing-the-cta-section)
11. [Managing Testimonials](#managing-testimonials)
12. [Troubleshooting](#troubleshooting)
13. [Additional Resources](#additional-resources)

## Introduction

This landing page is built using:
- HTML5 for structure
- Tailwind CSS for styling (loaded via CDN)
- Font Awesome for icons
- Alpine.js for interactive elements (like the mobile menu)

No backend programming or database is required to make basic changes to this page.

## File Structure

The landing page consists of:
- `index.html` - The main HTML file (what you're editing)
- External resources loaded via CDN (no local files to manage)

## Updating Text Content

### Updating the Page Title

The page title appears in browser tabs and search results. To update it:

1. Locate this line in the `<head>` section (around line 7):
   ```html
   <title>Best Websites In Texas | Custom Websites For Your Business</title>
   ```
2. Replace the text between the `<title>` tags with your preferred title.

### Updating the Header Logo Text

To change the logo text in the header:

1. Find this section in the header (around line 23):
   ```html
   <a href="#" class="text-2xl font-bold text-blue-600">
       <span class="text-gray-900">Texas</span>Websites
   </a>
   ```
2. Update the text inside the `<span>` tag (currently "Texas") and the text after it (currently "Websites").

### Updating the Hero Section

To modify the main headline and subheadline:

1. Locate the hero section (around line 66):
   ```html
   <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
       Best Websites In Texas
   </h1>
   <p class="text-xl md:text-2xl lg:text-3xl text-gray-600 font-light mb-10">
       Custom Websites For Your Business
   </p>
   ```
2. Replace the text between the `<h1>` tags for the main headline.
3. Replace the text between the `<p>` tags for the subheadline.

### Updating Feature Cards

To change the feature card content:

1. Find the features section (starting around line 136).
2. For each feature card, you can update:
   - The icon (using Font Awesome classes)
   - The heading (between `<h3>` tags)
   - The description (between `<p>` tags)
   - The bullet points (inside the `<li>` elements)

For example, to update the first feature card:

```html
<div class="bg-white rounded-xl shadow-lg hover:shadow-xl p-8 transition duration-300 transform hover:scale-105 border border-gray-100">
    <div class="w-14 h-14 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-mouse-pointer text-blue-600 text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-3">Easy to Use</h3>
    <p class="text-gray-600 mb-4">Intuitive interfaces and user-friendly designs make managing your website simple, even for beginners.</p>
    <!-- Bullet points below -->
</div>
```

## Modifying Tailwind CSS Classes

Tailwind CSS uses utility classes to style elements. Here's how to modify common styling:

### Understanding Key Tailwind Classes

- Text color: `text-{color}-{shade}` (e.g., `text-blue-600`)
- Background color: `bg-{color}-{shade}` (e.g., `bg-gray-50`)
- Text size: `text-{size}` (e.g., `text-xl`)
- Spacing: `m-{size}` (margin), `p-{size}` (padding)
- Responsive prefixes: `sm:`, `md:`, `lg:` (e.g., `md:text-4xl`)

### Changing Colors

To change the primary blue color to green throughout the page:

1. Find all instances of `blue-600` and replace with `green-600`
2. Find all instances of `blue-100` and replace with `green-100`
3. Find all instances of `blue-50` and replace with `green-50`

For example, to change the button color:

```html
<!-- Original blue button -->
<a href="https://sigmaseo.io" class="px-8 py-4 bg-blue-600 hover:bg-blue-700 text-white rounded-lg shadow-lg hover:shadow-xl font-medium transition duration-300 transform hover:scale-105 text-lg">
    Get Started Today
</a>

<!-- Changed to green button -->
<a href="https://sigmaseo.io" class="px-8 py-4 bg-green-600 hover:bg-green-700 text-white rounded-lg shadow-lg hover:shadow-xl font-medium transition duration-300 transform hover:scale-105 text-lg">
    Get Started Today
</a>
```

### Changing Text Size

To make text larger or smaller:

1. Find the element with the text you want to change
2. Look for classes like `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
3. Replace with your desired size

Size options from smallest to largest:
`text-xs`, `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`, `text-3xl`, `text-4xl`, `text-5xl`, `text-6xl`

### Changing Spacing

To adjust spacing (margin or padding):

1. Find classes starting with `m-` (margin) or `p-` (padding)
2. Change the number that follows (0-12, where higher numbers mean more space)

For example:
```html
<!-- Original spacing -->
<div class="mb-6">Content</div>

<!-- Increased spacing -->
<div class="mb-10">Content</div>
```

## Managing Navigation Links

### Updating Navigation Menu Items

The navigation menu appears in both desktop and mobile views. To update it:

1. Locate the desktop navigation (around line 28):
   ```html
   <nav class="hidden md:flex space-x-10">
       <a href="#features" class="text-base font-medium text-gray-700 hover:text-blue-600 transition duration-300">Features</a>
       <a href="#benefits" class="text-base font-medium text-gray-700 hover:text-blue-600 transition duration-300">Benefits</a>
       <a href="#faq" class="text-base font-medium text-gray-700 hover:text-blue-600 transition duration-300">FAQ</a>
       <a href="#contact" class="text-base font-medium text-gray-700 hover:text-blue-600 transition duration-300">Contact</a>
   </nav>
   ```

2. Also locate the mobile navigation (around line 53):
   ```html
   <div class="md:hidden" x-show="isOpen">
       <div class="px-2 pt-2 pb-4 space-y-1 sm:px-3">
           <a href="#features" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-blue-600 hover:bg-gray-50 transition duration-300">Features</a>
           <a href="#benefits" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-blue-600 hover:bg-gray-50 transition duration-300">Benefits</a>
           <a href="#faq" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-blue-600 hover:bg-gray-50 transition duration-300">FAQ</a>
           <a href="#contact" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-blue-600 hover:bg-gray-50 transition duration-300">Contact</a>
           <a href="https://sigmaseo.io" class="block px-3 py-2 rounded-md text-base font-medium text-white bg-blue-600 hover:bg-blue-700 transition duration-300">Get Started</a>
       </div>
   </div>
   ```

3. To update both menus:
   - Change the text between the `<a>` tags to update the menu label
   - Change the `href` attribute to update where the link points to

4. **Important**: You must update both the desktop and mobile menus to maintain consistency.

### Fixing Broken Links

The page contains several links that need to be updated:

1. **Navigation Menu Links**: These use `#section-id` format to link to sections on the same page
   - `#features` - Links to the features section
   - `#benefits` - Links to the benefits section
   - `#faq` - This link is broken as there's no FAQ section with this ID
   - `#contact` - This link is broken as there's no contact section with this ID

2. **Call-to-Action Links**: These link to an external website
   - All instances of `https://sigmaseo.io` should be updated to your actual website or desired URL

To fix the broken `#faq` and `#contact` links:

1. Either create these missing sections with matching IDs, or
2. Remove these links from both desktop and mobile navigation menus, or
3. Update the links to point to existing sections

For example, to add a FAQ section:
```html
<section id="faq" class="py-20 bg-white">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
            <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">Frequently Asked Questions</h2>
            <p class="text-xl text-gray-600 max-w-3xl mx-auto">Find answers to common questions about our website services.</p>
        </div>
        <!-- Add FAQ content here -->
    </div>
</section>
```

## Adding Privacy and Terms Pages

To add links to Privacy Policy and Terms of Service pages:

1. First, create your `privacy.html` and `terms.html` files in the same directory as your `index.html`

2. Add a footer section to your `index.html` before the closing `</body>` tag:

```html
<!-- Footer Section -->
<footer class="bg-gray-800 text-white py-12">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
            <!-- Company Info -->
            <div class="col-span-1 md:col-span-2">
                <a href="#" class="text-2xl font-bold text-white">
                    <span class="text-blue-400">Texas</span>Websites
                </a>
                <p class="mt-4 text-gray-400">Custom websites for businesses across Texas.</p>
            </div>
            
            <!-- Quick Links -->
            <div class="col-span-1">
                <h3 class="text-lg font-semibold mb-4">Quick Links</h3>
                <ul class="space-y-2">
                    <li><a href="#features" class="text-gray-400 hover:text-white transition duration-300">Features</a></li>
                    <li><a href="#benefits" class="text-gray-400 hover:text-white transition duration-300">Benefits</a></li>
                </ul>
            </div>
            
            <!-- Legal Links -->
            <div class="col-span-1">
                <h3 class="text-lg font-semibold mb-4">Legal</h3>
                <ul class="space-y-2">
                    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
                    <li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
                </ul>
            </div>
        </div>
        
        <div class="border-t border-gray-700 mt-12 pt-8 text-center text-gray-400">
            <p>&copy; 2023 Texas Websites. All rights reserved.</p>
        </div>
    </div>
</footer>
```

3. Ensure your `privacy.html` and `terms.html` files include navigation back to the main page:

```html
<!-- In privacy.html and terms.html -->
<a href="index.html" class="text-blue-600 hover:text-blue-800">← Back to Home</a>
```

## Customizing the Hero Section

The hero section is the first thing visitors see. To customize it:

1. Find the hero section (around line 65):
   ```html
   <section class="relative bg-gradient-to-r from-blue-50 to-indigo-50 py-20 md:py-28 lg:py-32 overflow-hidden">
   ```

2. To change the background gradient:
   - Modify `from-blue-50 to-indigo-50` to your preferred colors
   - For example: `from-green-50 to-teal-50`

3. To update the call-to-action buttons:
   ```html
   <div class="flex flex-col sm:flex-row justify-center gap-4">
       <a href="https://sigmaseo.io" class="px-8 py-4 bg-blue-600 hover:bg-blue-700 text-white rounded-lg shadow-lg hover:shadow-xl font-medium transition duration-300 transform hover:scale-105 text-lg">
           Get Started Today
       </a>
       <a href="#features" class="px-8 py-4 bg-white hover:bg-gray-100 text-blue-600 rounded-lg shadow-md hover:shadow-lg font-medium transition duration-300 transform hover:scale-105 text-lg border border-gray-200">
           Learn More
       </a>
   </div>
   ```
   - Change the button text between the `<a>` tags
   - Update the `href` attributes to point to your desired URLs
   - Modify colors by changing classes like `bg-blue-600` and `text-blue-600`

## Modifying Feature Cards

The Features section contains three cards highlighting key features. To modify them:

1. Locate the features section (around line 136)

2. For each feature card, you can change:

   a. The icon:
   ```html
   <i class="fas fa-mouse-pointer text-blue-600 text-2xl"></i>
   ```
   - Replace `fa-mouse-pointer` with any [Font Awesome icon](https://fontawesome.com/icons)
   - For example: `fa-rocket`, `fa-chart-bar`, `fa-shield-alt`

   b. The heading:
   ```html
   <h3 class="text-xl font-bold text-gray-900 mb-3">Easy to Use</h3>
   ```
   
   c. The description:
   ```html
   <p class="text-gray-600 mb-4">Intuitive interfaces and user-friendly designs make managing your website simple, even for beginners.</p>
   ```
   
   d. The bullet points:
   ```html
   <ul class="space-y-2">
       <li class="flex items-center">
           <svg class="w-5 h-5 text-blue-500 mr-2" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
               <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
           </svg>
           <span class="text-gray-600">User-friendly admin panel</span>
       </li>
       <!-- More list items -->
   </ul>
   ```
   - Update the text inside each `<span>` tag
   - Add or remove `<li>` elements to change the number of bullet points

3. To add a fourth feature card, copy an existing card and paste it after the third card, then update its content.

## Updating Benefits Section

The Benefits section works similarly to the Features section:

1. Find the benefits section (around line 198)

2. For each benefit card, you can update:
   - The icon (inside the `<i>` tag)
   - The heading (inside the `<h3>` tag)
   - The description (inside the `<p>` tag)

3. To change the "Learn more" link:
   ```html
   <div class="flex items-center text-blue-600 font-medium">
       <span>Learn more</span>
       <svg class="w-5 h-5 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
           <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path>
       </svg>
   </div>
   ```
   - Update the text inside the `<span>` tag
   - To make this an actual link, change it to:
   ```html
   <a href="your-url.html" class="flex items-center text-blue-600 font-medium">
       <span>Learn more</span>
       <svg class="w-5 h-5 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
           <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path>
       </svg>
   </a>
   ```

## Customizing the CTA Section

The Call-to-Action (CTA) section encourages visitors to take action:

1. Locate the CTA section (around line 238):
   ```html
   <section class="py-20 bg-gradient-to-r from-blue-600 to-indigo-700 relative overflow-hidden">
   ```

2. To change the background image:
   ```html
   <div class="absolute inset-0 opacity-10">
       <img src="https://images.unsplash.com/photo-1497366754035-f200968a6e72?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80" alt="Office workspace" class="w-full h-full object-cover" />
   </div>
   ```
   - Replace the `src` attribute with your image URL
   - Adjust the `opacity-10` class to make the image more or less visible (higher number = more visible)

3. To update the heading and description:
   ```html
   <h2 class="text-3xl md:text-4xl font-bold text-white mb-6">Ready to Transform Your Online Presence?</h2>
   <p class="text-xl text-blue-100 mb-10">Join hundreds of Texas businesses that have boosted their growth with our custom websites.</p>
   ```

4. To change the CTA button:
   ```html
   <a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-white text-blue-600 rounded-lg shadow-lg hover:shadow-xl font-medium transition duration-300 transform hover:scale-105 text-lg">
       Get Your Custom Website Today
   </a>
   ```
   - Update the text between the `<a>` tags
   - Change the `href` attribute to your desired URL

## Managing Testimonials

The Testimonials section showcases client feedback:

1. Find the testimonials section (around line 261)

2. For each testimonial, you can update:

   a. The star rating (if needed):
   ```html
   <div class="text-yellow-400 flex">
       <i class="fas fa-star"></i>
       <i class="fas fa-star"></i>
       <i class="fas fa-star"></i>
       <i class="fas fa-star"></i>
       <i class="fas fa-star"></i>
   </div>
   ```
   - For a 4-star rating, remove one `<i class="fas fa-star"></i>` line
   - For a half-star, use `<i class="fas fa-star-half-alt"></i>`

   b. The testimonial text:
   ```html
   <p class="text-gray-600 mb-6 italic">"Our website traffic has increased by 150% since launching our new site. The design is clean, modern, and perfectly represents our brand."</p>
   ```

   c. The client information:
   ```html
   <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center mr-4">
       <span class="text-blue-600 font-bold">JD</span>
   </div>
   <div>
       <h4 class="font-bold text-gray-900">John Doe</h4>
       <p class="text-gray-500 text-sm">CEO, Austin Tech Solutions</p>
   </div>
   ```
   - Update the initials inside the `<span>` tag
   - Change the name inside the `<h4>` tag
   - Update the title/company inside the `<p>` tag

3. To add more testimonials, copy an existing testimonial card and paste it within the grid.

## Troubleshooting

### Common Issues and Solutions

1. **Mobile Menu Not Working**
   - Check that Alpine.js is properly loaded via the CDN
   - Ensure the `x-data` and `x-show` attributes are correctly set

2. **Styles Not Applying**
   - Verify the Tailwind CSS CDN link is working
   - Check for typos in class names
   - Remember that Tailwind classes must be exact (e.g., `text-blue-600` not `text-blue`)

3. **Icons Not Displaying**
   - Ensure the Font Awesome CDN link is working
   - Verify the icon class names (e.g., `fa-star` not `fa-stars`)

4. **Links Not Working**
   - For internal links (starting with `#`), ensure the ID exists in the HTML
   - For external links, make sure the URL is complete (including `https://`)

### Testing Your Changes

Always test your changes in multiple browsers and on different devices to ensure:
- The page looks good on desktop, tablet, and mobile
- All links work correctly
- Images load properly
- The mobile menu opens and closes as expected

## Additional Resources

- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Font Awesome Icons Gallery](https://fontawesome.com/icons)
- [Alpine.js Documentation](https://alpinejs.dev/start-here)
- [HTML Tutorial](https://www.w3schools.com/html/)

---

This README covers the basics of maintaining and customizing your Texas Websites landing page. If you need more advanced customizations, consider consulting with a web developer.
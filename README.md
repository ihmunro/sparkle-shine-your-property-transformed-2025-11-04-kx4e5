# Sparkle & Shine Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing your Sparkle & Shine landing page. This document provides step-by-step instructions for developers of all skill levels.

---

## Table of Contents

1. [Overview](#overview)
2. [File Structure & Setup](#file-structure--setup)
3. [Updating Text Content](#updating-text-content)
4. [Understanding & Modifying Tailwind CSS Classes](#understanding--modifying-tailwind-css-classes)
5. [Fixing & Updating Links](#fixing--updating-links)
6. [Creating Privacy & Terms Pages](#creating-privacy--terms-pages)
7. [Responsive Design Considerations](#responsive-design-considerations)
8. [Troubleshooting Common Issues](#troubleshooting-common-issues)
9. [Best Practices for Maintenance](#best-practices-for-maintenance)

---

## Overview

The Sparkle & Shine landing page is built using:

- **HTML5**: Structure and semantic markup
- **Tailwind CSS**: Utility-first CSS framework for styling (via CDN)
- **Font Awesome**: Icon library for visual elements
- **Google Fonts**: Custom typography (Poppins and Playfair Display)
- **Vanilla JavaScript**: Interactive features like mobile menu and FAQ accordion

### Key Features of This Landing Page

- **Sticky Navigation Header**: Remains visible while scrolling
- **Hero Section**: Eye-catching introduction with gradient effects
- **Features Section**: Three main service highlights
- **Benefits Section**: Real-world advantages with statistics
- **Testimonials**: Client feedback carousel
- **FAQ Accordion**: Expandable frequently asked questions
- **About Section**: Company information and values
- **Call-to-Action Section**: Final conversion opportunity
- **Footer**: Navigation, links, and contact information

---

## File Structure & Setup

### Recommended Project Structure

```
project-folder/
├── index.html                 (Main landing page - what you have)
├── privacy.html               (Privacy Policy page - you'll create this)
├── terms.html                 (Terms of Service page - you'll create this)
├── blog.html                  (Optional blog page)
├── css/
│   └── custom.css             (Optional custom styles)
├── js/
│   └── custom.js              (Optional additional JavaScript)
└── images/
    └── (your images here)
```

### Opening & Editing Your File

**Using a Code Editor:**

1. Download and install a code editor:
   - [Visual Studio Code](https://code.microsoft.com/) (Recommended)
   - [Sublime Text](https://www.sublimetext.com/)
   - [Atom](https://atom.io/)

2. Open your project folder in the editor
3. Open `index.html` to start editing

**To preview your changes:**
- Right-click on `index.html` → "Open with" → Choose your browser
- Or drag the file into your browser window
- Refresh the page (Ctrl+R or Cmd+R) after making changes

---

## Updating Text Content

This section shows you exactly where to find and change all the text on your landing page.

### 1. Header Navigation & Logo

**Location**: Lines 42-75 (inside the `<header>` tag)

**What to change:**

```html
<!-- CURRENT CODE -->
<span class="text-xl font-bold gradient-text">Sparkle & Shine</span>

<!-- CHANGE TO YOUR BUSINESS NAME -->
<span class="text-xl font-bold gradient-text">Your Business Name</span>
```

**Navigation Menu Items:**

```html
<!-- CURRENT CODE (Lines 53-60) -->
<a href="#features" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Benefits</a>
<a href="#testimonials" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Testimonials</a>
<a href="#faq" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">FAQ</a>
<a href="#about" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">About</a>

<!-- ADD, REMOVE, OR MODIFY MENU ITEMS AS NEEDED -->
<!-- Example: Adding a new "Services" link -->
<a href="#services" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Services</a>
```

**Pro Tip**: The `#features`, `#benefits`, etc. are anchor links that jump to sections with matching `id` attributes. Keep them consistent!

---

### 2. Hero Section (Main Banner)

**Location**: Lines 85-145

**Headline:**

```html
<!-- CURRENT CODE (Line 92) -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight">
    <span class="gradient-text">Sparkle & Shine:</span> Your Property Transformed
</h1>

<!-- CHANGE TO -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight">
    <span class="gradient-text">Your Company Name:</span> Your New Headline
</h1>
```

**Subheading (Description):**

```html
<!-- CURRENT CODE (Lines 95-98) -->
<p class="text-lg md:text-xl text-gray-600 leading-relaxed">
    Give your home or business the radiant glow it deserves with our professional 
    painting and cleaning services. We combine expert craftsmanship with meticulous 
    attention to detail to create spaces that truly shine.
</p>

<!-- CHANGE TO YOUR DESCRIPTION -->
<p class="text-lg md:text-xl text-gray-600 leading-relaxed">
    Your new description here. Keep it 2-3 sentences and focus on the main benefit.
</p>
```

**Call-to-Action Buttons:**

```html
<!-- CURRENT CODE (Lines 99-112) -->
<a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank" rel="noopener noreferrer" 
   class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-8 py-4 rounded-lg font-bold text-lg hover:shadow-xl hover:scale-105 transition-all duration-300 text-center">
    Transform Your Space Today
</a>

<!-- CHANGE BUTTON TEXT AND LINK -->
<a href="https://your-website.com" target="_blank" rel="noopener noreferrer" 
   class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-8 py-4 rounded-lg font-bold text-lg hover:shadow-xl hover:scale-105 transition-all duration-300 text-center">
    Your Button Text Here
</a>
```

**Hero Statistics:**

```html
<!-- CURRENT CODE (Lines 122-131) -->
<div class="bg-white rounded-lg p-4 text-center shadow-md">
    <p class="text-2xl font-bold gradient-text">500+</p>
    <p class="text-sm text-gray-600">Projects Completed</p>
</div>

<!-- CHANGE TO YOUR STATISTICS -->
<div class="bg-white rounded-lg p-4 text-center shadow-md">
    <p class="text-2xl font-bold gradient-text">1000+</p>
    <p class="text-sm text-gray-600">Your Statistic Label</p>
</div>
```

---

### 3. Features Section

**Location**: Lines 155-239

**Section Title:**

```html
<!-- CURRENT CODE (Line 160) -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 tracking-tight">
    Why Choose Our Services?
</h2>

<!-- CHANGE TO -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 tracking-tight">
    Your New Section Title
</h2>
```

**Feature Cards** (There are 3 feature cards):

```html
<!-- FEATURE 1: CURRENT CODE (Lines 175-194) -->
<div class="group bg-white rounded-2xl p-8 shadow-md hover:shadow-2xl hover:scale-105 transition-all duration-300 cursor-pointer border border-gray-100">
    <div class="w-16 h-16 bg-gradient-to-br from-purple-600 to-pink-600 rounded-xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform duration-300">
        <i class="fas fa-clock text-white text-2xl"></i>
    </div>
    <h3 class="text-2xl font-bold mb-3">Fast Project Completion</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        We understand that your time is valuable...
    </p>
    <!-- Bullet points below -->
</div>

<!-- TO CHANGE: -->
<!-- 1. Change the icon: Replace "fas fa-clock" with another Font Awesome icon -->
<!-- 2. Change the title: Replace "Fast Project Completion" -->
<!-- 3. Change the description paragraph -->
<!-- 4. Update the bullet points in the <ul> -->
```

**Finding Different Icons:**
- Visit [Font Awesome Icons](https://fontawesome.com/icons) 
- Search for an icon you like
- Copy the icon name (e.g., `fa-star`, `fa-heart`, `fa-rocket`)
- Replace in your code: `<i class="fas fa-YOUR-ICON-NAME text-white text-2xl"></i>`

**Example - Changing Feature 1 to a different icon:**

```html
<!-- ORIGINAL -->
<i class="fas fa-clock text-white text-2xl"></i>

<!-- CHANGE TO ROCKET ICON -->
<i class="fas fa-rocket text-white text-2xl"></i>

<!-- CHANGE TO STAR ICON -->
<i class="fas fa-star text-white text-2xl"></i>
```

---

### 4. Benefits Section

**Location**: Lines 248-350

**Section Title:**

```html
<!-- CURRENT CODE (Line 253) -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 tracking-tight">
    Transform Your Space with Real Results
</h2>

<!-- CHANGE TO -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 tracking-tight">
    Your New Benefits Title
</h2>
```

**Benefit Cards** (There are 3 main benefit cards):

```html
<!-- BENEFIT 1: CURRENT CODE (Lines 267-285) -->
<div class="relative group">
    <div class="relative bg-gradient-to-br from-blue-50 to-indigo-50 rounded-2xl p-8 border border-blue-100 hover:border-purple-300 transition-colors duration-300">
        <div class="w-14 h-14 bg-gradient-to-br from-purple-600 to-pink-600 rounded-xl flex items-center justify-center mb-6">
            <i class="fas fa-diamond text-white text-2xl"></i>
        </div>
        <h3 class="text-2xl font-bold mb-3">Lasting Beauty</h3>
        <p class="text-gray-700 leading-relaxed">
            Our high-quality materials and expert application...
        </p>
    </div>
</div>
```

**To customize benefits:**

1. **Change the icon**: Replace `fa-diamond` with any Font Awesome icon
2. **Change the title**: Replace "Lasting Beauty"
3. **Change the description**: Replace the paragraph text
4. **Change the background color** (optional):
   - `from-blue-50 to-indigo-50` → `from-green-50 to-emerald-50`
   - `border-blue-100` → `border-green-100`

**Statistics Grid** (Lines 325-348):

```html
<!-- CURRENT CODE -->
<div class="text-center p-6 rounded-xl bg-gray-50 hover:bg-purple-50 transition-colors duration-300">
    <div class="text-3xl font-bold gradient-text mb-2">10+ Years</div>
    <p class="text-gray-600">Industry Experience</p>
</div>

<!-- CHANGE TO -->
<div class="text-center p-6 rounded-xl bg-gray-50 hover:bg-purple-50 transition-colors duration-300">
    <div class="text-3xl font-bold gradient-text mb-2">15+ Years</div>
    <p class="text-gray-600">Your Statistic Label</p>
</div>
```

---

### 5. Testimonials Section

**Location**: Lines 357-439

**Section Title:**

```html
<!-- CURRENT CODE (Line 362) -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 tracking-tight">
    What Our Clients Say
</h2>

<!-- CHANGE TO -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 tracking-tight">
    Client Testimonials
</h2>
```

**Individual Testimonial Cards** (There are 4 testimonials):

```html
<!-- TESTIMONIAL 1: CURRENT CODE (Lines 378-398) -->
<div class="bg-white rounded-xl p-6 shadow-md hover:shadow-xl transition-all duration-300 hover:scale-105">
    <div class="flex items-center mb-4">
        <div class="w-12 h-12 bg-gradient-to-br from-purple-600 to-pink-600 rounded-full flex items-center justify-center text-white font-bold">
            JM
        </div>
        <div class="ml-4">
            <p class="font-bold text-gray-900">Jennifer Martinez</p>
            <p class="text-sm text-gray-600">Homeowner, Vancouver</p>
        </div>
    </div>
    <div class="flex items-center mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
    </div>
    <p class="text-gray-700 leading-relaxed">
        "Sparkle & Shine completely transformed my living room!..."
    </p>
</div>

<!-- TO CHANGE TESTIMONIAL: -->
<!-- 1. Change "JM" to client's initials -->
<!-- 2. Change "Jennifer Martinez" to client's name -->
<!-- 3. Change "Homeowner, Vancouver" to client's title/location -->
<!-- 4. Adjust star count (remove or add <i> tags for different ratings) -->
<!-- 5. Replace the testimonial quote -->
```

**Reducing Star Rating:**

```html
<!-- 5-STAR RATING (CURRENT) -->
<i class="fas fa-star text-yellow-400"></i>
<i class="fas fa-star text-yellow-400"></i>
<i class="fas fa-star text-yellow-400"></i>
<i class="fas fa-star text-yellow-400"></i>
<i class="fas fa-star text-yellow-400"></i>

<!-- 4-STAR RATING -->
<i class="fas fa-star text-yellow-400"></i>
<i class="fas fa-star text-yellow-400"></i>
<i class="fas fa-star text-yellow-400"></i>
<i class="fas fa-star text-yellow-400"></i>

<!-- 3-STAR RATING -->
<i class="fas fa-star text-yellow-400"></i>
<i class="fas fa-star text-yellow-400"></i>
<i class="fas fa-star text-yellow-400"></i>
```

---

### 6. FAQ Section

**Location**: Lines 448-560

**Section Title:**

```html
<!-- CURRENT CODE (Line 453) -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 tracking-tight">
    Frequently Asked Questions
</h2>

<!-- CHANGE TO -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 tracking-tight">
    Your FAQ Title
</h2>
```

**FAQ Items** (There are 5 questions):

```html
<!-- FAQ ITEM 1: CURRENT CODE (Lines 467-483) -->
<div class="faq-item border border-gray-200 rounded-xl overflow-hidden hover:border-purple-300 transition-colors duration-300">
    <div class="faq-question cursor-pointer p-6 bg-gray-50 hover:bg-purple-50 transition-colors duration-300 flex items-center justify-between">
        <h3 class="text-lg font-bold text-gray-900">
            How long does a typical painting project take?
        </h3>
        <i class="faq-icon fas fa-chevron-down text-purple-600 transition-transform duration-300"></i>
    </div>
    <div class="faq-answer hidden p-6 bg-white border-t border-gray-200">
        <p class="text-gray-700 leading-relaxed">
            The duration of a painting project depends on several factors...
        </p>
    </div>
</div>

<!-- TO CHANGE FAQ: -->
<!-- 1. Replace the question text: "How long does a typical painting project take?" -->
<!-- 2. Replace the answer text in the <p> tag -->
<!-- 3. Add new FAQ items by copying this entire <div> block -->
```

**Adding a New FAQ Item:**

```html
<!-- COPY THIS ENTIRE BLOCK and paste it before the closing </div> of the FAQ section -->
<div class="faq-item border border-gray-200 rounded-xl overflow-hidden hover:border-purple-300 transition-colors duration-300">
    <div class="faq-question cursor-pointer p-6 bg-gray-50 hover:bg-purple-50 transition-colors duration-300 flex items-center justify-between">
        <h3 class="text-lg font-bold text-gray-900">
            Your New Question Here?
        </h3>
        <i class="faq-icon fas fa-chevron-down text-purple-600 transition-transform duration-300"></i>
    </div>
    <div class="faq-answer hidden p-6 bg-white border-t border-gray-200">
        <p class="text-gray-700 leading-relaxed">
            Your answer here. This can be multiple sentences.
        </p>
    </div>
</div>
```

---

### 7. About Section

**Location**: Lines 568-620

**Section Title:**

```html
<!-- CURRENT CODE (Line 573) -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 tracking-tight">
    About Sparkle & Shine
</h2>

<!-- CHANGE TO -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 tracking-tight">
    About [Your Company Name]
</h2>
```

**About Paragraphs:**

```html
<!-- CURRENT CODE (Lines 582-593) -->
<p>
    Sparkle & Shine was founded in 2014 by a team of passionate professionals...
</p>
<p>
    At Sparkle & Shine, we believe that every property deserves to look and feel its best...
</p>

<!-- REPLACE WITH YOUR COMPANY STORY -->
<p>
    [Your company name] was founded in [year] by [founder name(s)]...
</p>
<p>
    At [Your company name], we believe that [your mission statement]...
</p>
```

**About Section Cards** (Lines 607-619):

```html
<!-- CURRENT CODE -->
<div class="text-center p-6 bg-white rounded-xl shadow-md">
    <i class="fas fa-award text-4xl gradient-text mb-4"></i>
    <h3 class="text-xl font-bold mb-2">Award-Winning Service</h3>
    <p class="text-gray-600">Recognized for excellence and customer satisfaction</p>
</div>

<!-- CHANGE TO -->
<div class="text-center p-6 bg-white rounded-xl shadow-md">
    <i class="fas fa-star text-4xl gradient-text mb-4"></i>
    <h3 class="text-xl font-bold mb-2">Your Card Title</h3>
    <p class="text-gray-600">Your card description here</p>
</div>
```

---

### 8. CTA (Call-to-Action) Section

**Location**: Lines 628-651

**Headline:**

```html
<!-- CURRENT CODE (Line 640) -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-white mb-6 tracking-tight">
    Ready to Transform Your Space?
</h2>

<!-- CHANGE TO -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-white mb-6 tracking-tight">
    Your CTA Headline
</h2>
```

**CTA Description:**

```html
<!-- CURRENT CODE (Lines 641-644) -->
<p class="text-lg md:text-xl text-gray-100 mb-8 max-w-2xl mx-auto leading-relaxed">
    Don't wait to give your property the radiant glow it deserves. 
    Contact us today for a personalized quote and let's bring your vision to life.
</p>

<!-- CHANGE TO -->
<p class="text-lg md:text-xl text-gray-100 mb-8 max-w-2xl mx-auto leading-relaxed">
    Your CTA description here. Make it compelling and action-oriented.
</p>
```

**CTA Buttons:**

```html
<!-- CURRENT CODE (Lines 645-654) -->
<a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank" rel="noopener noreferrer" 
   class="bg-white text-purple-600 px-8 py-4 rounded-lg font-bold text-lg hover:bg-gray-100 hover:shadow-xl hover:scale-105 transition-all duration-300">
    Get Your Free Quote
</a>
<a href="mailto:iainhmunro@gmail.com" 
   class="border-2 border-white text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-white hover:text-purple-600 hover:shadow-xl transition-all duration-300">
    Contact Us
</a>

<!-- CHANGE TO -->
<a href="https://your-website.com" target="_blank" rel="noopener noreferrer" 
   class="bg-white text-purple-600 px-8 py-4 rounded-lg font-bold text-lg hover:bg-gray-100 hover:shadow-xl hover:scale-105 transition-all duration-300">
    Your Button Text
</a>
<a href="mailto:your-email@example.com" 
   class="border-2 border-white text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-white hover:text-purple-600 hover:shadow-xl transition-all duration-300">
    Your Button Text
</a>
```

---

### 9. Footer

**Location**: Lines 659-730

**Company Info:**

```html
<!-- CURRENT CODE (Lines 668-671) -->
<span class="text-xl font-bold text-white">Sparkle & Shine</span>
<p class="text-gray-400 text-sm leading-relaxed">
    Transforming properties with professional painting and cleaning services since 2014.
</p>

<!-- CHANGE TO -->
<span class="text-xl font-bold text-white">Your Company Name</span>
<p class="text-gray-400 text-sm leading-relaxed">
    Your company tagline or brief description here.
</p>
```

**Footer Links:**

```html
<!-- CURRENT CODE (Lines 688-693) -->
<li><a href="#features" class="hover:text-purple-400 transition-colors duration-300">Features</a></li>
<li><a href="#benefits" class="hover:text-purple-400 transition-colors duration-300">Benefits</a></li>
<li><a href="#testimonials" class="hover:text-purple-400 transition-colors duration-300">Testimonials</a></li>
<li><a href="#faq" class="hover:text-purple-400 transition-colors duration-300">FAQ</a></li>
<li><a href="#about" class="hover:text-purple-400 transition-colors duration-300">About Us</a></li>

<!-- These links should match your navigation menu -->
<!-- Keep them consistent throughout the page -->
```

**Resource Links** (Lines 702-707):

```html
<!-- CURRENT CODE -->
<li><a href="privacy.html" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
<li><a href="blog.html" class="hover:text-purple-400 transition-colors duration-300">Blog</a></li>

<!-- These links point to pages you'll create -->
<!-- We'll cover this in the "Creating Privacy & Terms Pages" section -->
```

**Contact Info** (Lines 715-721):

```html
<!-- CURRENT CODE -->
<li class="flex items-center space-x-2">
    <i class="fas fa-envelope text-purple-400"></i>
    <a href="mailto:iainhmunro@gmail.com" class="hover:text-purple-400 transition-colors duration-300">
        iainhmunro@gmail.com
    </a>
</li>
<li class="flex items-center space-x-2">
    <i class="fas fa-globe text-purple-400"></i>
    <a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank" rel="noopener noreferrer" 
       class="hover:text-purple-400 transition-colors duration-300">
        freshfeelpaintingandcleaning.ca
    </a>
</li>

<!-- CHANGE TO YOUR CONTACT INFO -->
<li class="flex items-center space-x-2">
    <i class="fas fa-envelope text-purple-400"></i>
    <a href="mailto:your-email@example.com" class="hover:text-purple-400 transition-colors duration-300">
        your-email@example.com
    </a>
</li>
<li class="flex items-center space-x-2">
    <i class="fas fa-globe text-purple-400"></i>
    <a href="https://your-website.com" target="_blank" rel="noopener noreferrer" 
       class="hover:text-purple-400 transition-colors duration-300">
        your-website.com
    </a>
</li>
```

**Copyright** (Line 733):

```html
<!-- CURRENT CODE -->
<p>&copy; 2025 Sparkle & Shine. All rights reserved. | Transforming properties with excellence and care.</p>

<!-- CHANGE TO -->
<p>&copy; 2025 Your Company Name. All rights reserved. | Your tagline here.</p>
```

---

## Understanding & Modifying Tailwind CSS Classes

Tailwind CSS is a utility-first CSS framework. Instead of writing custom CSS, you use pre-built classes directly in your HTML. This section explains the most important classes in your landing page.

### What Are Tailwind Classes?

Tailwind classes are small, single-purpose classes that you combine to style elements. For example:

```html
<!-- Instead of writing custom CSS, you use multiple classes -->
<button class="bg-purple-600 text-white px-6 py-2 rounded-lg font-bold hover:shadow-lg transition-all duration-300">
    Click Me
</button>
```

Let's break this down:
- `bg-purple-600` = Purple background color
- `text-white` = White text color
- `px-6` = Horizontal padding (left and right)
- `py-2` = Vertical padding (top and bottom)
- `rounded-lg` = Rounded corners
- `font-bold` = Bold text
- `hover:shadow-lg` = Large shadow on hover
- `transition-all` = Smooth transition effect
- `duration-300` = Animation duration (300 milliseconds)

### Common Tailwind Classes Used in This Landing Page

#### Colors

```html
<!-- Background Colors -->
<div class="bg-white">...</div>           <!-- White background -->
<div class="bg-gray-50">...</div>         <!-- Light gray background -->
<div class="bg-gray-900">...</div>        <!-- Dark gray/black background -->
<div class="bg-purple-600">...</div>      <!-- Purple background -->
<div class="bg-pink-600">...</div>        <!-- Pink background -->

<!-- Text Colors -->
<p class="text-white">...</p>             <!-- White text -->
<p class="text-gray-600">...</p>          <!-- Medium gray text -->
<p class="text-gray-900">...</p>          <!-- Dark text -->
<p class="text-purple-600">...</p>        <!-- Purple text -->

<!-- Changing Colors: The pattern is color-number (50, 100, 200...900) -->
<!-- Lower numbers = lighter, Higher numbers = darker -->
<div class="bg-purple-100">...</div>      <!-- Very light purple -->
<div class="bg-purple-600">...</div>      <!-- Medium purple -->
<div class="bg-purple-900">...</div>      <!-- Very dark purple -->
```

#### Spacing (Padding & Margins)

```html
<!-- Padding (space inside an element) -->
<div class="p-4">...</div>                <!-- Padding on all sides -->
<div class="px-6">...</div>               <!-- Horizontal padding (left & right) -->
<div class="py-4">...</div>               <!-- Vertical padding (top & bottom) -->
<div class="pt-4">...</div>               <!-- Padding top only -->
<div class="pb-4">...</div>               <!-- Padding bottom only -->
<div class="pl-4">...</div>               <!-- Padding left only -->
<div class="pr-4">...</div>               <!-- Padding right only -->

<!-- Margins (space outside an element) -->
<div class="m-4">...</div>                <!-- Margin on all sides -->
<div class="mx-auto">...</div>            <!-- Center horizontally -->
<div class="my-6">...</div>               <!-- Vertical margin -->
<div class="mb-4">...</div>               <!-- Margin bottom only -->
<div class="mt-8">...</div>               <!-- Margin top only -->

<!-- Number meanings: 1=4px, 2=8px, 3=12px, 4=16px, 6=24px, 8=32px, etc. -->
```

#### Typography

```html
<!-- Font Size -->
<h1 class="text-4xl">...</h1>             <!-- Extra large (36px) -->
<h2 class="text-3xl">...</h2>             <!-- Very large (30px) -->
<h3 class="text-2xl">...</h3>             <!-- Large (24px) -->
<p class="text-lg">...</p>                <!-- Large (18px) -->
<p class="text-base">...</p>              <!-- Normal (16px) -->
<p class="text-sm">...</p>                <!-- Small (14px) -->

<!-- Font Weight -->
<p class="font-light">...</p>             <!-- Thin text -->
<p class="font-normal">...</p>            <!-- Regular text -->
<p class="font-semibold">...</p>          <!-- Semi-bold text -->
<p class="font-bold">...</p>              <!-- Bold text -->
<p class="font-black">...</p>             <!-- Extra bold text -->

<!-- Text Alignment -->
<p class="text-left">...</p>              <!-- Align left -->
<p class="text-center">...</p>            <!-- Center text -->
<p class="text-right">...</p>             <!-- Align right -->

<!-- Line Height -->
<p class="leading-relaxed">...</p>        <!-- Loose spacing between lines -->
<p class="leading-tight">...</p>          <!-- Tight spacing between lines -->
```

#### Borders & Shadows

```html
<!-- Borders -->
<div class="border">...</div>             <!-- 1px border on all sides -->
<div class="border-2">...</div>           <!-- 2px border -->
<div class="border-gray-200">...</div>    <!-- Border color -->
<div class="rounded">...</div>            <!-- Slightly rounded corners -->
<div class="rounded-lg">...</div>         <!-- Large rounded corners -->
<div class="rounded-xl">...</div>         <!-- Extra large rounded corners -->
<div class="rounded-full">...</div>       <!-- Circular (for avatars, etc.) -->

<!-- Shadows -->
<div class="shadow">...</div>             <!-- Subtle shadow -->
<div class="shadow-md">...</div>          <!-- Medium shadow -->
<div class="shadow-lg">...</div>          <!-- Large shadow -->
<div class="shadow-xl">...</div>          <!-- Extra large shadow -->
```

#### Responsive Design Classes

Tailwind uses prefixes for responsive design:

```html
<!-- Mobile first: No prefix = all screen sizes -->
<div class="text-2xl">...</div>           <!-- All screens: 24px text -->

<!-- sm: = screens 640px and up -->
<div class="sm:text-3xl">...</div>        <!-- Tablets and up: 30px text -->

<!-- md: = screens 768px and up -->
<div class="md:text-4xl">...</div>        <!-- Larger tablets and up: 36px text -->

<!-- lg: = screens 1024px and up -->
<div class="lg:text-5xl">...</div>        <!-- Desktops and up: 48px text -->

<!-- Example: Responsive button -->
<button class="px-4 md:px-6 lg:px-8 py-2 md:py-3 lg:py-4">
    <!-- Mobile: smaller padding, Tablet: medium padding, Desktop: larger padding -->
</button>
```

#### Display & Layout

```html
<!-- Display -->
<div class="flex">...</div>               <!-- Flexbox layout -->
<div class="grid">...</div>               <!-- Grid layout -->
<div class="hidden">...</div>             <!-- Hidden (display: none) -->
<div class="block">...</div>              <!-- Block display -->

<!-- Flexbox Alignment -->
<div class="flex items-center">...</div>  <!-- Vertically center items -->
<div class="flex justify-between">...</div><!-- Space items apart -->
<div class="flex justify-center">...</div><!-- Center items horizontally -->
<div class="flex space-x-4">...</div>     <!-- Space between flex items -->

<!-- Grid -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
    <!-- Mobile: 1 column, Tablet: 2 columns, Desktop: 3 columns -->
</div>

<!-- Gap (space between grid/flex items) -->
<div class="gap-4">...</div>              <!-- 16px gap -->
<div class="gap-6">...</div>              <!-- 24px gap -->
<div class="gap-8">...</div>              <!-- 32px gap -->
```

### Practical Examples: Modifying Classes

#### Example 1: Change Button Color

```html
<!-- CURRENT: Purple button -->
<button class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-8 py-4 rounded-lg font-bold">
    Click Me
</button>

<!-- CHANGE TO: Blue button -->
<button class="bg-gradient-to-r from-blue-600 to-cyan-600 text-white px-8 py-4 rounded-lg font-bold">
    Click Me
</button>

<!-- CHANGE TO: Green button -->
<button class="bg-gradient-to-r from-green-600 to-emerald-600 text-white px-8 py-4 rounded-lg font-bold">
    Click Me
</button>

<!-- CHANGE TO: Solid color (no gradient) -->
<button class="bg-purple-600 text-white px-8 py-4 rounded-lg font-bold">
    Click Me
</button>
```

#### Example 2: Change Spacing

```html
<!-- CURRENT: Card with padding and margin -->
<div class="bg-white rounded-xl p-6 shadow-md mb-4">
    Content here
</div>

<!-- INCREASE padding and margin -->
<div class="bg-white rounded-xl p-8 shadow-md mb-8">
    Content here
</div>

<!-- DECREASE padding and margin -->
<div class="bg-white rounded-xl p-4 shadow-md mb-2">
    Content here
</div>
```

#### Example 3: Change Grid Columns

```html
<!-- CURRENT: 3 columns on desktop -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
</div>

<!-- CHANGE TO: 4 columns on desktop -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
    <div>Item 4</div>
</div>

<!-- CHANGE TO: 2 columns on desktop -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-8">
    <div>Item 1</div>
    <div>Item 2</div>
</div>
```

#### Example 4: Change Text Size

```html
<!-- CURRENT: Responsive heading -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold">
    My Heading
</h2>

<!-- MAKE LARGER -->
<h2 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    My Heading
</h2>

<!-- MAKE SMALLER -->
<h2 class="text-2xl md:text-3xl lg:text-4xl font-bold">
    My Heading
</h2>
```

### Gradient Classes in This Landing Page

Your landing page uses gradient backgrounds and text. Here's how to modify them:

```html
<!-- CURRENT: Purple to Pink gradient -->
<div class="bg-gradient-to-r from-purple-600 to-pink-600">...</div>

<!-- CHANGE TO: Blue to Cyan gradient -->
<div class="bg-gradient-to-r from-blue-600 to-cyan-600">...</div>

<!-- CHANGE TO: Green to Emerald gradient -->
<div class="bg-gradient-to-r from-green-600 to-emerald-600">...</div>

<!-- Gradient directions -->
<div class="bg-gradient-to-r">...</div>  <!-- Left to right -->
<div class="bg-gradient-to-b">...</div>  <!-- Top to bottom -->
<div class="bg-gradient-to-br">...</div> <!-- Top-left to bottom-right -->
<div class="bg-gradient-to-l">...</div>  <!-- Right to left -->
<div class="bg-gradient-to-t">...</div>  <!-- Bottom to top -->
```

### Hover Effects

Your landing page uses hover effects to make it interactive:

```html
<!-- CURRENT: Hover effects -->
<div class="hover:shadow-lg hover:scale-105 transition-all duration-300">
    Hover over me
</div>

<!-- Understanding hover effects -->
<div class="hover:shadow-lg">...</div>         <!-- Add shadow on hover -->
<div class="hover:scale-105">...</div>         <!-- Grow 5% on hover -->
<div class="hover:bg-purple-50">...</div>      <!-- Change background on hover -->
<div class="hover:text-purple-600">...</div>   <!-- Change text color on hover -->
<div class="hover:border-purple-300">...</div> <!-- Change border on hover -->

<!-- Transition (makes hover smooth instead of instant) -->
<div class="transition-all duration-300">...</div>
<!-- transition-all = animate all property changes -->
<!-- duration-300 = animation takes 300 milliseconds -->
```

---

## Fixing & Updating Links

This section shows you how to find and update all links on your landing page.

### Understanding Links

A link in HTML looks like this:

```html
<a href="https://example.com" target="_blank" rel="noopener noreferrer">
    Link Text
</a>
```

Breaking it down:
- `<a>` = Link tag
- `href="..."` = Where the link goes
- `target="_blank"` = Opens in new tab/window
- `rel="noopener noreferrer"` = Security setting for external links
- `Link Text` = What the user sees and clicks
- `</a>` = Closes the link

### Types of Links in Your Landing Page

#### 1. **Internal Navigation Links** (Jump within the page)

These use `#` to link to sections:

```html
<!-- CURRENT CODE (Header Navigation - Lines 53-60) -->
<a href="#features" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">
    Features
</a>
<a href="#benefits" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">
    Benefits
</a>
<a href="#testimonials" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">
    Testimonials
</a>
<a href="#faq" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">
    FAQ
</a>
<a href="#about" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">
    About
</a>
```

**How these work:**
- `#features` links to the section with `id="features"` (Line 157)
- `#benefits` links to the section with `id="benefits"` (Line 248)
- `#testimonials` links to the section with `id="testimonials"` (Line 357)
- `#faq` links to the section with `id="faq"` (Line 448)
- `#about` links to the section with `id="about"` (Line 568)

**To add a new internal link:**

```html
<!-- 1. First, add an id to the section you want to link to -->
<section id="my-new-section">
    Content here
</section>

<!-- 2. Then add a link to it -->
<a href="#my-new-section">Go to My Section</a>
```

**Important**: The `#` name in the link must EXACTLY match the `id` in the section:
- ✅ Correct: `<a href="#services">` links to `<section id="services">`
- ❌ Wrong: `<a href="#services">` links to `<section id="service">` (won't work!)

#### 2. **External Links** (Go to other websites)

These use full URLs starting with `http://` or `https://`:

```html
<!-- CURRENT CODE (Line 64) -->
<a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank" rel="noopener noreferrer" 
   class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-6 py-2 rounded-lg font-semibold hover:shadow-lg hover:scale-105 transition-all duration-300">
    Get Started
</a>

<!-- TO CHANGE: Replace the href -->
<a href="https://your-website.com" target="_blank" rel="noopener noreferrer" 
   class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-6 py-2 rounded-lg font-semibold hover:shadow-lg hover:scale-105 transition-all duration-300">
    Get Started
</a>
```

**Key parts of external links:**
- `target="_blank"` = Opens in new tab (keep this!)
- `rel="noopener noreferrer"` = Security setting (keep this!)
- `href="https://..."` = Must start with `https://` or `http://`

#### 3. **Email Links**

These use `mailto:` instead of `http://`:

```html
<!-- CURRENT CODE (Line 649) -->
<a href="mailto:iainhmunro@gmail.com" 
   class="border-2 border-white text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-white hover:text-purple-600 hover:shadow-xl transition-all duration-300">
    Contact Us
</a>

<!-- TO CHANGE -->
<a href="mailto:your-email@example.com" 
   class="border-2 border-white text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-white hover:text-purple-600 hover:shadow-xl transition-all duration-300">
    Contact Us
</a>
```

**Format for email links:**
- `mailto:your-email@example.com` = Sends email to this address
- Don't use `target="_blank"` for email links
- Don't use `rel="noopener noreferrer"` for email links

### All Links in Your Landing Page

Here's a complete list of every link that needs updating:

#### Header Navigation (Lines 53-60, 76-82)

```html
<!-- Desktop Menu -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#testimonials">Testimonials</a>
<a href="#faq">FAQ</a>
<a href="#about">About</a>

<!-- Mobile Menu (same links repeated) -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#testimonials">Testimonials</a>
<a href="#faq">FAQ</a>
<a href="#about">About</a>
```

**Status**: These are internal links and should NOT be changed unless you rename sections.

#### Header CTA Buttons (Line 64, Line 85)

```html
<!-- Desktop Button -->
<a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank" rel="noopener noreferrer">
    Get Started
</a>

<!-- Mobile Button -->
<a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank" rel="noopener noreferrer">
    Get Started
</a>
```

**Action**: Change to your website URL

#### Hero Section Buttons (Lines 99-112)

```html
<!-- Primary CTA Button -->
<a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank" rel="noopener noreferrer">
    Transform Your Space Today
</a>

<!-- Secondary Button (Internal Link) -->
<a href="#features">
    Learn More
</a>
```

**Action**: 
- Change the primary button to your website
- Keep the secondary button as-is (it's an internal link)

#### CTA Section Buttons (Lines 645-654)

```html
<!-- Quote Button -->
<a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank" rel="noopener noreferrer">
    Get Your Free Quote
</a>

<!-- Contact Button -->
<a href="mailto:iainhmunro@gmail.com">
    Contact Us
</a>
```

**Action**: 
- Change the quote button to your website
- Change the email address to your email

#### Footer Links - Quick Links Section (Lines 688-693)

```html
<li><a href="#features">Features</a></li>
<li><a href="#benefits">Benefits</a></li>
<li><a href="#testimonials">Testimonials</a></li>
<li><a href="#faq">FAQ</a></li>
<li><a href="#about">About Us</a></li>
```

**Status**: These are internal links. Keep them as-is.

#### Footer Links - Resources Section (Lines 702-707)

```html
<li><a href="privacy.html">Privacy Policy</a></li>
<li><a href="terms.html">Terms of Service</a></li>
<li><a href="blog.html">Blog</a></li>
<li><a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank" rel="noopener noreferrer">
    Visit Website
</a></li>
```

**Action**: 
- `privacy.html` and `terms.html` are for pages you'll create (see next section)
- `blog.html` is optional - remove if you don't have a blog
- Update the website link to your website

#### Footer Contact Links (Lines 715-721)

```html
<!-- Email Link -->
<a href="mailto:iainhmunro@gmail.com">
    iainhmunro@gmail.com
</a>

<!-- Website Link -->
<a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank" rel="noopener noreferrer">
    freshfeelpaintingandcleaning.ca
</a>
```

**Action**: Update to your email and website

#### Footer Social Links (Lines 725-740)

```html
<a href="#" aria-label="Facebook">
    <i class="fab fa-facebook-f text-white"></i>
</a>
<a href="#" aria-label="Instagram">
    <i class="fab fa-instagram text-white"></i>
</a>
<a href="#" aria-label="Twitter">
    <i class="fab fa-twitter text-white"></i>
</a>
<a href="#" aria-label="LinkedIn">
    <i class="fab fa-linkedin-in text-white"></i>
</a>
```

**Action**: Replace `#` with your social media profiles:

```html
<!-- EXAMPLE: Update to your Facebook page -->
<a href="https://www.facebook.com/your-page-name" aria-label="Facebook" target="_blank" rel="noopener noreferrer">
    <i class="fab fa-facebook-f text-white"></i>
</a>

<!-- EXAMPLE: Update to your Instagram profile -->
<a href="https://www.instagram.com/your-username" aria-label="Instagram" target="_blank" rel="noopener noreferrer">
    <i class="fab fa-instagram text-white"></i>
</a>
```

### Step-by-Step: Updating All Links

**Step 1: Update Hero & CTA Website Links**

```html
<!-- Find these lines (approximately 64, 99, 645) -->
<a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank" rel="noopener noreferrer">

<!-- Replace the URL -->
<a href="https://your-actual-website.com" target="_blank" rel="noopener noreferrer">
```

**Step 2: Update Email Links**

```html
<!-- Find these lines (approximately 649, 721) -->
<a href="mailto:iainhmunro@gmail.com">

<!-- Replace with your email -->
<a href="mailto:your-email@example.com">
```

**Step 3: Update Footer Website Link**

```html
<!-- Find this line (approximately 707, 721) -->
<a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank" rel="noopener noreferrer">
    freshfeelpaintingandcleaning.ca
</a>

<!-- Replace with your website -->
<a href="https://your-website.com" target="_blank" rel="noopener noreferrer">
    your-website.com
</a>
```

**Step 4: Update Social Media Links (Optional)**

```html
<!-- Find these lines (approximately 725-740) -->
<a href="#" aria-label="Facebook">

<!-- Replace # with your social media URLs -->
<a href="https://www.facebook.com/your-page" aria-label="Facebook" target="_blank" rel="noopener noreferrer">

<!-- Add target="_blank" and rel="noopener noreferrer" for external links -->
```

### Testing Your Links

After updating links:

1. **Open your page in a browser** (right-click the file → Open with browser)
2. **Test each link** by clicking it
3. **Check that:**
   - Internal links (with #) jump to the correct section
   - External links open in a new tab
   - Email links open your email client
4. **Fix any broken links** - make sure the URLs are correct

---

## Creating Privacy & Terms Pages

Your footer currently links to `privacy.html` and `terms.html` pages that don't exist yet. This section shows you how to create them.

### Why You Need These Pages

- **Legal requirement** for most websites
- **Trust & credibility** with visitors
- **Protection** for your business
- **SEO benefit** for search engines

### Step 1: Create the Privacy Policy Page

**Create a new file:**

1. Open your code editor
2. Click "File" → "New File"
3. Copy the code below
4. Save as `privacy.html` in the same folder as `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for Sparkle & Shine">
    <title>Privacy Policy | Sparkle & Shine</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&family=Playfair+Display:wght@700;800;900&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
        }
        
        h1, h2, h3 {
            font-family: 'Playfair Display', serif;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-sparkles text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold gradient-text">Sparkle & Shine</a>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">
                Back to Home
            </a>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold mb-8 tracking-tight">Privacy Policy</h1>
        
        <div class="prose prose-lg max-w-none space-y-6 text-gray-700 leading-relaxed">
            <p>
                <strong>Last Updated: January 2025</strong>
            </p>

            <section>
                <h2 class="text-2xl font-bold mt-8 mb-4 text-gray-900">1. Introduction</h2>
                <p>
                    Sparkle & Shine ("we," "us," "our," or "Company") operates the Sparkle & Shine website. 
                    This page informs you of our policies regarding the collection, use, and disclosure of 
                    personal data when you use our Service and the choices you have associated with that data.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold mt-8 mb-4 text-gray-900">2. Information Collection and Use</h2>
                <p>
                    We collect several different types of information for various purposes to provide and 
                    improve our Service to you.
                </p>
                
                <h3 class="text-xl font-bold mt-6 mb-3 text-gray-900">Types of Data Collected:</h3>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li><strong>Personal Data:</strong> While using our Service, we may ask you to provide 
                    us with certain personally identifiable information that can be used to contact or 
                    identify you ("Personal Data"). This may include, but is not limited to:
                        <ul class="list-disc list-inside space-y-1 ml-4 mt-2">
                            <li>Email address</li>
                            <li>First name and last name</li>
                            <li>Phone number</li>
                            <li>Address, State, Province, ZIP/Postal code, City</li>
                            <li>Cookies and Usage Data</li>
                        </ul>
                    </li>
                    <li><strong>Usage Data:</strong> We may also collect information on how the Service is 
                    accessed and used ("Usage Data"). This may include information such as your computer's 
                    Internet Protocol address (e.g. IP address), browser type, browser version, the pages 
                    you visit, the time and date of your visit, the time spent on those pages, and other 
                    diagnostic data.</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold mt-8 mb-4 text-gray-900">3. Use of Data</h2>
                <p>Sparkle & Shine uses the collected data for various purposes:</p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>To provide and maintain our Service</li>
                    <li>To notify you about changes to our Service</li>
                    <li>To allow you to participate in interactive features of our Service when you choose to do so</li>
                    <li>To provide customer support</li>
                    <li>To gather analysis or valuable information so that we can improve our Service</li>
                    <li>To monitor the usage of our Service</li>
                    <li>To detect, prevent and address technical issues</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold mt-8 mb-4 text-gray-900">4. Security of Data</h2>
                <p>
                    The security of your data is important to us but remember that no method of transmission 
                    over the Internet or method of electronic storage is 100% secure. While we strive to use 
                    commercially acceptable means to protect your Personal Data, we cannot guarantee its 
                    absolute security.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold mt-8 mb-4 text-gray-900">5. Contact Us</h2>
                <p>
                    If you have any questions about this Privacy Policy, please contact us:
                </p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>By email: <a href="mailto:iainhmunro@gmail.com" class="text-purple-600 hover:text-purple-700">iainhmunro@gmail.com</a></li>
                    <li>By visiting our website: <a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank" rel="noopener noreferrer" class="text-purple-600 hover:text-purple-700">freshfeelpaintingandcleaning.ca</a></li>
                </ul>
            </section>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12 mt-24 border-t border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p>&copy; 2025 Sparkle & Shine. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
```

### Step 2: Create the Terms of Service Page

**Create a new file:**

1. Open your code editor
2. Click "File" → "New File"
3. Copy the code below
4. Save as `terms.html` in the same folder as `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for Sparkle & Shine">
    <title>Terms of Service | Sparkle & Shine</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&family=Playfair+Display:wght@700;800;900&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
        }
        
        h1, h2, h3 {
            font-family: 'Playfair Display', serif;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-sparkles text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold gradient-text">Sparkle & Shine</a>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">
                Back to Home
            </a>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold mb-8 tracking-tight">Terms of Service</h1>
        
        <div class="prose prose-lg max-w-none space-y-6 text-gray-700 leading-relaxed">
            <p>
                <strong>Last Updated: January 2025</strong>
            </p>

            <section>
                <h2 class="text-2xl font-bold mt-8 mb-4 text-gray-900">1. Agreement to Terms</h2>
                <p>
                    By accessing and using the Sparkle & Shine website and services, you accept and agree 
                    to be bound by and comply with these terms and conditions. If you do not agree to abide 
                    by the above, please do not use this service.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold mt-8 mb-4 text-gray-900">2. Use License</h2>
                <p>
                    Permission is granted to temporarily download one copy of the materials (information or 
                    software) on Sparkle & Shine's website for personal, non-commercial transitory viewing only. 
                    This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>Modifying or copying the materials</li>
                    <li>Using the materials for any commercial purpose or for any public display</li>
                    <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                    <li>Removing any copyright or other proprietary notations from the materials</li>
                    <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold mt-8 mb-4 text-gray-900">3. Disclaimer</h2>
                <p>
                    The materials on Sparkle & Shine's website are provided on an 'as is' basis. Sparkle & Shine 
                    makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties 
                    including, without limitation, implied warranties or conditions of merchantability, fitness for 
                    a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold mt-8 mb-4 text-gray-900">4. Limitations</h2>
                <p>
                    In no event shall Sparkle & Shine or its suppliers be liable for any damages (including, without 
                    limitation, damages for loss of data or profit, or due to business interruption) arising out of 
                    the use or inability to use the materials on Sparkle & Shine's website, even if Sparkle & Shine 
                    or an authorized representative has been notified orally or in writing of the possibility of such damage.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold mt-8 mb-4 text-gray-900">5. Accuracy of Materials</h2>
                <p>
                    The materials appearing on Sparkle & Shine's website could include technical, typographical, or 
                    photographic errors. Sparkle & Shine does not warrant that any of the materials on its website are 
                    accurate, complete, or current. Sparkle & Shine may make changes to the materials contained on its 
                    website at any time without notice.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold mt-8 mb-4 text-gray-900">6. Links</h2>
                <p>
                    Sparkle & Shine has not reviewed all of the sites linked to its website and is not responsible for 
                    the contents of any such linked site. The inclusion of any link does not imply endorsement by 
                    Sparkle & Shine of the site. Use of any such linked website is at the user's own risk.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold mt-8 mb-4 text-gray-900">7. Modifications</h2>
                <p>
                    Sparkle & Shine may revise these terms of service for its website at any time without notice. 
                    By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold mt-8 mb-4 text-gray-900">8. Governing Law</h2>
                <p>
                    These terms and conditions are governed by and construed in accordance with the laws of Canada, 
                    and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold mt-8 mb-4 text-gray-900">9. Contact Us</h2>
                <p>
                    If you have any questions about these Terms of Service, please contact us:
                </p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>By email: <a href="mailto:iainhmunro@gmail.com" class="text-purple-600 hover:text-purple-700">iainhmunro@gmail.com</a></li>
                    <li>By visiting our website: <a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank" rel="noopener noreferrer" class="text-purple-600 hover:text-purple-700">freshfeelpaintingandcleaning.ca</a></li>
                </ul>
            </section>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12 mt-24 border-t border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p>&copy; 2025 Sparkle & Shine. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
```

### Step 3: Customize the Pages

**Update company information in both files:**

```html
<!-- In privacy.html and terms.html, find and update: -->

<!-- Email address -->
<a href="mailto:iainhmunro@gmail.com">iainhmunro@gmail.com</a>
<!-- Change to -->
<a href="mailto:your-email@example.com">your-email@example.com</a>

<!-- Website link -->
<a href="https://www.freshfeelpaintingandcleaning.ca/">freshfeelpaintingandcleaning.ca</a>
<!-- Change to -->
<a href="https://your-website.com">your-website.com</a>

<!-- Company name -->
Sparkle & Shine
<!-- Change to -->
Your Company Name

<!-- Last Updated date -->
<strong>Last Updated: January 2025</strong>
<!-- Change to -->
<strong>Last Updated: [Current Date]</strong>
```

### Step 4: Test the Links

1. Open `index.html` in your browser
2. Scroll to the footer
3. Click on "Privacy Policy" - it should open `privacy.html`
4. Click on "Terms of Service" - it should open `terms.html`
5. Click "Back to Home" - it should return to `index.html`

### Step 5: Customize Privacy Policy Content

The template provided is generic. Customize it for your business:

**Things to update:**
- Add your company's specific data collection practices
- Explain what data you collect from quote requests
- Describe how you use customer information
- Add your data retention policies
- Include your cookie policy
- Add any third-party services you use (e.g., email marketing)

**Example customization:**

```html
<!-- ORIGINAL GENERIC TEXT -->
<p>
    While using our Service, we may ask you to provide us with certain personally 
    identifiable information...
</p>

<!-- CUSTOMIZE TO YOUR BUSINESS -->
<p>
    When you request a quote for our painting and cleaning services, we collect 
    your name, email address, phone number, and property address. This information 
    helps us provide accurate estimates and schedule your service.
</p>
```

### Step 6: Customize Terms of Service Content

Update the template to reflect your actual terms:

**Things to update:**
- Service cancellation policies
- Payment terms
- Warranty information
- Liability limitations specific to your services
- Dispute resolution process

**Example customization:**

```html
<!-- ORIGINAL -->
<p>
    The materials on Sparkle & Shine's website are provided on an 'as is' basis...
</p>

<!-- CUSTOMIZE -->
<p>
    Our painting and cleaning services are provided on an 'as is' basis. We warrant 
    that all work will be performed professionally and in accordance with industry standards. 
    All painting projects include a 2-year warranty covering paint quality and workmanship.
</p>
```

---

## Responsive Design Considerations

Your landing page is built to work on all devices. Here's how to maintain responsive design when making changes.

### Understanding Responsive Breakpoints

Your page uses these breakpoints:

```html
<!-- sm: (small) = 640px and up (tablets) -->
<!-- md: (medium) = 768px and up (larger tablets) -->
<!-- lg: (large) = 1024px and up (desktops) -->

<!-- Example: Text size changes based on screen size -->
<h1 class="text-2xl md:text-4xl lg:text-6xl">
    <!-- Mobile: 24px, Tablet: 36px, Desktop: 48px -->
</h1>
```

### Testing Responsive Design

**In Your Browser:**

1. Open your page in a browser
2. Press `F12` to open Developer Tools
3. Click the device icon (looks like a phone/tablet)
4. Choose different devices to test:
   - iPhone SE (mobile)
   - iPad (tablet)
   - Desktop

**What to check:**
- Text is readable on all sizes
- Images scale properly
- Buttons are easy to click on mobile
- Navigation menu works on mobile
- No horizontal scrolling on mobile

### Common Responsive Issues & Fixes

**Issue: Text is too small on mobile**

```html
<!-- PROBLEM: Only large text -->
<h2 class="text-4xl font-bold">My Heading</h2>

<!-- SOLUTION: Add responsive sizes -->
<h2 class="text-2xl md:text-3xl lg:text-4xl font-bold">My Heading</h2>
```

**Issue: Too many columns on mobile**

```html
<!-- PROBLEM: Always 3 columns -->
<div class="grid grid-cols-3 gap-4">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
</div>

<!-- SOLUTION: Responsive columns -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
</div>
<!-- Mobile: 1 column, Tablet: 2 columns, Desktop: 3 columns -->
```

**Issue: Content too wide on mobile**

```html
<!-- PROBLEM: Padding is same on all sizes -->
<div class="px-8 py-6">Content</div>

<!-- SOLUTION: Responsive padding -->
<div class="px-4 md:px-6 lg:px-8 py-4 md:py-6">Content</div>
<!-- Mobile: smaller padding, Desktop: larger padding -->
```

### When Adding New Content

Always use responsive classes:

```html
<!-- ❌ NOT RESPONSIVE -->
<div class="text-4xl px-8">Content</div>

<!-- ✅ RESPONSIVE -->
<div class="text-xl md:text-2xl lg:text-4xl px-4 md:px-6 lg:px-8">Content</div>
```

---

## Troubleshooting Common Issues

### Issue 1: Changes Not Showing Up

**Problem**: You made changes but the page looks the same.

**Solutions:**

1. **Hard refresh your browser:**
   - Windows: `Ctrl + Shift + R`
   - Mac: `Cmd + Shift + R`

2. **Clear browser cache:**
   - Chrome: Settings → Privacy → Clear browsing data
   - Firefox: History → Clear Recent History

3. **Close and reopen the file:**
   - Make sure you saved the file
   - Close the browser tab
   - Reopen the HTML file

### Issue 2: Styling Looks Broken

**Problem**: Buttons look wrong, colors are off, or layout is messed up.

**Solutions:**

1. **Check for typos in class names:**

```html
<!-- ❌ WRONG - Class doesn't exist -->
<div class="bg-purpl-600">Content</div>

<!-- ✅ CORRECT -->
<div class="bg-purple-600">Content</div>
```

2. **Make sure Tailwind CSS is loaded:**

```html
<!-- This line must be in your <head> -->
<script src="https://cdn.tailwindcss.com"></script>
```

3. **Check for missing closing tags:**

```html
<!-- ❌ WRONG - Missing </div> -->
<div class="bg-white">
    <p>Content</p>
</div>

<!-- ✅ CORRECT -->
<div class="bg-white">
    <p>Content</p>
</div>
```

### Issue 3: Links Not Working

**Problem**: Clicking a link does nothing or goes to the wrong place.

**Solutions:**

1. **Check the href matches the id:**

```html
<!-- ❌ WRONG - href and id don't match -->
<a href="#feature">Go to Features</a>
<section id="features">...</section>

<!-- ✅ CORRECT -->
<a href="#features">Go to Features</a>
<section id="features">...</section>
```

2. **Check external links have https://**

```html
<!-- ❌ WRONG -->
<a href="www.example.com">Link</a>

<!-- ✅ CORRECT -->
<a href="https://www.example.com">Link</a>
```

3. **Check email links use mailto:**

```html
<!-- ❌ WRONG -->
<a href="email@example.com">Email</a>

<!-- ✅ CORRECT -->
<a href="mailto:email@example.com">Email</a>
```

### Issue 4: Mobile Menu Not Working

**Problem**: The hamburger menu on mobile doesn't open/close.

**Solutions:**

1. **Check JavaScript is enabled** in your browser
2. **Make sure you didn't delete the JavaScript code** (Lines 741-790)
3. **Check the mobile menu button class is correct:**

```html
<!-- This must exist in your header -->
<button class="md:hidden mobile-menu-button">
    <i class="fas fa-bars"></i>
</button>

<!-- And this mobile menu div must exist -->
<div class="mobile-menu hidden">
    <!-- Menu items -->
</div>
```

### Issue 5: Images Not Showing

**Problem**: You see broken image icons instead of images.

**Solutions:**

1. **Check the image file exists** in your project folder
2. **Use correct relative path:**

```html
<!-- ❌ WRONG - Looking in wrong folder -->
<img src="/images/photo.jpg">

<!-- ✅ CORRECT - Same folder -->
<img src="photo.jpg">

<!-- ✅ CORRECT - In subfolder -->
<img src="images/photo.jpg">
```

3. **Check file extension is correct:**

```html
<!-- Common extensions: .jpg, .png, .gif, .webp -->
<img src="photo.jpg">
```

### Issue 6: Gradient Colors Not Showing

**Problem**: Gradient effects aren't displaying.

**Solutions:**

1. **Make sure you're using gradient classes:**

```html
<!-- ❌ WRONG - Not a gradient -->
<div class="bg-purple-600">Content</div>

<!-- ✅ CORRECT - Gradient -->
<div class="bg-gradient-to-r from-purple-600 to-pink-600">Content</div>
```

2. **Check color names are spelled correctly:**

```html
<!-- ❌ WRONG -->
<div class="from-purpl-600">Content</div>

<!-- ✅ CORRECT -->
<div class="from-purple-600">Content</div>
```

### Issue 7: Text Overflowing or Cut Off

**Problem**: Text extends beyond its container or gets cut off.

**Solutions:**

1. **Add word-break classes:**

```html
<!-- ❌ PROBLEM - Text overflows -->
<div class="w-32">
    This is a very long word that doesn't fit
</div>

<!-- ✅ SOLUTION - Allow text to break -->
<div class="w-32 break-words">
    This is a very long word that doesn't fit
</div>
```

2. **Use responsive widths:**

```html
<!-- ✅ BETTER - Wider on larger screens -->
<div class="w-full md:w-1/2 lg:w-1/3">Content</div>
```

### Issue 8: Form Not Sending

**Problem**: Contact form doesn't work.

**Note**: This landing page doesn't have a built-in form. The contact buttons link to external services or email. To add a working form:

1. Use a service like [Formspree](https://formspree.io/) or [Netlify Forms](https://www.netlify.com/products/forms/)
2. Or use PHP/backend code if you have server access

---

## Best Practices for Maintenance

### 1. Keep a Backup

**Always keep a backup of your original file:**

```
project-folder/
├── index.html              (Current version)
├── index-backup.html       (Backup copy)
└── index-v2.html           (Previous version)
```

**How to backup:**
- Right-click the file → Copy
- Right-click → Paste
- Rename to `index-backup.html`

### 2. Make One Change at a Time

**Don't make multiple changes before testing:**

```
✅ GOOD WORKFLOW:
1. Change one thing
2. Save the file
3. Test in browser
4. Repeat for next change

❌ BAD WORKFLOW:
1. Change 5 things
2. Save the file
3. Test - something is broken
4. Don't know which change caused it
```

### 3. Use Version Control (Optional but Recommended)

**If you know Git:**

```bash
git init
git add index.html privacy.html terms.html
git commit -m "Initial landing page"
git commit -m "Updated contact email"
```

**If you don't know Git:**
- Use [GitHub Desktop](https://desktop.github.com/) (easier than command line)
- Or just keep multiple backup files

### 4. Update Regularly

**Things to update periodically:**

- [ ] Check all links still work (quarterly)
- [ ] Update testimonials (as you get new ones)
- [ ] Update statistics (projects completed, ratings)
- [ ] Refresh FAQ with new questions
- [ ] Update copyright year (annually)
- [ ] Review and update privacy policy (annually)

### 5. Monitor for Broken Links

**Broken link checker tools:**
- [Broken Link Checker](https://www.brokenlinkchecker.com/)
- [Dr. Link Check](https://www.drlinkccheck.com/)

**How to use:**
1. Go to the website
2. Enter your website URL
3. Run the check
4. Fix any broken links

### 6. Test on Multiple Browsers

**Test your site on:**
- Chrome
- Firefox
- Safari
- Edge

**Why?** Different browsers sometimes render things differently.

### 7. Keep Security Updated

**Update these regularly:**

```html
<!-- Font Awesome icons (check for updates) -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<!-- Tailwind CSS (check for updates) -->
<script src="https://cdn.tailwindcss.com"></script>

<!-- Google Fonts (usually auto-updates) -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&family=Playfair+Display:wght@700;800;900&display=swap" rel="stylesheet">
```

### 8. Optimize Images

**Before adding images:**

1. Resize to appropriate dimensions (not larger than needed)
2. Compress the file size using:
   - [TinyPNG](https://tinypng.com/)
   - [Compressor.io](https://compressor.io/)
   - [ImageOptim](https://imageoptim.com/)

**Why?** Smaller images = faster page load = better user experience

### 9. Use Descriptive File Names

**Good file names:**
- `privacy.html`
- `terms.html`
- `contact-form.html`
- `logo.png`

**Bad file names:**
- `page1.html`
- `file.html`
- `image1.png`
- `new-file.html`

### 10. Document Your Changes

**Keep a changelog:**

```
# Changelog

## Version 2.1 (January 15, 2025)
- Updated hero section headline
- Added new testimonial from Sarah Patel
- Fixed broken links in footer
- Updated privacy policy

## Version 2.0 (January 1, 2025)
- Created privacy and terms pages
- Updated company information
- Added new features section

## Version 1.0 (December 1, 2024)
- Initial launch
```

---

## Summary Checklist

Use this checklist when maintaining your landing page:

### Content Updates
- [ ] Update company name/branding
- [ ] Update hero headline and description
- [ ] Update feature descriptions and icons
- [ ] Update benefit descriptions
- [ ] Update testimonials
- [ ] Update FAQ questions and answers
- [ ] Update about section
- [ ] Update statistics (projects, ratings, etc.)

### Links & Navigation
- [ ] Update all website URLs
- [ ] Update all email addresses
- [ ] Update social media links
- [ ] Test all internal navigation links
- [ ] Test all external links
- [ ] Verify privacy policy link works
- [ ] Verify terms page link works

### Visual Elements
- [ ] Check colors are consistent
- [ ] Verify all icons display correctly
- [ ] Test responsive design on mobile
- [ ] Test responsive design on tablet
- [ ] Test responsive design on desktop
- [ ] Check no text is cut off

### Legal & Security
- [ ] Customize privacy policy
- [ ] Customize terms of service
- [ ] Update copyright year
- [ ] Verify SSL certificate (if applicable)
- [ ] Check for broken links

### Performance
- [ ] Optimize images
- [ ] Test page load speed
- [ ] Verify fonts load correctly
- [ ] Test on different browsers

---

## Final Notes

### When to Hire a Professional

Consider hiring a web developer if you need to:
- Build a shopping cart or payment system
- Create a complex form with validation
- Set up email automation
- Implement a booking system
- Add a blog with CMS
- Optimize for SEO beyond basics
- Deploy to a custom domain

### Free Resources for Learning

- [MDN Web Docs](https://developer.mozilla.org/) - HTML/CSS reference
- [Tailwind CSS Documentation](https://tailwindcss.com/docs) - Tailwind classes
- [Font Awesome Icons](https://fontawesome.com/icons) - Find and use icons
- [W3Schools](https://www.w3schools.com/) - HTML/CSS/JavaScript tutorials
- [YouTube Tutorials](https://www.youtube.com/) - Search for specific topics

### Getting Help

If you get stuck:
1. **Check this guide** - Most issues are covered in Troubleshooting
2. **Search online** - Copy your error message into Google
3. **Check browser console** - Press F12, click "Console" to see errors
4. **Visit forums** - Stack Overflow, Reddit r/webdev
5. **Hire a developer** - If it's too complex

---

**You've got this! Your landing page is well-structured and easy to maintain. Make small changes, test frequently, and don't be afraid to experiment. Good luck with your Sparkle & Shine landing page!**
# The Shift Chiropractic Landing Page - Maintenance & Customization Guide

## Table of Contents
1. [Introduction](#introduction)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Common Customizations](#common-customizations)
8. [Troubleshooting Guide](#troubleshooting-guide)

---

## Introduction

This guide will help you maintain and customize The Shift Chiropractic landing page. Whether you're updating business information, changing colors, or adding new pages, you'll find step-by-step instructions tailored to this specific website.

**What You'll Need:**
- A text editor (Notepad++, Visual Studio Code, or similar)
- Basic understanding of HTML tags and structure
- No advanced coding experience required!

---

## Understanding the Page Structure

Before making changes, it's helpful to understand how this page is organized. Think of the HTML file as a blueprint with different sections:

```
Landing Page Structure:
├── Header (Navigation Menu)
├── Hero Section (Main Banner)
├── Features Section
├── Benefits Section
├── CTA Section (Call-to-Action)
├── Testimonials Section
├── About Us Section
├── FAQ Section
├── Final CTA Section
├── Footer
└── JavaScript (Interactive Features)
```

### Key Concept: HTML Tags

HTML uses tags (words in angle brackets) to organize content. For example:
- `<h1>` = Main heading
- `<p>` = Paragraph of text
- `<a>` = Link (clickable text)
- `<section>` = Large content area
- `<div>` = Container for grouping content

When you see `<h1>Oakland Car Accident Recovery...</h1>`, the text between the opening tag `<h1>` and closing tag `</h1>` is what displays on the page.

---

## Updating Text Content

### How to Find and Edit Text

**Step 1: Open the File**
1. Right-click on your `index.html` file
2. Select "Open with" and choose your text editor
3. You should see all the HTML code

**Step 2: Use Find & Replace**
This is the easiest way to update text:

1. Press `Ctrl+H` (Windows) or `Cmd+H` (Mac) to open Find & Replace
2. Type the old text in the "Find" field
3. Type the new text in the "Replace" field
4. Click "Replace All" to update everywhere at once

### Common Text Areas to Update

#### Header/Navigation Menu

**Location:** Look for this section near the top (around line 35):

```html
<span class="text-xl font-bold text-white hidden sm:inline">The Shift</span>
```

**To change the business name:**
- Find: `The Shift`
- Replace with: Your business name

**Navigation Links Text:**

```html
<a href="#features" class="text-gray-300 hover:text-blue-400 transition-smooth font-medium">Features</a>
```

The text between `>` and `</a>` is what displays. Change "Features" to any menu item name you want.

---

#### Hero Section (Main Banner)

**Location:** Search for this heading (around line 135):

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-6 text-white">
    Oakland Car Accident Recovery - No Payment Required - Compassionate Care
</h1>
```

**To change the main headline:**
1. Find the entire text between `<h1>` and `</h1>`
2. Delete it completely
3. Type your new headline
4. Keep the `<h1>` and `</h1>` tags

**Example:**
```html
<!-- BEFORE -->
<h1>Oakland Car Accident Recovery - No Payment Required - Compassionate Care</h1>

<!-- AFTER -->
<h1>Fast Auto Injury Treatment in Oakland - Zero Upfront Cost</h1>
```

**Subtitle under the heading:**

```html
<p class="text-xl md:text-2xl text-gray-300 mb-8 leading-relaxed font-light">
    Same-Day Auto Injury Care - Oakland Doctors Who Can Heal You
</p>
```

Change the text between `<p>` and `</p>` to your new subtitle.

---

#### Features Section

**Location:** Search for "Comprehensive Auto Injury Care Services" (around line 195):

Each feature has three parts:

```html
<h3 class="text-2xl font-bold mb-4 text-white">Immediate Treatment</h3>
<p class="text-gray-400 leading-relaxed mb-4">
    Same-day appointments available for accident victims...
</p>
<ul class="space-y-2 text-gray-300">
    <li class="flex items-center"><i class="fas fa-check text-blue-400 mr-3"></i>Emergency same-day availability</li>
    <li class="flex items-center"><i class="fas fa-check text-blue-400 mr-3"></i>Rapid diagnostic imaging</li>
</ul>
```

**To update a feature:**
1. Change the `<h3>` title
2. Change the `<p>` description
3. Update each `<li>` bullet point

---

#### Benefits Section

**Location:** Search for "Why Choose The Shift Chiropractic" (around line 270):

```html
<h3 class="text-2xl font-bold text-white mb-3">Doctor Gender Choice</h3>
<p class="text-gray-400 leading-relaxed">
    We respect your comfort and preferences...
</p>
```

Same process: update the heading and paragraph text.

---

#### Testimonials Section

**Location:** Search for "Real Stories from Our Patients" (around line 390):

Each testimonial has a name, job title, and quote:

```html
<h3 class="text-lg font-bold text-white">Marcus Johnson</h3>
<p class="text-sm text-gray-400">Software Engineer</p>
```

And the testimonial text:

```html
<p class="text-gray-300 leading-relaxed">
    "After my car accident, I was in severe pain..."
</p>
```

**To update a testimonial:**
1. Change the person's name in the `<h3>` tag
2. Change their job title in the `<p class="text-sm text-gray-400">` tag
3. Change the quote in the larger `<p>` tag

---

#### Footer

**Location:** Scroll to the very bottom (around line 775):

```html
<p class="text-gray-500 text-sm">
    &copy; 2025 The Shift Chiropractic. All rights reserved.
</p>
```

**To update the copyright year:**
- Find: `2025`
- Replace with: Current year (e.g., `2024`)

---

### Important: Preserving HTML Tags

⚠️ **Critical Rule:** Always keep the HTML tags when editing text!

**WRONG:**
```html
<!-- Don't delete the tags! -->
<h1></h1>  ← Empty heading
```

**RIGHT:**
```html
<!-- Keep tags, just change the text -->
<h1>Your new text here</h1>
```

---

## Modifying Tailwind CSS Classes

Tailwind CSS is a system that uses class names to style elements. This page uses Tailwind extensively. Understanding how to modify these classes will let you change colors, sizes, spacing, and more.

### Understanding Tailwind Class Names

Tailwind class names are descriptive and follow a pattern. Here are common ones used in this page:

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-white` | Makes text white | `<p class="text-white">` |
| `bg-gray-900` | Dark gray background | `<div class="bg-gray-900">` |
| `text-4xl` | Large text size | `<h1 class="text-4xl">` |
| `px-4` | Padding (space inside) left/right | `<div class="px-4">` |
| `py-24` | Padding (space inside) top/bottom | `<section class="py-24">` |
| `mb-6` | Margin (space outside) bottom | `<h2 class="mb-6">` |
| `rounded-lg` | Slightly rounded corners | `<div class="rounded-lg">` |
| `hover:bg-blue-600` | Changes on mouse hover | `<button class="hover:bg-blue-600">` |

### The Color System

This page uses a color scheme based on gray and blue. Here are the main colors:

**Gray Colors:**
- `gray-900` = Very dark gray (almost black)
- `gray-800` = Dark gray
- `gray-700` = Medium dark gray
- `gray-400` = Light gray
- `gray-300` = Lighter gray

**Blue Colors (Accent):**
- `blue-400` = Light blue (used for highlights)
- `blue-500` = Medium blue (used for buttons)
- `blue-600` = Darker blue (used on hover)

### Changing the Accent Color

The page uses blue as the accent color throughout. If you want to change it to a different color, you'll need to replace all blue references.

**Step 1: Identify all blue classes**

Common blue classes in this page:
- `bg-blue-500` (button background)
- `bg-blue-600` (button hover)
- `text-blue-400` (accent text)
- `border-blue-500` (accent border)
- `from-blue-400 to-blue-600` (gradient)

**Step 2: Choose your new color**

Tailwind colors include: red, orange, yellow, green, emerald, teal, cyan, blue, indigo, purple, pink, rose

**Step 3: Use Find & Replace**

For example, to change from blue to purple:

1. Press `Ctrl+H` to open Find & Replace
2. Find: `blue-500`
3. Replace with: `purple-500`
4. Click "Replace All"

Repeat for other blue classes:
- `blue-600` → `purple-600`
- `blue-400` → `purple-400`

**Example: Changing button colors from blue to green**

```html
<!-- BEFORE -->
<a href="https://theshiftchiro.com" class="px-6 py-2 bg-blue-500 text-white rounded-lg font-semibold hover:bg-blue-600">
    Schedule Now
</a>

<!-- AFTER -->
<a href="https://theshiftchiro.com" class="px-6 py-2 bg-green-500 text-white rounded-lg font-semibold hover:bg-green-600">
    Schedule Now
</a>
```

### Changing Text Size

Text sizes in Tailwind follow this pattern: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`, `text-3xl`, `text-4xl`, `text-5xl`, `text-6xl`

**Example: Making the hero headline smaller**

```html
<!-- BEFORE -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">...</h1>

<!-- AFTER (Make it smaller) -->
<h1 class="text-3xl md:text-4xl lg:text-5xl font-bold">...</h1>
```

The `md:` and `lg:` prefixes mean "on medium screens and larger" and "on large screens and larger." This is responsive design—it adapts to different screen sizes.

### Changing Spacing

**Padding (space inside):**
- `p-4` = All sides
- `px-4` = Left and right
- `py-4` = Top and bottom

**Margin (space outside):**
- `m-4` = All sides
- `mx-4` = Left and right
- `my-4` = Top and bottom
- `mb-6` = Bottom only

Numbers go from 1-96, with higher numbers = more space.

**Example: Adding more space between sections**

```html
<!-- BEFORE -->
<section class="py-24 md:py-32 bg-gray-900">

<!-- AFTER (More space) -->
<section class="py-32 md:py-40 bg-gray-900">
```

### Changing Border and Shadow

**Rounded corners:**
- `rounded-lg` = Slightly rounded
- `rounded-xl` = More rounded
- `rounded-full` = Circle

**Shadows:**
- `shadow-md` = Medium shadow
- `shadow-lg` = Larger shadow

**Example: Making cards more rounded**

```html
<!-- BEFORE -->
<div class="card-hover bg-gray-800 rounded-xl p-8 border border-gray-700">

<!-- AFTER -->
<div class="card-hover bg-gray-800 rounded-3xl p-8 border border-gray-700">
```

### Responsive Design Classes

This page uses three breakpoints:
- `sm:` = Small screens (640px and up)
- `md:` = Medium screens (768px and up)
- `lg:` = Large screens (1024px and up)

**Example: Show/hide on different screens**

```html
<!-- Hidden on mobile, shows on desktop -->
<div class="hidden md:flex">
    Desktop menu here
</div>

<!-- Shows on mobile, hidden on desktop -->
<div class="md:hidden">
    Mobile menu here
</div>
```

---

## Fixing and Managing Links

Links are crucial for directing visitors to important pages. Let's explore all the links in this page and how to update them.

### Understanding Links

A link in HTML looks like this:

```html
<a href="https://example.com">Click here</a>
```

Breaking it down:
- `<a>` = Link tag
- `href="..."` = Where the link goes (the address)
- `Click here` = The text that appears and is clickable
- `</a>` = Closes the link

### Types of Links in This Page

#### 1. External Links (Go to another website)

These use full URLs like `https://theshiftchiro.com`

**Location:** Throughout the page in buttons and navigation

```html
<a href="https://theshiftchiro.com" class="px-8 py-4 bg-blue-500 text-white rounded-lg">
    Schedule Now
</a>
```

#### 2. Internal Links (Jump to sections on this page)

These use `#` followed by a section ID like `#features`

```html
<a href="#features" class="text-gray-300 hover:text-blue-400">Features</a>
```

This links to:
```html
<section id="features" class="py-24 md:py-32 bg-gray-800">
```

#### 3. Email Links

```html
<a href="mailto:theshiftchiropractic@gmail.com">Email Us</a>
```

---

### Finding All Links in the Page

**Step 1: Search for all links**

Press `Ctrl+F` and search for `href=` to find every link in the document.

**Step 2: Common link locations**

| Location | Line # | Current Link |
|----------|--------|--------------|
| Desktop Schedule button | ~46 | `https://theshiftchiro.com` |
| Mobile Schedule button | ~62 | `https://theshiftchiro.com` |
| Hero "Get Immediate Care" | ~148 | `https://theshiftchiro.com` |
| Hero "Learn More" | ~152 | `#features` |
| CTA Section button | ~360 | `https://theshiftchiro.com` |
| Testimonials section | N/A | Internal links only |
| Final CTA "Schedule Now" | ~620 | `https://theshiftchiro.com` |
| Final CTA "Email Us" | ~625 | `mailto:theshiftchiropractic@gmail.com` |
| Footer links | ~700-730 | Various |

---

### Updating the Main Scheduling Link

The main link to schedule appointments appears multiple times throughout the page.

**Step 1: Find all instances**

Press `Ctrl+F` and search for: `https://theshiftchiro.com`

You'll see it appears in multiple locations.

**Step 2: Update using Find & Replace**

1. Press `Ctrl+H` to open Find & Replace
2. Find: `https://theshiftchiro.com`
3. Replace with: Your scheduling URL (e.g., `https://calendly.com/yourname`)
4. Click "Replace All"

**Step 3: Verify the changes**

After replacing, search again to make sure all instances were updated.

**Example:**

```html
<!-- BEFORE -->
<a href="https://theshiftchiro.com" class="px-8 py-4 bg-blue-500 text-white rounded-lg">
    Schedule Now
</a>

<!-- AFTER -->
<a href="https://calendly.com/drsmith" class="px-8 py-4 bg-blue-500 text-white rounded-lg">
    Schedule Now
</a>
```

---

### Updating the Email Link

**Location:** Footer section (around line 625)

```html
<a href="mailto:theshiftchiropractic@gmail.com" class="px-8 py-4 border-2 border-white text-white rounded-lg">
    Email Us
</a>
```

Also appears in the footer contact section:

```html
<a href="mailto:theshiftchiropractic@gmail.com" class="text-gray-400 hover:text-blue-400">
    theshiftchiropractic@gmail.com
</a>
```

**To update the email:**

1. Press `Ctrl+H` to open Find & Replace
2. Find: `theshiftchiropractic@gmail.com`
3. Replace with: Your email address
4. Click "Replace All"

---

### Internal Navigation Links

These links jump to sections on the same page using `#sectionname`.

**Current internal links:**
- `#features` → Features section
- `#benefits` → Benefits section
- `#testimonials` → Testimonials section
- `#faq` → FAQ section
- `#about` → About Us section

**These are in the navigation menu:**

```html
<a href="#features" class="text-gray-300 hover:text-blue-400">Features</a>
<a href="#benefits" class="text-gray-300 hover:text-blue-400">Benefits</a>
<a href="#testimonials" class="text-gray-300 hover:text-blue-400">Testimonials</a>
<a href="#faq" class="text-gray-300 hover:text-blue-400">FAQ</a>
<a href="#about" class="text-gray-300 hover:text-blue-400">About</a>
```

**Important:** These links work because the sections have matching `id` attributes:

```html
<section id="features" class="py-24 md:py-32 bg-gray-800">
<section id="benefits" class="py-24 md:py-32 bg-gray-900">
<section id="testimonials" class="py-24 md:py-32 bg-gray-800">
<section id="faq" class="py-24 md:py-32 bg-gray-800">
<section id="about" class="py-24 md:py-32 bg-gray-900">
```

**If you rename a section**, you must update both:
1. The link: `href="#newname"`
2. The section ID: `id="newname"`

---

### Social Media Links

**Location:** Footer (around line 700)

```html
<a href="#" class="text-gray-400 hover:text-blue-400" aria-label="Facebook">
    <i class="fab fa-facebook text-lg"></i>
</a>
```

Currently all set to `#` (placeholder). 

**To add social media links:**

Replace `#` with your actual social media URLs:

```html
<!-- BEFORE (Placeholder) -->
<a href="#" class="text-gray-400 hover:text-blue-400" aria-label="Facebook">
    <i class="fab fa-facebook text-lg"></i>
</a>

<!-- AFTER (Real link) -->
<a href="https://facebook.com/theshiftchiro" class="text-gray-400 hover:text-blue-400" aria-label="Facebook">
    <i class="fab fa-facebook text-lg"></i>
</a>
```

**Social media links to update:**

```html
<a href="#" aria-label="Facebook">         → https://facebook.com/yourpage
<a href="#" aria-label="Twitter">          → https://twitter.com/yourhandle
<a href="#" aria-label="Instagram">        → https://instagram.com/yourhandle
<a href="#" aria-label="LinkedIn">         → https://linkedin.com/company/yourcompany
```

---

### Broken Link Checklist

After updating links, test them:

✓ All external links (starting with `http://` or `https://`) open correct websites
✓ All internal links (starting with `#`) jump to correct sections
✓ Email link (`mailto:`) opens email client
✓ No links go to placeholder URLs like `#` or `example.com`

---

## Adding Privacy and Terms Pages

This page currently references `privacy.html` and `terms.html` in the footer, but these links don't lead anywhere yet. Let's set them up.

### Step 1: Create the Privacy Policy Page

**Create a new file:**

1. Open your text editor
2. Go to File → New
3. Paste this template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - The Shift Chiropractic">
    <title>Privacy Policy | The Shift Chiropractic</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header -->
    <header class="sticky top-0 z-50 bg-gray-900 bg-opacity-95 backdrop-blur-md border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-blue-400 to-blue-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-heart text-white text-lg"></i>
                </div>
                <span class="text-xl font-bold text-white hidden sm:inline">The Shift</span>
            </div>
            <a href="index.html" class="text-gray-300 hover:text-blue-400 transition-smooth font-medium">Back to Home</a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 md:py-32 bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold mb-12 text-white">Privacy Policy</h1>
            
            <div class="space-y-8 text-gray-300">
                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">1. Introduction</h2>
                    <p class="leading-relaxed">
                        The Shift Chiropractic ("we," "our," or "us") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">2. Information We Collect</h2>
                    <p class="leading-relaxed mb-4">
                        We may collect information about you in a variety of ways. The information we may collect on the site includes:
                    </p>
                    <ul class="list-disc list-inside space-y-2">
                        <li>Personal Information (name, email, phone number, address)</li>
                        <li>Medical History (accident details, injury information)</li>
                        <li>Insurance Information</li>
                        <li>Usage Data (how you interact with our website)</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">3. Use of Your Information</h2>
                    <p class="leading-relaxed">
                        Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the site to:
                    </p>
                    <ul class="list-disc list-inside space-y-2 mt-4">
                        <li>Process your appointment requests</li>
                        <li>Generate invoices and send billing information</li>
                        <li>Fulfill and manage purchases, orders, payments, and other transactions related to our services</li>
                        <li>Email regarding your account or order</li>
                        <li>Improve our website and services</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">4. Disclosure of Your Information</h2>
                    <p class="leading-relaxed">
                        We may share information we have collected about you in certain situations:
                    </p>
                    <ul class="list-disc list-inside space-y-2 mt-4">
                        <li><strong>By Law or to Protect Rights:</strong> If we believe the release of information about you is necessary to comply with the law</li>
                        <li><strong>Third-Party Service Providers:</strong> We may share your information with third parties that perform services for us, including payment processing and insurance coordination</li>
                        <li><strong>Your Attorney:</strong> We may share medical information with your personal injury attorney as part of your legal case</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">5. Security of Your Information</h2>
                    <p class="leading-relaxed">
                        We use administrative, technical, and physical security measures to protect your personal information. However, perfect security does not exist on the Internet.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">6. Contact Us</h2>
                    <p class="leading-relaxed">
                        If you have questions or comments about this Privacy Policy, please contact us at:
                    </p>
                    <p class="mt-4">
                        Email: <a href="mailto:theshiftchiropractic@gmail.com" class="text-blue-400 hover:text-blue-300">theshiftchiropractic@gmail.com</a><br>
                        Location: Oakland, California
                    </p>
                </div>

                <p class="text-sm text-gray-400 mt-12 pt-8 border-t border-gray-700">
                    Last Updated: January 2025
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-950 border-t border-gray-800 py-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-500 text-sm">
                &copy; 2025 The Shift Chiropractic. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

4. Save the file as `privacy.html` in the same folder as your `index.html`

---

### Step 2: Create the Terms of Service Page

**Create a new file:**

1. Open your text editor
2. Go to File → New
3. Paste this template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - The Shift Chiropractic">
    <title>Terms of Service | The Shift Chiropractic</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header -->
    <header class="sticky top-0 z-50 bg-gray-900 bg-opacity-95 backdrop-blur-md border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-blue-400 to-blue-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-heart text-white text-lg"></i>
                </div>
                <span class="text-xl font-bold text-white hidden sm:inline">The Shift</span>
            </div>
            <a href="index.html" class="text-gray-300 hover:text-blue-400 transition-smooth font-medium">Back to Home</a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 md:py-32 bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold mb-12 text-white">Terms of Service</h1>
            
            <div class="space-y-8 text-gray-300">
                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">1. Agreement to Terms</h2>
                    <p class="leading-relaxed">
                        By accessing and using the The Shift Chiropractic website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">2. Use License</h2>
                    <p class="leading-relaxed mb-4">
                        Permission is granted to temporarily download one copy of the materials (information or software) on The Shift Chiropractic website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside space-y-2">
                        <li>Modify or copy the materials</li>
                        <li>Use the materials for any commercial purpose or for any public display</li>
                        <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                        <li>Remove any copyright or other proprietary notations from the materials</li>
                        <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">3. Disclaimer</h2>
                    <p class="leading-relaxed">
                        The materials on The Shift Chiropractic website are provided on an 'as is' basis. The Shift Chiropractic makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">4. Limitations</h2>
                    <p class="leading-relaxed">
                        In no event shall The Shift Chiropractic or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on The Shift Chiropractic website.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">5. Accuracy of Materials</h2>
                    <p class="leading-relaxed">
                        The materials appearing on The Shift Chiropractic website could include technical, typographical, or photographic errors. The Shift Chiropractic does not warrant that any of the materials on the website are accurate, complete, or current. The Shift Chiropractic may make changes to the materials contained on the website at any time without notice.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">6. Links</h2>
                    <p class="leading-relaxed">
                        The Shift Chiropractic has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by The Shift Chiropractic of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">7. Modifications</h2>
                    <p class="leading-relaxed">
                        The Shift Chiropractic may revise these terms of service for the website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">8. Governing Law</h2>
                    <p class="leading-relaxed">
                        These terms and conditions are governed by and construed in accordance with the laws of California, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </div>

                <p class="text-sm text-gray-400 mt-12 pt-8 border-t border-gray-700">
                    Last Updated: January 2025
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-950 border-t border-gray-800 py-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-500 text-sm">
                &copy; 2025 The Shift Chiropractic. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

4. Save the file as `terms.html` in the same folder as your `index.html`

---

### Step 3: Verify the Links Work

Now that you've created these pages, the links in your footer should work!

**In your index.html footer (around line 825), you should already have:**

```html
<a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-smooth text-sm">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-smooth text-sm">Terms of Service</a>
```

These links are already correct! They point to the files you just created.

**Test them:**
1. Open `index.html` in your browser
2. Scroll to the footer
3. Click "Privacy Policy" - should go to `privacy.html`
4. Click "Terms of Service" - should go to `terms.html`
5. Click "Back to Home" on those pages to return to the main page

---

### Step 4: Customize the Legal Pages

You may want to customize the privacy and terms pages with your specific information.

**In privacy.html, update:**

```html
<!-- Find this section and update with your info -->
<p class="mt-4">
    Email: <a href="mailto:theshiftchiropractic@gmail.com" class="text-blue-400">theshiftchiropractic@gmail.com</a><br>
    Location: Oakland, California
</p>
```

**In both files, update the year if needed:**

```html
<p class="text-sm text-gray-400 mt-12 pt-8 border-t border-gray-700">
    Last Updated: January 2025  <!-- Change to current date -->
</p>
```

---

### Step 5: File Organization

Your project folder should now look like this:

```
your-project-folder/
├── index.html          (Main landing page)
├── privacy.html        (Privacy Policy)
├── terms.html          (Terms of Service)
└── blog.html           (Optional - Blog page)
```

**Important:** All three files must be in the same folder for the links to work correctly.

---

## Common Customizations

### Adding a Blog Link

The footer already references a blog page that doesn't exist yet.

**To add it:**

1. Create a new file called `blog.html`
2. Use a similar template as `privacy.html` and `terms.html`
3. The footer link is already there: `<a href="blog.html">`

---

### Changing the Logo

The logo is made with HTML and CSS. Find this section (around line 26):

```html
<div class="w-10 h-10 bg-gradient-to-br from-blue-400 to-blue-600 rounded-lg flex items-center justify-center">
    <i class="fas fa-heart text-white text-lg"></i>
</div>
```

**To change the icon:**

Replace `fa-heart` with another icon from Font Awesome:
- `fa-stethoscope` (stethoscope)
- `fa-hospital` (hospital)
- `fa-heartbeat` (heartbeat)
- `fa-medical-bag` (medical bag)

Visit [fontawesome.com](https://fontawesome.com) to find more icons.

---

### Adding a Phone Number

**In the header:**

Find the navigation and add:

```html
<div class="hidden md:flex items-center space-x-4">
    <a href="tel:+15105551234" class="text-gray-300 hover:text-blue-400 transition-smooth font-medium">
        (510) 555-1234
    </a>
    <a href="https://theshiftchiro.com" class="px-6 py-2 bg-blue-500 text-white rounded-lg">
        Schedule Now
    </a>
</div>
```

**In the footer contact section:**

Find the footer contact area (around line 750) and add:

```html
<li class="flex items-start gap-3">
    <i class="fas fa-phone text-blue-400 mt-1 flex-shrink-0"></i>
    <a href="tel:+15105551234" class="text-gray-400 hover:text-blue-400 transition-smooth">
        (510) 555-1234
    </a>
</li>
```

Replace `+15105551234` with your actual phone number.

---

### Updating Business Hours

In the footer, you'll see:

```html
<li class="flex items-start gap-3">
    <i class="fas fa-clock text-blue-400 mt-1 flex-shrink-0"></i>
    <span class="text-gray-400">24/7 Emergency Support</span>
</li>
```

**To change it:**

Replace `24/7 Emergency Support` with your actual hours:

```html
<span class="text-gray-400">Mon-Fri: 9AM-6PM | Sat: 10AM-4PM</span>
```

---

### Adding a Location Map

You can add a Google Map to the About section. Find the About Us section (around line 510) and add:

```html
<div class="mt-12 rounded-xl overflow-hidden">
    <iframe src="https://www.google.com/maps/embed?pb=..." width="100%" height="400" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
</div>
```

To get the embed code:
1. Go to [Google Maps](https://maps.google.com)
2. Search for your business location
3. Click the share button
4. Select "Embed a map"
5. Copy the iframe code
6. Paste it into your HTML

---

## Troubleshooting Guide

### Problem: Links Don't Work

**Symptom:** Clicking a link does nothing or shows a 404 error

**Solutions:**

1. **Check the href attribute:**
   ```html
   <!-- WRONG - missing closing quote -->
   <a href="https://example.com class="button">Link</a>
   
   <!-- RIGHT -->
   <a href="https://example.com" class="button">Link</a>
   ```

2. **For internal links, check the section ID matches:**
   ```html
   <!-- Link says #features but section is id="feature" (no 's') -->
   <!-- This won't work! -->
   <a href="#features">Link</a>
   <section id="feature">  <!-- Wrong ID -->
   ```

3. **For external links, check the full URL:**
   ```html
   <!-- WRONG - missing https:// -->
   <a href="theshiftchiro.com">Link</a>
   
   <!-- RIGHT -->
   <a href="https://theshiftchiro.com">Link</a>
   ```

---

### Problem: Text Looks Wrong or Cuts Off

**Symptom:** Text is too small, too large, or doesn't fit on the screen

**Solution:** Check the Tailwind classes:

```html
<!-- Too small? -->
<h1 class="text-2xl">Heading</h1>  <!-- Make it bigger -->
<h1 class="text-4xl">Heading</h1>  <!-- Better -->

<!-- Too large on mobile? Use responsive classes -->
<h1 class="text-2xl md:text-4xl">Heading</h1>  <!-- Small on mobile, large on desktop -->
```

---

### Problem: Colors Look Wrong

**Symptom:** Changed a color but it didn't update everywhere

**Solution:** You may have missed some instances

1. Press `Ctrl+F` to search
2. Search for the old color (e.g., `blue-500`)
3. Make sure you replaced ALL instances, not just one
4. Use Find & Replace (`Ctrl+H`) to replace all at once

---

### Problem: Mobile Menu Doesn't Work

**Symptom:** The hamburger menu on mobile doesn't open/close

**Solution:** This requires JavaScript. Make sure you have the JavaScript section at the bottom of your file:

```html
<script>
    document.addEventListener('DOMContentLoaded', function() {
        // Mobile Menu Toggle
        const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
        const mobileMenu = document.querySelector('header nav .mobile-menu');
        
        if (mobileMenuButton && mobileMenu) {
            mobileMenuButton.addEventListener('click', () => {
                mobileMenu.classList.toggle('hidden');
                // ... rest of code
            });
        }
    });
</script>
```

Don't delete this code! It makes the mobile menu work.

---

### Problem: Accordion (FAQ) Doesn't Open/Close

**Symptom:** Clicking on FAQ questions doesn't expand the answers

**Solution:** This also requires JavaScript. The code for this is in the same `<script>` section:

```html
// FAQ Accordion Toggle
const faqItems = document.querySelectorAll('.faq-item');
faqItems.forEach(item => {
    const question = item.querySelector('.faq-question');
    if (question) {
        question.addEventListener('click', () => {
            // ... accordion code
        });
    }
});
```

Make sure this code is present and not accidentally deleted.

---

### Problem: Page Layout Looks Broken

**Symptom:** Elements are overlapping or not aligned properly

**Possible causes:**

1. **Deleted a CSS class accidentally:**
   ```html
   <!-- WRONG - missing classes -->
   <div>Content</div>
   
   <!-- RIGHT - has proper classes -->
   <div class="max-w-7xl mx-auto px-4">Content</div>
   ```

2. **Didn't close a tag properly:**
   ```html
   <!-- WRONG - missing closing tag -->
   <div class="container">
       <h1>Heading
   </div>
   
   <!-- RIGHT -->
   <div class="container">
       <h1>Heading</h1>
   </div>
   ```

3. **Accidentally deleted a closing tag:**
   ```html
   <!-- WRONG -->
   <section class="py-24">
       <div class="max-w-7xl">
           <h2>Title</h2>
       <!-- Missing closing </div> -->
   </section>
   
   <!-- RIGHT -->
   <section class="py-24">
       <div class="max-w-7xl">
           <h2>Title</h2>
       </div>
   </section>
   ```

**Solution:** 
- Use your editor's Find & Replace to search for mismatched tags
- Look for red error indicators in your editor
- Compare with the original HTML file

---

### Problem: Images Don't Load

**Symptom:** You see a broken image icon instead of an image

**Solution:** Check the image URL

```html
<!-- WRONG - local file that doesn't exist -->
<img src="image.jpg">

<!-- RIGHT - external image -->
<img src="https://images.unsplash.com/photo-xxxxx">

<!-- RIGHT - local file in same folder -->
<img src="./images/photo.jpg">
```

For this landing page, all images are from external sources (Unsplash), so they should load automatically.

---

### Problem: Styling Doesn't Match Original

**Symptom:** After editing, the page looks different than expected

**Checklist:**

- [ ] Did you accidentally delete any `<style>` tags?
- [ ] Did you accidentally delete any CSS classes?
- [ ] Did you accidentally change Tailwind class names?
- [ ] Did you accidentally delete the Tailwind CDN link? (Line 11)
- [ ] Did you accidentally delete the Font Awesome link? (Line 12)

**The critical lines that must stay:**

```html
<script src="https://cdn.tailwindcss.com"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
```

If these are missing, no styling will work!

---

### Problem: Can't Find Where to Edit Something

**Solution:** Use the Find function

1. Press `Ctrl+F` (Windows) or `Cmd+F` (Mac)
2. Type the text you want to find
3. Press Enter to jump to it

**Examples:**
- Want to change "Features"? Search for `Features`
- Want to find the benefits section? Search for `Why Choose`
- Want to find a testimonial? Search for the person's name

---

## Best Practices

### Before Making Changes

1. **Make a backup:**
   - Copy your `index.html` file
   - Rename it to `index-backup.html`
   - Keep this safe in case you need to revert

2. **Test in a browser:**
   - Open your file in a web browser
   - Make sure everything works before editing

### While Making Changes

1. **Change one thing at a time:**
   - Don't edit multiple sections at once
   - This makes it easier to find problems

2. **Use Find & Replace carefully:**
   - Preview changes before replacing all
   - Some editors show you how many replacements will be made

3. **Save frequently:**
   - Press `Ctrl+S` after each major change
   - This prevents losing work

### After Making Changes

1. **Test the page:**
   - Open it in a browser
   - Click all links
   - Check on mobile and desktop
   - Test on different browsers (Chrome, Firefox, Safari)

2. **Verify nothing broke:**
   - Does the mobile menu work?
   - Do internal links jump to the right sections?
   - Do external links open in new tabs?
   - Do the FAQ accordions expand/collapse?

---

## File Structure Summary

Your final project should have:

```
project-folder/
├── index.html          ← Main landing page
├── privacy.html        ← Privacy Policy
├── terms.html          ← Terms of Service
├── blog.html           ← Blog (optional)
├── index-backup.html   ← Backup (recommended)
└── README.md           ← Documentation (optional)
```

All files should be in the same folder for relative links to work.

---

## Quick Reference: Common Edits

### Changing Business Name
1. Find: `The Shift Chiropractic`
2. Replace with: Your business name
3. Use Replace All

### Changing Main Headline
1. Find the `<h1>` tag in the hero section
2. Replace the text between `<h1>` and `</h1>`
3. Keep the tags

### Changing Schedule Link
1. Find: `https://theshiftchiro.com`
2. Replace with: Your scheduling URL
3. Use Replace All

### Changing Email
1. Find: `theshiftchiropractic@gmail.com`
2. Replace with: Your email
3. Use Replace All

### Changing Accent Color (Blue to Purple)
1. Find: `blue-500`
2. Replace with: `purple-500`
3. Find: `blue-600`
4. Replace with: `purple-600`
5. Find: `blue-400`
6. Replace with: `purple-400`
7. Use Replace All for each

### Adding Phone Number
1. Find the footer contact section
2. Add a new `<li>` with phone icon and link
3. Use `href="tel:+15105551234"` format

---

## Getting Help

If you get stuck:

1. **Check the error message:**
   - Browser console (press F12) shows JavaScript errors
   - Look for red underlines in your editor

2. **Compare with original:**
   - Open the original HTML file
   - Compare your changes side-by-side
   - Look for differences

3. **Search online:**
   - Error message + "HTML" or "CSS"
   - Most common issues have solutions online

4. **Use a validator:**
   - Visit [validator.w3.org](https://validator.w3.org)
   - Upload your HTML file
   - It will show errors and warnings

---

## Conclusion

You now have all the tools to maintain and customize The Shift Chiropractic landing page! Remember:

✓ Always keep backups
✓ Test after making changes
✓ Use Find & Replace for bulk updates
✓ Keep HTML tags intact
✓ Save frequently

Good luck with your customizations!
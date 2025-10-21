# Basic HTML Website

A multi-page website built with semantic HTML, demonstrating proper structure, navigation, forms, and SEO best practices.

## Project Overview

This project showcases the creation of a complete multi-page website using only HTML (no CSS styling), focusing on semantic markup, accessibility, and SEO optimization.

## Features

### ✅ Multiple Pages
- **Homepage (index.html)** - Main landing page with hero section, projects list, work experience, education, and testimonials
- **Projects (projects.html)** - Portfolio of completed projects with descriptions
- **Articles (articles.html)** - Blog articles about web development topics
- **Contact (contact.html)** - Comprehensive contact form and contact information

### ✅ Navigation
- Consistent navigation bar present on all pages
- Links to all pages from every page
- Clear visual indication of site structure
- Accessible navigation with semantic HTML

### ✅ Semantic HTML Structure
All pages use proper HTML5 semantic elements:
- `<header>` - Page header with logo and navigation
- `<nav>` - Navigation menus
- `<main>` - Main content wrapper
- `<section>` - Major content sections
- `<article>` - Self-contained content pieces
- `<aside>` - Complementary content (if applicable)
- `<footer>` - Page footer
- `<figure>` and `<figcaption>` - For images with captions
- `<time>` - Dates and timestamps
- `<address>` - Contact information
- `<blockquote>` and `<cite>` - Quotations and citations

### ✅ SEO Meta Tags
Each page includes:
- Charset and viewport settings
- Unique, descriptive title tags
- Meta description (unique per page)
- Meta keywords relevant to page content
- Author meta tag
- Robots meta tag for search engine indexing
- Open Graph tags for social media sharing
- Twitter Card tags
- Favicon references

### ✅ Contact Form
The contact page features a comprehensive form with:
- **Text inputs:** Name, email, phone, company, subject, timeline
- **Email input:** With proper email validation
- **Select dropdowns:** Inquiry type and budget selection
- **Textarea:** Multi-line message field
- **Radio buttons:** Referral source selection
- **Checkboxes:** Newsletter subscription and copy options
- **File upload:** Attachment support
- **Fieldsets and legends:** Logical form grouping
- **Labels:** Proper labeling for all form fields
- **Required fields:** Marked with asterisks and HTML5 validation
- **Placeholders:** Helpful input examples
- **Submit and reset buttons:** Form actions

### ✅ Additional Elements
- **Tables:** Business hours displayed in structured table format
- **Lists:** Unordered and ordered lists throughout
- **Links:** Internal navigation and external links with proper attributes
- **Contact information:** Phone, email, address with semantic tags
- **Timestamps:** Article dates using `<time>` element
- **Accessibility:** ARIA labels where appropriate, alt attributes ready for images

## File Structure

```
2-Basic/
├── index.html          # Homepage
├── projects.html       # Projects portfolio page
├── articles.html       # Blog articles page
├── contact.html        # Contact form and information
└── README.md          # Project documentation
```

## Page Descriptions

### Homepage (index.html)
- Hero section with title and tagline
- Projects list
- Work experience highlights
- Education information
- Testimonials from teachers/colleagues
- Footer with copyright

### Projects Page (projects.html)
- List of portfolio projects
- Project descriptions
- Technologies used
- Links to live demos and code repositories

### Articles Page (articles.html)
- Blog-style article listings
- Article titles and summaries
- Publication dates using `<time>` elements
- Reading time estimates
- Links to full articles

### Contact Page (contact.html)
- Comprehensive contact form with validation
- Alternative contact methods (email, phone)
- Physical location with `<address>` tag
- Social media links
- Business hours in table format

## HTML Best Practices Demonstrated

1. **Semantic Markup**
   - Uses appropriate HTML5 semantic elements
   - Meaningful structure that conveys content hierarchy
   - Proper heading levels (h1-h6) in logical order

2. **Accessibility**
   - All form inputs have associated labels
   - Required fields are clearly marked
   - Alt text ready for images
   - ARIA attributes where needed
   - Keyboard navigation friendly

3. **SEO Optimization**
   - Unique title tags for each page
   - Descriptive meta descriptions
   - Proper heading hierarchy
   - Semantic HTML for better crawling
   - Open Graph tags for social sharing

4. **Form Best Practices**
   - Proper input types (email, tel, url, etc.)
   - HTML5 validation attributes
   - Grouped form fields with fieldsets
   - Clear labels and placeholders
   - Logical tab order

5. **Link Management**
   - Descriptive link text
   - External links with `target="_blank"` and `rel="noopener noreferrer"`
   - Proper use of relative and absolute URLs

## Validation

All HTML files are structured to pass W3C HTML validation:
- Proper DOCTYPE declaration
- Valid HTML5 syntax
- Closed tags and proper nesting
- Required attributes present

## Browser Compatibility

This website works in all modern browsers:
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Opera (latest)

## Future Enhancements

This HTML structure is ready for:
- **CSS Styling** - Add visual design and layout
- **Responsive Design** - Mobile-friendly styling
- **JavaScript** - Interactive features and form validation
- **Backend Integration** - Connect form to server-side processing
- **Images** - Add actual images to enhance content
- **Icons** - Add icon fonts or SVG icons

## How to Use

1. **View the Website:**
   - Open any HTML file in a web browser
   - Navigate between pages using the navigation menu

2. **Customize Content:**
   - Replace "Your Name" with your actual name
   - Update contact information (email, phone, address)
   - Modify projects, articles, and experience sections
   - Add your own content and links

3. **Update Meta Tags:**
   - Change meta descriptions for each page
   - Update Open Graph images and URLs
   - Modify keywords to match your content

4. **Test the Form:**
   - Try filling out the contact form
   - Test form validation by submitting empty or invalid data
   - Note: Form doesn't actually submit anywhere (needs backend)

## Customization Tips

- **Logo:** Replace the square (■) symbol with your actual logo image
- **Colors:** When adding CSS, use consistent color scheme
- **Content:** Keep content concise and focused
- **Images:** Add actual project screenshots and profile photos
- **Links:** Update all "#" placeholder links with real URLs
- **Form Action:** Connect form to email service or backend API

## Learning Outcomes

By completing this project, you've learned:
- How to structure a multi-page website
- Proper use of semantic HTML5 elements
- Creating accessible navigation
- Building comprehensive forms with various input types
- Implementing SEO best practices
- Preparing HTML for future styling
- Structuring content logically

## Next Steps

1. **Add CSS styling** to make the website visually appealing
2. **Implement responsive design** for mobile devices
3. **Add JavaScript** for form validation and interactivity
4. **Connect backend** to make the contact form functional
5. **Add images** and media content
6. **Deploy** the website to a hosting service

## Resources

- [MDN HTML Documentation](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [HTML5 Semantic Elements](https://www.w3schools.com/html/html5_semantic_elements.asp)
- [Web Forms Documentation](https://developer.mozilla.org/en-US/docs/Learn/Forms)
- [HTML Validation Service](https://validator.w3.org/)

---

**Created for:** Frontend Roadmap Project #2  
**Date:** October 2025  
**Status:** HTML Structure Complete - Ready for CSS Styling
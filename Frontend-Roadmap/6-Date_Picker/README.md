# Datepicker Component (Static UI)

A beautiful static datepicker UI component built with HTML and CSS only. This project demonstrates positioning, layout techniques, and CSS styling without any JavaScript functionality.

## 🎯 Project Overview

This project creates a non-functional but visually complete datepicker component. It showcases:

- **Input field** with placeholder text and calendar button
- **Dropdown calendar** using absolute positioning
- **Calendar grid** layout using CSS Grid
- **Navigation controls** for previous/next month
- **Responsive design** that adapts to different screen sizes

## ✨ Features

- ✅ **No JavaScript** - Pure HTML & CSS implementation
- ✅ **Absolute Positioning** - Calendar dropdown positioned relative to input
- ✅ **CSS Grid Layout** - 7-column grid for calendar days
- ✅ **Responsive Design** - Mobile, tablet, and desktop support
- ✅ **Modern Styling** - Clean, professional appearance
- ✅ **Hover Effects** - Interactive visual feedback
- ✅ **Accessibility** - Keyboard focus states and ARIA labels
- ✅ **SVG Icons** - Scalable icons for calendar and navigation
- ✅ **Smooth Animations** - Slide-down effect for calendar

## 🎨 Design Features

### Input Field
- Clean white background
- Placeholder text: "dd / mm / yyyy"
- Calendar icon button on the right
- Focus state with blue border and shadow
- Responsive padding and sizing

### Calendar Dropdown
- Absolutely positioned below input
- White background with shadow
- Animated slide-down effect
- Header with month/year and navigation arrows
- 7-column grid (S M T W T F S)
- 31 days displayed for December 2022

### Interactive Elements
- **Hover effects** on day cells
- **Selected day** highlighted in blue (day 15)
- **Current day** indicator with dot (day 22)
- **Weekend days** styled in blue color
- **Navigation buttons** with hover states

## 📂 File Structure

```
6-Date_Picker/
├── index.html          # HTML structure
├── styles.css          # CSS styling
└── README.md          # Documentation
```

## 🚀 Getting Started

### View the Component

1. **Open the file**
   ```bash
   # Navigate to the folder
   cd 6-Date_Picker
   
   # Open in browser
   # Double-click index.html or
   # Right-click > Open with > Browser
   ```

2. **Test Responsiveness**
   - Open browser DevTools (F12)
   - Toggle device toolbar (Ctrl+Shift+M)
   - Test at 320px, 768px, and 1024px widths

## 🎓 CSS Concepts Demonstrated

### 1. Absolute Positioning

The calendar dropdown is positioned relative to its wrapper:

```css
.datepicker-wrapper {
    position: relative;
}

.calendar-dropdown {
    position: absolute;
    top: calc(100% + var(--spacing-md));
    left: 0;
    right: 0;
    z-index: 10;
}
```

**Key Points:**
- Parent has `position: relative`
- Child has `position: absolute`
- Positioned below input with spacing
- `z-index` ensures it appears above other content

### 2. CSS Grid for Calendar Layout

7-column grid for days of the week:

```css
.calendar-grid {
    display: grid;
    grid-template-columns: repeat(7, 1fr);
    gap: var(--spacing-xs);
}
```

**Key Points:**
- `repeat(7, 1fr)` creates 7 equal columns
- `gap` adds spacing between cells
- Auto-wrapping creates rows
- Day labels and day cells flow in order

### 3. Flexbox for Input Group

Input and button aligned horizontally:

```css
.date-input-group {
    display: flex;
    align-items: center;
}

.date-input {
    flex: 1;  /* Takes remaining space */
}
```

**Key Points:**
- `display: flex` for horizontal layout
- `flex: 1` makes input fill available space
- Button maintains its width

### 4. CSS Variables

Consistent theming throughout:

```css
:root {
    --color-primary: #3b82f6;
    --spacing-md: 1rem;
    --radius-md: 8px;
    --transition-base: 200ms ease-in-out;
}
```

**Benefits:**
- Easy color scheme changes
- Consistent spacing
- Centralized configuration
- Maintainable code

### 5. Pseudo-selectors for Visual States

```css
/* Selected day */
.day-cell:nth-child(18) {
    background: var(--color-primary);
    color: white;
}

/* Current day indicator */
.day-cell:nth-child(25)::after {
    content: '';
    position: absolute;
    bottom: 4px;
    width: 4px;
    height: 4px;
    background: var(--color-primary);
    border-radius: 50%;
}

/* Weekend styling */
.day-cell:nth-child(7n+1),  /* First column (Sunday) */
.day-cell:nth-child(7n) {   /* Last column (Saturday) */
    color: var(--color-primary);
}
```

### 6. Smooth Animations

```css
@keyframes slideDown {
    from {
        opacity: 0;
        transform: translateY(-10px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.calendar-dropdown {
    animation: slideDown var(--transition-base);
}
```

## 📱 Responsive Breakpoints

### Desktop (> 768px)
- Full size layout
- Larger fonts and spacing
- Comfortable click targets

### Tablet (481px - 768px)
- Reduced padding
- Slightly smaller fonts
- Optimized spacing

### Mobile (≤ 480px)
- Compact layout
- Smaller day cells
- Reduced gaps
- Touch-friendly sizes

## 🎨 Customization Guide

### Change Colors

Edit CSS variables:

```css
:root {
    --color-primary: #10b981;        /* Green theme */
    --color-primary-hover: #059669;
    --color-primary-light: #d1fae5;
}
```

### Change Month/Year

Update the calendar title:

```html
<h2 class="calendar-title">January 2025</h2>
```

### Adjust Calendar Size

Modify day cell sizing:

```css
.day-cell {
    min-height: 50px;  /* Larger cells */
    font-size: 1.125rem;
}
```

### Change Input Placeholder

```html
<input placeholder="Select Date" />
```

### Add More Days

Adjust for months with different day counts:

```html
<!-- For 30-day months, remove one day cell -->
<!-- For 28/29-day months, remove cells accordingly -->
```

### Position Calendar Above Input

```css
.calendar-dropdown {
    top: auto;
    bottom: calc(100% + var(--spacing-md));
}
```

## 💡 Advanced Customization Ideas

### 1. Multi-month View

```html
<div class="calendar-grid">
    <!-- First month -->
</div>
<div class="calendar-grid">
    <!-- Second month -->
</div>
```

### 2. Date Range Picker

```css
.day-cell.range-start,
.day-cell.range-end {
    background: var(--color-primary);
}

.day-cell.in-range {
    background: var(--color-primary-light);
}
```

### 3. Disabled Dates

```css
.day-cell.disabled {
    color: var(--color-text-muted);
    pointer-events: none;
    opacity: 0.5;
}
```

### 4. Year Picker

```html
<div class="year-picker">
    <button>2020</button>
    <button>2021</button>
    <button class="selected">2022</button>
    <button>2023</button>
</div>
```

### 5. Time Picker Addition

```html
<div class="time-picker">
    <input type="time" />
</div>
```

## 🛠️ Technical Details

### HTML Structure

```
datepicker-wrapper
├── date-input-group
│   ├── input (text field)
│   └── button (calendar icon)
└── calendar-dropdown
    ├── calendar-header
    │   ├── button.prev
    │   ├── h2.title
    │   └── button.next
    └── calendar-grid
        ├── day-label (×7)
        ├── day-cell.empty (×4)
        └── day-cell (×31)
```

### CSS Architecture

1. **Variables** - Centralized configuration
2. **Reset** - Normalize browser defaults
3. **Layout** - Container and spacing
4. **Components** - Modular styling
5. **States** - Hover, focus, active
6. **Responsive** - Media queries
7. **Accessibility** - Focus and motion
8. **Print** - Print-friendly styles

### Grid Layout Breakdown

```
S  M  T  W  T  F  S   ← Day labels (7 items)
.  .  .  .  1  2  3   ← Empty cells (4) + Days (3)
4  5  6  7  8  9  10  ← Days (7)
11 12 13 14 15 16 17  ← Days (7)
18 19 20 21 22 23 24  ← Days (7)
25 26 27 28 29 30 31  ← Days (7)
```

Total: 7 labels + 4 empty + 31 days = 42 cells

## 🧪 Testing Checklist

- [ ] Calendar displays correctly in Chrome
- [ ] Calendar displays correctly in Firefox
- [ ] Calendar displays correctly in Safari
- [ ] Input field shows placeholder
- [ ] Calendar button visible
- [ ] Calendar dropdown positioned below input
- [ ] Month/year displays correctly
- [ ] Navigation arrows visible
- [ ] All 31 days visible
- [ ] Day labels (S M T W T F S) visible
- [ ] Hover effects work on day cells
- [ ] Selected day (15) highlighted
- [ ] Current day (22) has dot indicator
- [ ] Weekend days colored differently
- [ ] Responsive at 320px width
- [ ] Responsive at 768px width
- [ ] Responsive at 1024px width
- [ ] Keyboard focus states visible
- [ ] No horizontal scrolling on mobile

## 📖 Learning Outcomes

By completing this project, you will understand:

1. **Absolute Positioning**
   - Position context with relative parent
   - Absolutely positioned children
   - Z-index stacking
   - Positioning relative to edges

2. **CSS Grid**
   - Creating equal-width columns
   - Using repeat() function
   - Gap property for spacing
   - Auto-wrapping grid items

3. **Flexbox**
   - Horizontal layouts
   - Aligning items
   - Flex grow/shrink
   - Space distribution

4. **Component Styling**
   - Modular CSS
   - Component-based thinking
   - Reusable patterns
   - State management with classes

5. **Responsive Design**
   - Media queries
   - Mobile-first approach
   - Breakpoint strategy
   - Flexible layouts

6. **CSS Variables**
   - Custom properties
   - Theme creation
   - Centralized values
   - Maintainability

7. **Visual States**
   - Hover effects
   - Focus states
   - Active states
   - Pseudo-selectors

8. **Accessibility**
   - ARIA labels
   - Focus indicators
   - Reduced motion
   - Keyboard navigation

## 🚀 Next Steps

### Make it Functional with JavaScript

1. **Toggle Calendar Visibility**
   ```javascript
   calendarButton.addEventListener('click', () => {
       calendar.classList.toggle('visible');
   });
   ```

2. **Generate Dynamic Days**
   ```javascript
   function generateCalendar(year, month) {
       // Calculate days in month
       // Create day elements
       // Handle empty cells
   }
   ```

3. **Date Selection**
   ```javascript
   dayCell.addEventListener('click', () => {
       dateInput.value = formatDate(day, month, year);
   });
   ```

4. **Month Navigation**
   ```javascript
   nextButton.addEventListener('click', () => {
       currentMonth++;
       updateCalendar();
   });
   ```

### Advanced Features

- Date range selection
- Min/max date restrictions
- Disabled dates
- Multiple date selection
- Localization (different languages)
- Custom date formats
- Keyboard navigation
- Touch gestures
- Animation improvements

## 🌟 Project Highlights

- ✅ **Pure CSS** - No JavaScript required
- ✅ **Modern Design** - Clean and professional
- ✅ **Fully Responsive** - Mobile to desktop
- ✅ **Absolute Positioning** - Dropdown positioning
- ✅ **CSS Grid** - 7-column calendar layout
- ✅ **Smooth Animations** - Slide-down effect
- ✅ **Interactive States** - Hover and focus
- ✅ **Accessible** - ARIA labels and focus states
- ✅ **SVG Icons** - Scalable graphics
- ✅ **Well Documented** - Comprehensive comments

## 📚 Resources

- [MDN - Position](https://developer.mozilla.org/en-US/docs/Web/CSS/position)
- [MDN - CSS Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)
- [MDN - Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout)
- [CSS Tricks - A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [CSS Tricks - Absolute Positioning](https://css-tricks.com/absolute-positioning-inside-relative-positioning/)

## 📝 Notes

- This is a **static UI component** for learning purposes
- The calendar does **not** function without JavaScript
- Perfect for understanding **CSS positioning and layout**
- Great foundation for building a **functional datepicker**
- Can be enhanced with JavaScript in future projects

---

**Project Status:** ✅ Complete  
**Difficulty Level:** Beginner to Intermediate  
**Estimated Time:** 2-3 hours  
**Last Updated:** October 2025

## 🎉 Congratulations!

You've successfully created a static datepicker UI component using only HTML and CSS! You've learned about absolute positioning, CSS Grid, and building complex layouts. This foundation will be invaluable when you add JavaScript functionality in future projects.

**Happy Coding! 🚀**

# Product Requirements Document (PRD) - Portfolio Website

## 1. Project Overview
**Goal**: Build a professional, responsive, and SEO-friendly portfolio website for a UI/UX designer.
**Technology Stack**:
-   **Core**: Pure HTML5, CSS3, JavaScript (ES6+).
-   **Frameworks**: None (No React, Vue, Tailwind, Bootstrap, etc.). Custom CSS required.
-   **Fonts**: Lato (Primary).
-   **Browser Support**: Modern browsers (Chrome, Firefox, Safari, Edge).

## 2. Design Guidelines
**Visual Source of Truth**: The design files in `instructions/page-designs` are the primary reference for layout, spacing, and visual hierarchy. Stick to the design as close as possible.
**Color Palette**:
-   Primary color is #F64134, secondary color is #3F4245, complimentary background color is #FEF6F6, main background color is #F5F5F5. The rest of the colors are likely to be extracted from the design files.
-   Common colors likely include a primary brand color (check buttons/links), neutral backgrounds (white/light gray), and text colors.
**Typography**:
-   **Font Family**: `Lato` (Google Fonts).
-   **Weights**: Use `300`, `400`, `700` as needed based on the visual weight in the designs.
**Responsiveness**:
-   **Mobile-First** or **Responsive** approach.
-   Ensure layouts adapt gracefully to mobile, tablet, and desktop screens.
-   Images and assets must be responsive.

## 3. Page Requirements & Asset Mapping

### 3.1 Global Elements
-   **Navigation**: Responsive header/navbar.
    -   *Assets*: use font icons/generic SVGs if not provided.
-   **Footer**: Standard footer with links.

### 3.2 Home Page
**Design Reference**:
-   `instructions/page-designs/home-company-projects.png` (Default view?)
-   `instructions/page-designs/home-side-projects.png` (Variant or tab view?)

**Key Sections**:
1.  **Hero Section**: Introduction, role title, potential CTA.
    -   *Assets*: Look for personal images in `assets/` (e.g., `assets/home/me.jpeg`)
2.  **Projects Gallery**: Grid or list of projects.
    -   **Tabs/Filters**: "Company Projects" vs "Side Projects" as suggested by the two design files.
    -   *Assets*:
        -   `assets/home/company-projects/`: Images for company project thumbnails.
        -   `assets/home/side-projects/`: Images for side project thumbnails.
3.  **About/Intro Snippet**: Brief text about the designer.

### 3.3 Case Studies
**General Structure**: Each case study page likely follows a similar template: Hero (Title/Banner), Overview, Role, Challenge, Solution, Results.

#### A. Floopay
-   **Design Reference**: `instructions/page-designs/casestudy-floopay.png`
-   **Assets Path**: `assets/floopay/`

#### B. Gigulu
-   **Design Reference**: `instructions/page-designs/casestudy-gigulu.png`
-   **Assets Path**: `assets/gigulu/`

#### C. Kutanapay
-   **Design Reference**: `instructions/page-designs/casestudy-kutanapay.png`
-   **Assets Path**: `assets/kutanapay/`

#### D. Totebag
-   **Design Reference**: `instructions/page-designs/casestudy-totebag.png`
-   **Assets Path**: `assets/totebag/`

### 3.4 Contact Page
-   **Design Reference**: `instructions/page-designs/contact-page.png`
-   **Functionality**: Contact form or list of contact details/social links.
-   **Assets**: Use font icons/generic SVGs if not provided.

## 4. Technical Requirements

### 4.1 HTML Structure
-   Semantic HTML5 tags (`<main>`, `<nav>`, `<article>`, `<section>`, `<aside>`, `<footer>`).
-   Accessible attributes (`alt` text for images, `aria-labels` where necessary).

### 4.2 CSS Architecture
-   **Methodology**: BEM (Block Element Modifier) or similar clean naming convention recommended.
-   **Variables**: Use CSS Custom Properties (`:root`) for colors and fonts to facilitate theme management.
-   **Reset**: Use a modern CSS reset (e.g., modern-normalize).

### 4.3 JavaScript
-   Vanila Javascript interactions (Mobile menu toggle, Project tab switching).
-   No heavy libraries.

### 4.4 SEO
-   **Meta Tags**: Title, Description, Viewport, Charset.
-   **Open Graph**: Basic OG tags for social sharing.
-   **Performance**: Lazy loading for images (`loading="lazy"`).

### 4.5 Folder Structure Proposal
```
/ (Root)
├── index.html          (Home)
├── contact.html        (Contact)
├── projects/
│   ├── floopay.html
│   ├── gigulu.html
│   ├── kutanapay.html
│   └── totebag.html
├── assets/             (Existing directory structure)
├── css/
│   ├── style.css
│   └── reset.css
└── js/
    └── main.js
```

## 5. Implementation Steps for AI Builder
1.  **Analyze Designs**: Open the specified PNG files to understand layout and spacing.
2.  **Extract Colors/Fonts**: Define CSS variables based on analysis.
3.  **Global Header/Footer**: Build responsive navigation using font icons/generic SVGs if not provided.
4.  **Home Page**: Implement the project tabs switching logic ("Company" vs "Side").
5.  **Project Pages**: Build a reusable template for common case studies sections and populate with specific content and assets.
6.  **Contact Page**: Implementation.
7.  **Final Polish**: Mobile responsiveness check and SEO meta tags.

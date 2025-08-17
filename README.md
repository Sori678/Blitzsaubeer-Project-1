# Blitzsaubeer-Project-1
A responsive static website for a fictional cleaning company, **Blitzsaubeer**. The site showcases services, builds trust, and makes it easy to get in touch or book a service. Built as Portfolio Project 1 for the Code Institute Full-Stack Developer Diploma.

## Table of Contents
- [Live Project & Repository](#live-project--repository)
- [Overview](#overview)
- [User Stories](#user-stories)
- [Features](#features)
- [UX Design](#ux-design)
- [Accessibility](#accessibility)
- [Information Architecture](#information-architecture)
- [Technologies Used](#technologies-used)
- [Screenshots](#screenshots)
- [Testing](#testing)
- [Known Bugs](#known-bugs)
- [Performance & SEO](#performance--seo)
- [Deployment](#deployment)
- [Local Development](#local-development)
- [Credits](#credits)
- [Future Enhancements](#future-enhancements)
- [Resubmission Notes](#resubmission-notes)

## Live Project & Repository
- **Live Site:** https://Sori678.github.io/Blitzsaubeer-Project-1/
- **Repository:** https://github.com/Sori678/Blitzsaubeer-Project-1

## Overview
**External user goals**
- Learn about services and prices
- Build trust through clear visuals and content
- Easily contact the company or submit a booking

**Site owner goals**
- Present a professional, consistent brand
- Attract and convert potential clients
- Collect enquiries via validated forms

## User Stories
1. **First-time visitor:** I want to quickly understand what services are offered so I can decide if they fit my needs.  
   **Acceptance:** Clear hero, “Unsere Leistungen” cards, link to full services.  
   **Implemented by:** Home hero + service cards + CTA to Services.

2. **Price-conscious user:** I want indicative pricing so I can estimate my budget.  
   **Acceptance:** Pricing visible or one click away; structured lists/tables.  
   **Implemented by:** `dienste-und-preis.html` with expandable details and price lists.

3. **Potential client:** I want to submit a booking or question easily and get confirmation.  
   **Acceptance:** Required fields; basic validation; confirmation page.  
   **Implemented by:** Booking form (Services) and FAQ form, both route to `thank-you.html`.

4. **Mobile user:** I want the site to be usable on my phone.  
   **Acceptance:** Responsive layout, mobile nav, readable text.  
   **Implemented by:** Grid layouts, responsive images, Bootstrap navbar.

## Features
### Header & Navigation
- Logo links to Home
- Bootstrap 5 responsive navbar with toggler
- Active page highlighting

### Hero (Home)
- Welcome copy with clear value proposition
- Primary CTA to Services/Booking

### Services Cards (Home)
- Responsive grid of four services
- `<picture>` sources for smaller images on mobile
- CTA buttons to booking section

### Services & Prices (`dienste-und-preis.html`)
- Consistent service blocks: image + text + expandable details
- `<details>/<summary>` used for pricing, benefits, tips
- Booking form on the same page

### Forms
- **Booking form** (Services) and **Question form** (FAQ)
- Required fields, `email`/`tel` patterns, native browser validation
- Visual feedback icons for valid/invalid states
- Both submit via **GET** to `thank-you.html` (front-end only)

### About (`uber.html`)
- Company intro and values
- Bootstrap carousel
- CTA back to booking

### FAQ (`faq.html`)
- Intro text + simple contact form

### Footer
- Contact details and social links (Font Awesome)
- Legal links: Privacy & Impressum
- Opening hours table

### Legal
- **Impressum:** `impressum.html`  
- **Privacy Policy:** `datenschutzerklarung.html`

## UX Design
- **Wireframes:** Basic layout planned for mobile and desktop.
- **Design choices:** Calm, clean palette (white/cyan/green), generous spacing, readable type.
- **Typography:** Google Fonts — Inter (body), Josefin Sans (headings).
- **Icons:** Font Awesome.

## Accessibility
- Semantic HTML structure (headings, lists, tables)
- All images include meaningful `alt` text
- Interactive icons marked `aria-hidden="true"` when decorative
- Labels tied to inputs via `for`/`id`, selects with clear labels
- Visible focus styles (`:focus-visible`) across interactive elements
- Table captions and appropriate scoping for headers
- Sufficient color contrast maintained

## Information Architecture
**Pages**
- `index.html` (Home)
- `dienste-und-preis.html` (Services & Prices + Booking)
- `uber.html` (About)
- `faq.html` (FAQ + Contact form)
- `impressum.html` (Legal notice)
- `datenschutzerklarung.html` (Privacy policy)
- `thank-you.html` (Submission confirmation)

**Folders**
assets/
css/
style.css
images/

## Technologies Used
- HTML5, CSS3
- Bootstrap 5 (CDN)
- Google Fonts (Inter, Josefin Sans)
- Font Awesome (icons)
- Git & GitHub for version control and hosting

## Screenshots
**Home**
- `assets/images/Screenshot-navbar-mobile.png`  
- `assets/images/Screenshot-navbar-homepage-desktop.png`  
- `assets/images/Screenshot-footer-mobile.png`  
- `assets/images/Screenshot-footer-service-card-desktop.png`

**Services**
- `assets/images/Screenshot-service-reservation-desktop.png`  
- `assets/images/Screenshot-service-reservation-mobile.png`

**About**
- `assets/images/Screenshot-carousel-desktop.png`  
- `assets/images/screenshot-carousel-mobile.png`

**FAQ**
- `assets/images/Screenshot-faq-form-mobile.png`  
- `assets/images/Screenshot-faq-form-desktop.png`

**Confirmation**
- `assets/images/confirmation-small.png`  
- `assets/images/confirmation-big.png`
> Ensure the file names above exactly match files in the repo (case-sensitive on GitHub Pages).

## Testing
### Validators
- **HTML:** W3C Nu Validator — no errors on all pages  
  Evidence in: `assets/validation/html/`
- **CSS:** W3C Jigsaw — no errors  
  Evidence in: `assets/validation/css/`

### Manual Test Matrix
| Area             | Test                                                  | Result |
|------------------|-------------------------------------------------------|--------|
| Navbar           | Mobile toggler opens/closes; links navigate correctly | Pass   |
| Active link      | Current page highlighted in nav                       | Pass   |
| Hero CTA         | Button navigates to Services/Booking                  | Pass   |
| Services details | `summary` toggles via mouse and keyboard              | Pass   |
| Forms required   | Submitting empty form shows native validation         | Pass   |
| Email pattern    | Invalid email prevented                               | Pass   |
| Tel pattern      | Invalid phone prevented                               | Pass   |
| Visual icons     | Valid/invalid icons update as fields change           | Pass   |
| Thank-you        | Forms redirect to `thank-you.html` (GET)              | Pass   |
| Footer links     | Social open in new tab; legal pages accessible        | Pass   |
| Images           | `<picture>` sources swap on narrow widths             | Pass   |
| Focus            | Keyboard focus visible                                | Pass   |

### Responsive Checks
- Chrome DevTools & real devices at 320px, 375px, 768px, 1024px, 1440px — layout holds as intended.

> Optional: add Lighthouse screenshots in `assets/validation/lighthouse/`.

## Known Bugs
- None observed after validation and manual testing.

## Performance & SEO
- Responsive images using `<picture>` where applicable
- Minimal render-blocking: single CSS file and Bootstrap CDN
- Per-page `<meta name="description">`
- Descriptive headings and link text
- Lighthouse evidence can be added to `assets/validation/lighthouse/`


## Deployment
### GitHub Pages
1. Push the `main` branch to GitHub.
2. Repo → **Settings** → **Pages** → Source: *Deploy from a branch*.
3. Branch: `main`, Folder: `/root`, then **Save**.
4. Site published at `https://<username>.github.io/Blitzsaubeer-Project-1/`.

### Notes on Forms
- Front-end only. Submissions use **GET** to `thank-you.html`. No server-side data storage.

## Local Development
### Prerequisites
- Modern browser

### Clone & Run
- git clone https://github.com/Sori678/Blitzsaubeer-Project-1.git
- cd Blitzsaubeer-Project-1


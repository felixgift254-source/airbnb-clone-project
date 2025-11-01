# airbnb-clone-project
This project is a full-stack clone of the popular accommodation booking platform AirBnB. The goal is to build a functional web application that allows users to browse property listings, view detailed property information, and complete bookings. The project will cover frontend development, backend APIs, database design, and deployment

Tech Stack
Frontend: HTML, CSS, JavaScript (React or similar framework)
Version Control: Git and GitHub
Design Tools: Figma for UI/UX design





---

## UI/UX Design Planning

### Design Goals

- **Clear and intuitive navigation:** Allow users to quickly find listings, view details, and complete bookings with minimal steps.
- **Responsive and accessible layout:** Ensure the app works seamlessly on both mobile and desktop, following accessibility best practices (semantic HTML, keyboard navigation, sufficient color contrast).
- **Fast content visibility:** Prioritize important information (price, location, availability, booking CTA) so users can make decisions quickly.
- **Trust and safety cues:** Display host verification, reviews, and clear pricing to build user confidence.
- **Minimal friction checkout:** Reduce form fields and steps during booking to increase conversions.

### Key Features to Implement

- Search and filter functionality (location, dates, price range, type of place, amenities).
- Pagination or infinite scroll for listing results.
- Responsive card-based listing UI with image galleries.
- Detailed listing pages with calendar availability, reviews, host info, and a map.
- Simple, secure checkout flow with booking summary, guest details, and payment placeholder.
- User authentication (signup/login) and basic profile management.
- Input validation and helpful inline error messages.
- Loading states and skeleton screens for data fetching.

### Primary Pages

| Page                  | Purpose                                                                                   | Key UI Elements                                                                                                                                               |
|-----------------------|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Property Listing View | Let users browse available properties matching their search and filter criteria.           | Search bar, filters (location, dates, price, amenities), result count, listing cards (image, title, rating, price per night), pagination/infinite scroll, map toggle. |
| Listing Detailed View | Provide comprehensive information about a selected property so users can make decisions.   | Image gallery, title & summary, price breakdown, availability calendar, booking sidebar with date selector and total price, host info, reviews, location map, amenity list, clear "Book" CTA. |
| Simple Checkout View  | Guide users through confirming a booking with minimal steps and clear cost transparency.   | Booking summary (dates, nights, per-night price), guest info form, contact details, payment placeholder, final confirmation button, cancellation policy, order summary, success confirmation screen. |

### Why User-Friendly Design Matters in a Booking System

A user-friendly design is critical for a booking platform because it directly impacts conversion rates and customer trust. Booking is often a high-friction moment: users may abandon the process if they cannot quickly find availability, understand total costs, or feel confident about safety and payment. Clear layouts, consistent affordances (buttons, inputs), informative error messages, and transparent pricing reduce confusion and friction. Additionally, responsive and accessible design broadens the user base, ensuring people on different devices and with different abilities can complete bookings reliably. Good UI/UX also reduces support requests and increases repeat bookings by creating a smooth, trustworthy experience.

---



Color styles (named tokens + hex + usage)
- --color-primary: #FF5A5F — Primary brand/accent (calls-to-action, primary buttons, links)
- --color-primary-600: #E04F52 — Hover / active state
- --color-accent: #00A699 — Secondary accent (highlights, success accents)
- --color-accent-600: #008F7F — Accent hover
- --color-bg: #FFFFFF — Page background
- --color-surface: #F7F7F7 — Cards, surface panels
- --color-muted-surface: #F1F1F1 — Secondary surfaces (inputs, dropdown backgrounds)
- --color-border: #E6E6E6 — Dividers, borders
- --color-shadow: rgba(16, 24, 40, 0.04) — Card shadow
- --color-text-primary: #222222 — Primary body text
- --color-text-secondary: #484848 — Secondary text (meta, labels)
- --color-text-tertiary: #767676 — Tertiary text / helper copy
- --color-placeholder: #BDBDBD — Input placeholders
- --color-success: #28A745 — Success messages
- --color-warning: #FFB020 — Warnings / cautions
- --color-danger: #E02424 — Errors / destructive actions
- --color-link: var(--color-primary) — Links (use primary token)
- --color-overlay: rgba(0,0,0,0.4) — Modal/backdrop overlay

Accessibility notes for colors:
- Use --color-text-primary on --color-bg for main content (aim for WCAG AA/AAA as needed).
- Use contrast-checker while theming; provide a darker variant of primary if needed for text-on-color.

Typography tokens (family, weight, size, line-height, letter-spacing)
- Font stack (preferred -> fallbacks):
  - --font-sans: "Circular", "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif
  - (Note: Circular is Airbnb’s proprietary font. If unavailable, Inter or system fonts are good substitutes.)

Font weights (tokens)
- --fw-regular: 400
- --fw-medium: 500
- --fw-semibold: 600
- --fw-bold: 700
- --fw-light: 300 (optional for subtle styles)

Type scale (desktop base: 16px). Define responsive scales for mobile if required.
- H1 (display): 40px — line-height: 48px — weight: 600 (or 700) — letter-spacing: -0.02em
- H2: 32px — line-height: 40px — weight: 600 — letter-spacing: -0.02em
- H3: 24px — line-height: 32px — weight: 600 — letter-spacing: -0.01em
- H4: 20px — line-height: 28px — weight: 600 — letter-spacing: 0
- H5: 16px — line-height: 24px — weight: 600 — letter-spacing: 0
- H6 (subheading): 14px — line-height: 20px — weight: 600 — letter-spacing: 0.01em

Body & utility text
- Body / paragraph (body-lg): 18px — line-height: 28px — weight: 400 — letter-spacing: 0
- Body / paragraph (body): 16px — line-height: 24px — weight: 400 — letter-spacing: 0
- Small / caption: 12px — line-height: 16px — weight: 400 or 500 — letter-spacing: 0.02em
- Label / overline: 11px — line-height: 16px — weight: 500 — letter-spacing: 0.06em (uppercase if used)
- Button (primary): 14px — line-height: 20px — weight: 600 — letter-spacing: 0.02em

Form & UI specifics
- Input text: 16px — line-height: 24px — weight: 400
- Placeholder: 14px — color: --color-placeholder
- Micro copy (helper/error): 12px — weight: 400 (error uses --color-danger)

Responsive hints
- Scale headings down on mobile (example: H1 from 40px → 32px, H2 32 → 26, H3 24 → 20).
- Consider using a modular scale (1.125 or 1.2) for consistent typographic rhythm.

Concrete CSS variable example (short)
:root {
  --font-sans: "Circular", "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  --fw-regular: 400; --fw-medium: 500; --fw-semibold: 600; --fw-bold: 700;
  --color-primary: #FF5A5F; --color-primary-600: #E04F52; --color-accent: #00A699;
  --color-bg: #FFFFFF; --color-surface: #F7F7F7; --color-border: #E6E6E6;
  --color-text-primary: #222222; --color-text-secondary: #484848; --color-placeholder: #BDBDBD;
  --text-size-base: 16px;
  --text-h1: 40px; --lh-h1: 48px; --text-h2: 32px; --lh-h2: 40px;
  --text-body: 16px; --lh-body: 24px; --text-small: 12px;
}

Why identifying design properties of a mockup matters (concise)
- Visual consistency: Unifies component appearance across pages and states.
- Faster developer handoff: Exact tokens remove ambiguity and speed implementation.
- Accessibility: Lets you validate color contrast, readable sizes, and focus states early.
- Scalability & theming: Central tokens make brand or mode changes (dark/light) trivial.
- Performance: Limits fonts/weights to those actually used, reducing payload.
- Maintainability: Single source of truth (variables/tokens) reduces duplicated values and bugs.
- Clear UX hierarchy: Defined sizes and weights create predictable visual rhythm and scanning patterns.


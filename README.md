# airbnb-clone-project
This project is a full-stack clone of the popular accommodation booking platform AirBnB. The goal is to build a functional web application that allows users to browse property listings, view detailed pages, and complete bookings in a secure and user-friendly way.

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

| Page                  | Purpose                                                                                   | Key UI Elements                                                               |
|-----------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| Property Listing View | Let users browse available properties matching their search and filter criteria.           | Search bar, filters (location, dates, price, amenities), result count, listing cards |
| Listing Detailed View | Provide comprehensive information about a selected property so users can make decisions.   | Image gallery, title & summary, price breakdown, availability calendar, booking CTA |
| Simple Checkout View  | Guide users through confirming a booking with minimal steps and clear cost transparency.   | Booking summary (dates, nights, per-night price), guest info form, contact details |

### Why User-Friendly Design Matters in a Booking System

A user-friendly design is critical for a booking platform because it directly impacts conversion rates and customer trust. Booking is often a high-friction moment: users may abandon the process if the flow is confusing, slow, or uncertain.

---



Color styles 
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
- 


## Project Roles and Responsibilities

This section outlines the core roles on the project and their primary responsibilities. Clear role definitions help ensure accountability, faster delivery, and a high-quality product.

- Project Manager
  - Key responsibilities: Plan and track project timelines, coordinate cross-team work, manage risks and dependencies, communicate progress to stakeholders, and remove blockers for the team.
  - Contribution: Keeps the project on schedule and aligned with business goals, enabling teams to focus on delivery.

- Product Owner
  - Key responsibilities: Define and prioritize the product backlog, write and refine user stories/acceptance criteria, decide on feature priorities, and represent customer and business needs.
  - Contribution: Ensures the team builds the right product by providing clear priorities and acceptance criteria.

- Scrum Master
  - Key responsibilities: Facilitate Agile ceremonies (standups, sprint planning, retrospectives), coach the team on Scrum practices, remove impediments, and protect the team from external interruptions.
  - Contribution: Improves team productivity and process health, helping deliver predictable value each sprint.

- Frontend Developers
  - Key responsibilities: Implement UI components, build responsive layouts, integrate with APIs, ensure accessibility, write unit and integration tests for UI, and optimize performance.
  - Contribution: Deliver a usable, performant, and accessible user experience that matches the design.

- Backend Developers
  - Key responsibilities: Design and implement APIs, manage data models and database schema, handle authentication/authorization, enforce business logic, and write backend tests.
  - Contribution: Provide reliable, secure, and scalable server-side functionality that powers the frontend.

- Designers (UI/UX)
  - Key responsibilities: Create user flows, wireframes, high-fidelity mockups, design system tokens, and handoff assets; run usability testing and iterate on designs.
  - Contribution: Provide a clear, accessible, and delightful user interface that guides implementation and reduces rework.

- QA / Testers
  - Key responsibilities: Define test plans, write and execute test cases (manual and automated), report and verify bugs, and ensure feature acceptance criteria are met.
  - Contribution: Maintain product quality by catching regressions and preventing defects from reaching users.

- DevOps Engineers
  - Key responsibilities: Configure CI/CD pipelines, manage infrastructure (IaC), monitor application health and logs, automate deployments, and manage environments (staging/production).
  - Contribution: Ensure reliable deployments, scalable infrastructure, and effective monitoring so the team can ship with confidence.

Notes on collaboration
- Cross-functional pairing: Encourage designers, frontend, and backend developers to pair early on complex features to reduce misunderstandings.
- Shared ownership: While roles have primary responsibilities, encourage shared ownership of quality and product outcomes across the team.
- Communication: Regular demos, backlog grooming, and clear acceptance criteria help reduce rework and align expectations.

- ## UI Component Patterns

Below is a list of planned reusable UI components for the project with descriptions, purpose, suggested props, and accessibility notes.

### Navbar
- Description: A responsive navigation bar with the application logo and links to primary pages (Home, Explore, Bookings, Host, Profile).
- Purpose: Provide clear, consistent navigation across the application.
- Suggested Props: `links` (array of { label, href }), `logo` (string or component), `user` (object | null)
- Notes: Implement keyboard navigation, ARIA landmarks (role="navigation"), and an accessible mobile menu (ARIA-expanded on toggles).

### Property Card
- Description: A card component that displays a property's thumbnail, title, brief description, location, price per night, and rating.
- Purpose: Surface key property details in listing grids and search results.
- Suggested Props: `id` (string), `image` (string), `title` (string), `location` (string), `price` (number | string), `rating` (number), `onClick` (function)
- Notes: Use meaningful alt text for images, include focus states, and ensure the card is keyboard actionable.

### Footer
- Description: A site footer containing informational links, social links, and legal text.
- Purpose: Offer secondary navigation and application information.
- Suggested Props: `links` (array), `social` (array), `copyright` (string)
- Notes: Keep content readable on small screens and avoid overlapping fixed positioning with main content.

### Search Bar
- Description: A search input with optional location, date, and guest controls.
- Purpose: Enable users to quickly find properties matching criteria.
- Suggested Props: `value` (string), `onChange` (function), `onSearch` (function), `placeholder` (string)
- Notes: Provide clear labels, ARIA attributes, and suggested auto-complete where relevant.

### Filters Panel
- Description: A panel or drawer that exposes filtering options (price range, property type, amenities, rating).
- Purpose: Help users narrow down listing results.
- Suggested Props: `filters` (object), `onFilterChange` (function), `onApply` (function), `onClear` (function)
- Notes: Ensure controls (checkboxes, selects) are keyboard navigable and screen-reader friendly.

### Property Details Modal
- Description: A modal dialog that shows a gallery, full description, amenities, host info, and booking CTA for a property.
- Purpose: Provide an in-depth view of a property without leaving the listing context.
- Suggested Props: `property` (object), `isOpen` (boolean), `onClose` (function)
- Notes: Trap focus when open, return focus on close, and label the dialog with aria-labelledby.

### Booking Form
- Description: A form collecting reservation dates, guest count, payment details, and contact information.
- Purpose: Facilitate completed bookings and validate required inputs.
- Suggested Props: `propertyId` (string), `onSubmit` (function), `initialValues` (object)
- Notes: Provide inline validation, associate labels with inputs, and ensure secure handling of payment fields.

### Rating Stars
- Description: A visual and interactive star-rating component used to display or collect ratings.
- Purpose: Surface user feedback on properties and allow rating interactions.
- Suggested Props: `rating` (number), `max` (number, default 5), `onRate` (function)
- Notes: Make rating keyboard-accessible and include an accessible label announcing the rating value.

### Pagination Controls
- Description: Navigational controls for paginated listing results (previous/next, page numbers).
- Purpose: Allow users to move between pages of results.
- Suggested Props: `currentPage` (number), `totalPages` (number), `onPageChange` (function)
- Notes: Provide aria-current for the active page and ensure controls are reachable by keyboard.

### User Profile Menu
- Description: A dropdown menu for user account actions (Profile, Trips, Settings, Logout).
- Purpose: Centralize account-related navigation and actions.
- Suggested Props: `user` (object), `onSelect` (function), `onLogout` (function)
- Notes: Ensure the menu is dismissible by Escape and clicking outside, and that it manages focus appropriately.

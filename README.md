# Tabuco Dental Clinic — Website

A modern, responsive dental clinic website built with pure HTML, CSS, and JavaScript.

## Live Preview

Run locally and visit: `http://localhost:8080`

## Project Structure

```
Web/
└── index.html      # Single-page website (all HTML, CSS, JS included)
```

## Features

- Sticky navbar with scroll effect and mobile hamburger menu
- Animated hero section with floating info cards
- Services grid with hover gradient effects
- Dark "Why Choose Us" section with stats
- Team section with social overlay on hover
- Patient testimonials
- Appointment booking form with success feedback
- Responsive footer with office hours
- Fade-in scroll animations (IntersectionObserver)
- Scroll-to-top button
- Fully responsive — mobile, tablet, desktop

## Sections

| Section | Description |
|---|---|
| Hero | Headline, stats, CTA buttons |
| Trust Banner | Certifications and quick highlights |
| Services | 6 service cards (General, Whitening, Cosmetic, Implants, Pediatric, Emergency) |
| Why Choose Us | Features list + stat grid |
| Our Team | 4 doctor cards with hover overlay |
| Testimonials | 3 patient reviews |
| Appointment | Booking form + contact info |
| Footer | Links, hours, social icons |

## Tech Stack

- **HTML5** — semantic structure
- **CSS3** — custom properties, grid, flexbox, animations
- **Vanilla JavaScript** — scroll effects, form handling, mobile nav
- **Font Awesome 6** — icons
- **Google Fonts** — Plus Jakarta Sans, Playfair Display

## Running Locally

```bash
# Python (recommended)
cd Web
python3 -m http.server 8080

# Then open in browser
http://localhost:8080
```

## Clinic Info (Placeholder)

Update the following in `index.html` with real details:

| Field | Current Value |
|---|---|
| Phone | (555) 123-4567 |
| Email | hello@tabucodental.com |
| Address | 123 Smile Avenue, New York, NY 10001 |
| Hours | Mon–Fri 8am–6pm · Sat 9am–3pm |

## Customization

- **Colors** — edit CSS variables at the top of the `<style>` block (`:root { ... }`)
- **Clinic name** — search and replace `Tabuco Dental` / `Tabuco Dental Clinic`
- **Doctors** — update the team cards in the `#team` section
- **Services** — add or remove cards in the `#services` section

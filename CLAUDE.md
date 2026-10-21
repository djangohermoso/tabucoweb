# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Running Locally

```bash
python3 -m http.server 8080
# Visit http://localhost:8080
```

## Architecture

This is a **single-file static website** for Tabuco Dental Clinic. All HTML structure, CSS styles, and JavaScript behavior live in `index.html` — no build step, no bundler, no dependencies to install.

**File layout:**
- `index.html` — entire site (HTML + embedded `<style>` + embedded `<script>`)
- `presentation.html` — standalone slide-deck presentation
- `res/logo.jpg` — clinic logo

**Inside `index.html`, the code is organized in order:**
1. `<style>` block (line 9) — all CSS, starting with `:root { ... }` CSS variables (colors, font, shadows)
2. HTML sections: `<!-- NAV -->` (797), `<!-- MOBILE NAV -->` (819), `<!-- HERO -->` (828), `<!-- TRUST -->` (896), `<!-- SERVICES -->` (907), `<!-- WHY US -->` (956), `<!-- TEAM -->` (1013), `<!-- TESTIMONIALS -->` (1082), `<!-- APPOINTMENT -->` (1131), `<!-- FOOTER -->` (1238), `<!-- MOBILE STICKY CTA BAR -->` (1301), `<!-- SCROLL TOP -->` (1311)
3. `<script>` block (line 1316) — handles: mobile nav toggle, scroll-based navbar style, IntersectionObserver fade-in animations, scroll-to-top button, `handleSubmit(event)` for the appointment form

**`presentation.html`** is a standalone keyboard-driven slide deck (arrow keys / Space to advance, left/up to go back). It shares no code with `index.html`.

**Appointment form** posts to Formspree (`https://formspree.io/f/mwvyzora`). The `handleSubmit` function intercepts the submit event, sends a `fetch` POST, shows a success message on the page, and resets the form. No backend needed — submissions arrive by email (see `APPOINTMENT_FORM.md`). Free plan limit: 50 submissions/month.

**External CDN dependencies** (no local fallbacks): Google Fonts (Plus Jakarta Sans, Playfair Display) and Font Awesome 6 icons — both loaded in `<head>`.

## Customization Locations

| What to change | Where |
|---|---|
| Brand colors | `:root { ... }` at the top of the `<style>` block |
| Clinic name | Search/replace `Tabuco Dental` / `Tabuco Dental Clinic` |
| Phone, email, address, hours | `<!-- APPOINTMENT -->` and `<!-- FOOTER -->` sections — current placeholders: `(555) 123-4567`, `hello@tabucodental.com`, `123 Smile Avenue, New York, NY 10001`, `Mon–Fri 8am–6pm · Sat 9am–3pm` |
| Team doctors | `<!-- TEAM -->` section |
| Services | `<!-- SERVICES -->` section |
| Formspree endpoint | `action` attribute on `#appointmentForm` and the `fetch` URL in `handleSubmit` |

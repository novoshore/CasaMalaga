# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

CasaMálaga is a static single-page website for a vacation rental property in Málaga, Spain. The entire site lives in one self-contained file: [casamalaga.html](casamalaga.html).

There is no build step, no dependencies, and no package manager. The `.next/` directory is a leftover from an abandoned Next.js scaffolding and can be ignored.

## Development

Open `casamalaga.html` directly in a browser. There is no dev server or build process.

## File structure

Everything — HTML, CSS, and JavaScript — is in `casamalaga.html`:

- Lines 1–1042: `<style>` block with all CSS
- Lines 1043–1576: HTML body sections (Header, Hero, Booking Bar, Trust Strip, The House, Gallery, Málaga Highlights, Location, CTA Band, Footer)
- Lines 1577–1638: `<script>` block with all JavaScript

## Design system (CSS custom properties)

All tokens are defined in `:root` at the top of the `<style>` block:

- **Fonts**: `--font-head` (Fraunces, serif) for headings; `--font-body` (DM Sans) for body text
- **Colors**: `--primary-600: #0E7AA7` (blue), `--accent-600: #E4572E` (coral), `--sand-50: #FBF7F0`, plus a neutral scale (`--neutral-50` through `--neutral-950`)
- **Spacing**: `--s8` through `--s96` (multiples of 8px)
- **Radius**: `--r-card: 16px`, `--r-btn: 12px`, `--r-pill: 999px`, `--r-img: 16px`
- **Shadows**: `--shadow-soft`, `--shadow-hover`

Always use these tokens rather than hardcoded values when editing styles.

## Page sections

Each section is clearly delimited by a banner comment and has a corresponding `id`:

| Section | `id` |
|---------|------|
| Header | `header` |
| Hero | `hero` |
| Booking bar | `booking-check` |
| Trust strip | `trust` |
| The House | `house` |
| Gallery | `gallery` |
| Málaga Highlights | `malaga` |
| Location | `location` |
| CTA band | `cta-band` |

## Images

Images are loaded from Unsplash via URL. There are no local image assets.

## Booking

The booking form is a UI placeholder only — the "Check availability" button shows an `alert()` directing users to WhatsApp or email. No backend or API is connected.

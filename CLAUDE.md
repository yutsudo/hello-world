# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static website project - a Progate learning platform landing page clone. The site is built with pure HTML and CSS, with no build tools, JavaScript frameworks, or backend dependencies.

## Project Structure

- `index.html` - Main landing page with header, hero section, lessons overview, call-to-action, and footer
- `stylesheet.css` - All styling including responsive design
- `top.png` - Hero section background image
- `README.md` - Brief project description

## Development

**Viewing the site:**
Simply open `index.html` in a web browser. For a more production-like environment with proper MIME types:
```bash
python3 -m http.server 8000
# Then visit http://localhost:8000
```

## Architecture Notes

**HTML Structure:**
The page is organized into semantic sections within `index.html`:
- `<header>` - Fixed navigation bar (lines 11-23)
- `.top-wrapper` - Hero section with call-to-action buttons (lines 24-35)
- `.lesson-wrapper` - Four lesson cards: HTML & CSS, jQuery, Ruby, PHP (lines 36-73)
- `.message-wrapper` - Bottom call-to-action (lines 74-82)
- `<footer>` - Site footer (lines 83-88)

**Responsive Design:**
The stylesheet implements mobile-first responsive design with three breakpoints in `stylesheet.css`:
- `@media (max-width: 1000px)` - Lessons grid changes to 2 columns (lines 206-219)
- `@media (max-width: 750px)` - Font size adjustments (lines 221-229)
- `@media (max-width: 670px)` - Mobile menu, full-width buttons, single column layout (lines 231-271)

**External Dependencies:**
- Font Awesome 4.7.0 (loaded via CDN for icons)
- Progate images (loaded via CDN from prog-8.com)

**Styling Approach:**
Uses traditional CSS with floats for layout (pre-flexbox/grid era). The fixed header uses `position: fixed` with `z-index: 10` to stay on top during scrolling (stylesheet.css:78-85).

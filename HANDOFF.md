# C&M Building Solutions - Project Handoff

**Last Updated:** March 9, 2026
**Status:** Live (Cloudflare) + In Development

---

## Quick Links

| Resource | URL |
|----------|-----|
| **Live Site** | https://cm-building-solutions.excido.workers.dev |
| **GitHub Repo** | https://github.com/Indras-Mirror/CM-Building-Solutions |
| **Local Path** | `/home/mal/AI/C&M-Building-Solutions` |

---

## Project Overview

**Client:** C&M Building Solutions
**Business:** Carpentry, cabinet making, and handyman services
**Location:** Melbourne, Australia (based in Sunbury & Greenvale)
**Target Audience:** Melbourne homeowners needing quality craftsmanship

### Business Details
- Two workers based in Sunbury and Greenvale
- Service ALL Melbourne metropolitan areas
- Currently doing big job in Altona
- Not picky about location - "go where the work is"
- Services: Carpentry, Cabinet Making, Handyman

---

## Tech Stack

| Component | Technology |
|-----------|------------|
| **Frontend** | HTML5, CSS3, Vanilla JavaScript |
| **Hosting** | Cloudflare Workers (static assets) |
| **Version Control** | GitHub (Indras-Mirror/CM-Building-Solutions) |
| **Fonts** | Playfair Display (headings), Inter (body) - Google Fonts |
| **Icons** | Custom SVG |

### No Build Tools Required
This is a static site - no npm, webpack, or build step. Just open `index.html` in a browser or serve with any static server.

---

## File Structure

```
/home/mal/AI/C&M-Building-Solutions/
├── index.html              # Main HTML file
├── css/
│   └── style.css           # All styles (1600+ lines)
├── js/
│   └── main.js             # Navigation, scroll reveal, form handling
├── images/
│   ├── C&M-Logo.png              # Original logo (white background)
│   ├── logo-transparent.png      # Logo with transparent background ★
│   ├── logo-main.svg             # SVG recreation of logo
│   ├── skirting-plank.svg        # Dark timber divider plank ★
│   ├── ornament.svg              # Diamond decorative divider
│   ├── wood-divider.svg          # Hammer tool icon
│   ├── saw.svg                   # Saw tool icon
│   ├── chisel.svg                # Chisel tool icon
│   ├── corner-flourish.svg       # Corner decoration
│   ├── banner.svg                # Header banner
│   └── logo.svg                  # Simple logo SVG
├── .gitignore
└── HANDOFF.md                   # This file
```

★ = Currently in use on live site

---

## Color Palette (CSS Variables)

```css
/* Dark Timber Theme - Warm workshop aesthetic */

/* Background Colors */
--bg-dark: #1F1410          /* Darkest - main background */
--bg-warm: #2A1A12          /* Section backgrounds */
--bg-card: #352218          /* Card backgrounds */
--bg-elevated: #3D2820      /* Elevated surfaces */
--bg-surface: #483020       /* Highest surface */

/* Timber/Wood Tones */
--timber-dark: #2D1810
--timber-medium: #4A2C1A
--timber-light: #6B4423
--timber-warm: #8B5A2B

/* Amber/Gold Accents (Primary) */
--amber-glow: #D4915C       /* Main accent color */
--amber-light: #E8B882
--amber-bright: #F5C98A
--honey: #C4853F

/* Text Colors */
--text-bright: #F5E6D3      /* Headings */
--text-light: #D4C4B0       /* Body text */
--text-muted: #A89880       /* Secondary text */
--text-dim: #7A6A58         /* Dimmed text */

/* Accent Colors */
--gold-accent: #D4A84B
--copper: #B87333
--rust: #A0522D
```

---

## Site Sections (in order)

1. **Navigation** - Sticky navbar with logo + menu links
2. **Hero** - Full viewport with tagline, CTA buttons, floating tool decorations
3. **Section Divider** - Ornament SVG
4. **Services** - 3 cards (Carpentry, Cabinet Making, Handyman)
5. **Skirting Plank** - Dark timber divider
6. **About** - Company description + feature grid + stats
7. **Ornament Divider**
8. **Service Areas** - Melbourne suburbs list (SEO section)
9. **Ornament Divider**
10. **Gallery** - Project placeholders (5 items)
11. **Skirting Plank Divider**
12. **Contact** - Form + contact details
13. **Ornament Divider**
14. **Footer** - Logo + links + copyright

---

## Completed Features

### Design & Layout
- [x] Warm amber timber color scheme (dark theme, easy on eyes)
- [x] Responsive design (mobile, tablet, desktop)
- [x] Sticky navigation with scroll effect
- [x] Mobile hamburger menu
- [x] Custom logo integration (user-generated)
- [x] Decorative SVG elements (tools, ornaments, planks)
- [x] Wood grain texture overlays
- [x] Floating tool animations in hero

### Sections
- [x] Hero with badge, tagline, CTAs
- [x] Services grid (3 cards)
- [x] About section with features
- [x] Service Areas (Melbourne suburbs for SEO)
- [x] Gallery placeholders
- [x] Contact form with validation
- [x] Footer

### Technical
- [x] CSS variables for easy theming
- [x] Scroll reveal animations
- [x] Form validation (client-side)
- [x] Smooth scroll navigation
- [x] Notification system for form feedback

### Deployment
- [x] GitHub repository setup
- [x] Cloudflare Workers deployment
- [x] Auto-deploy on git push

---

## Pending / Future Work

### High Priority
- [ ] **Custom domain** - cmbuildingsolutions.com.au ($20.60/year at CrazyDomains)
- [ ] **Real gallery images** - Replace placeholders with actual project photos
- [ ] **Contact details** - Add real phone number and email
- [ ] **Form backend** - Connect form to actually send emails (Formspree, EmailJS, or custom)

### SEO Improvements
- [ ] **Schema markup** - LocalBusiness structured data
- [ ] **sitemap.xml** - For search engine crawling
- [ ] **robots.txt** - Crawl instructions
- [ ] **Google Business Profile** - Create/claim listing
- [ ] **Meta tags refinement** - Open Graph, Twitter cards
- [ ] **Image alt text** - Add to all images

### Content Additions
- [ ] **Testimonials section** - Customer reviews
- [ ] **Before/After gallery** - Transformation photos
- [ ] **FAQ section** - Common questions
- [ ] **Business hours** - When available for calls
- [ ] **Project process** - "How it works" steps
- [ ] **Click-to-call** - Tapable phone on mobile

### Technical Enhancements
- [ ] **Lazy loading images** - Performance
- [ ] **Image optimization** - WebP conversion
- [ ] **Analytics** - Google Analytics or Cloudflare Analytics
- [ ] **SSL** - Already handled by Cloudflare

---

## Deployment Instructions

### Current Setup (Cloudflare Workers)
Site auto-deploys when you push to GitHub main branch.

### To Update the Site:
```bash
cd /home/mal/AI/C\&M-Building-Solutions
# Make your changes
git add .
git commit -m "Description of changes"
git push
# Cloudflare will auto-deploy within ~30 seconds
```

### To Preview Locally:
```bash
cd /home/mal/AI/C\&M-Building-Solutions
python3 -m http.server 8080
# Open http://localhost:8080
```

### Connecting Custom Domain:
1. Buy domain from CrazyDomains or VentraIP
2. In Cloudflare dashboard: Workers & Pages → cm-building-solutions → Settings → Custom Domains
3. Add your domain (e.g., cmbuildingsolutions.com.au)
4. Update nameservers at your registrar to Cloudflare's
5. Wait for DNS propagation (up to 24 hours)

---

## Services Offered (Current List)

### Carpentry Services
- Door installations & repairs
- Skirting boards & architraves
- Timber framing
- Decking & pergolas
- Flooring repairs & installations

### Cabinet Making
- Custom cabinets
- Kitchen cabinetry & modifications
- Laundry fit-outs
- Built-in wardrobes
- Storage solutions

### Handyman Services
- Caulking & sealing
- General home repairs
- Fixture & fitting installations
- Property maintenance
- Tiling & waterproofing

---

## Service Areas (Current List)

### North West
Sunbury, Greenvale, Craigieburn, Roxburgh Park, Tullamarine, Airport West, Essendon, Moonee Ponds

### North & CBD
Melbourne CBD, North Melbourne, Brunswick, Coburg, Preston, Reservoir, Epping, Bundoora

### West & South West
Altona, Footscray, Sunshine, St Albans, Werribee, Melton, Bacchus Marsh, & Beyond

---

## Known Issues / Notes

1. **Gallery placeholders** - Currently showing generic text, need real photos
2. **Contact info** - Shows "Contact us for details" - needs real phone/email
3. **Form submission** - Currently simulated, needs backend integration
4. **Logo** - User-generated PNG, could be refined for better transparency

---

## GitHub Credentials

- **Repo:** https://github.com/Indras-Mirror/CM-Building-Solutions
- **Token:** Stored in user's environment (check ~/.claude or env vars)

---

## Cloudflare Details

- **Account:** excido
- **Worker URL:** cm-building-solutions.excido.workers.dev
- **API Key:** Stored securely (check user's Cloudflare dashboard)
- **Email:** User needs to provide for full API access

---

## Resume Prompt

When starting a new session, use this prompt:

```
I'm continuing work on the C&M Building Solutions website project.

Project location: /home/mal/AI/C&M-Building-Solutions
Live site: https://cm-building-solutions.excido.workers.dev
GitHub: https://github.com/Indras-Mirror/CM-Building-Solutions

Read the HANDOFF.md file at /home/mal/AI/C&M-Building-Solutions/HANDOFF.md for full project context, including:
- File structure
- Color palette
- Completed features
- Pending work
- Deployment instructions

I want to continue with: [describe what you want to work on]
```

---

## Contact Info to Add (When Available)

- Phone: _______________
- Email: _______________
- Business hours: _______________
- ABN: _______________ (optional, for footer)

---

*Generated by Claude Code - Session March 9, 2026*

# Cervejaria Du Baú - AI Coding Guidelines

## Project Overview
Static HTML/CSS website for Du Baú craft brewery in São Bento do Sapucaí, Brazil. Simple responsive site with 4 main pages: home, beers, events, and location map.

## Architecture
- **Static site**: No build tools, frameworks, or server-side code
- **File structure**: Root-level HTML files, single `style.css`, images in `imagens/` folder
- **Language**: Portuguese (pt-BR) content throughout

## Key Patterns

### HTML Structure
Each page follows consistent layout:
```html
<header class="hero">
  <nav class="menu">...</nav>
  <div class="hero-content">...</div>
</header>
<section class="content-section">...</section>
<footer>...</footer>
```

### Navigation
- Mobile-responsive hamburger menu with JavaScript toggle
- Links use `onclick="toggleMenu()"` for mobile closure
- **Issue**: Some navigation links point to non-existent files (e.g., `cardapio.html`, `imagens.html`)

### Styling Conventions
- CSS variables for brand colors:
  ```css
  :root {
    --verde-escuro: #0b3d2e;  /* Dark green */
    --dourado: #d4af37;       /* Gold */
  }
  ```
- Hero sections use gradient backgrounds with dark overlays
- Cards use `box-shadow` and `transform: translateY(-5px)` hover effects

### Content Patterns
- Beer listings: Name, style description, price (e.g., "R$ 12,00")
- Event cards with image overlays
- WhatsApp integration: `https://wa.me/5512997410925`
- Instagram: `https://www.instagram.com/dubaucervejariaartesanal`

## Development Workflow
1. Edit HTML files directly in root directory
2. Update `style.css` for styling changes
3. Add images to `imagens/` folder (supports JPG, PNG, HEIC)
4. Test by opening HTML files in browser

## Common Tasks
- **Adding new beer**: Follow `.cerveja` class structure in `cervejas.html`
- **New event**: Use `.evento-card` with image overlay pattern from `eventos.html`
- **Navigation updates**: Maintain consistent menu structure across all pages
- **Responsive design**: Test mobile menu toggle functionality

## Known Issues to Address
- `mapa.html` is empty - needs Google Maps embed
- Broken navigation links to `cardapio.html` and `imagens.html`
- Inconsistent navigation menus between pages

## External Dependencies
- Google Fonts: Playfair Display (headings), Montserrat (body)
- WhatsApp and Instagram links for contact
- Google Maps iframe for location (when implemented)</content>
<parameter name="filePath">c:\Users\Business\Documents\PROJETO VOLÚNTARIO\cervejaria-dubau\.github\copilot-instructions.md
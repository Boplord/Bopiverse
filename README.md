# Bopiverse Website  

A three-page site (**Home**, **About**, **Contact**) showcasing the Bopiverse NFT project.  
Layout is built with Flexbox and CSS Grid, accessible on both desktop and mobile devices.  

## Design  
- Pure HTML & CSS  
- CSS variables for layout and spacing  
- Breakpoints at 700px and 1024px  
- Minimal black/white palette with strong contrast  

## Features  
- Hamburger menu using a hidden checkbox (CSS-only, mobile view)  
- Keyboard navigation and visible focus styles (skips hidden links when menu closed)  
- Skip link for screen readers  
- Image gallery with hover/focus effects  
- Contact form with native HTML validation  
- Reduced-motion support  

## Accessibility  
Tested with keyboard navigation and tab order.  
All pages include landmarks (`header`, `nav`, `main`, `footer`), `alt` text, and focus outlines.  

## CSS Interactivity

### Hamburger menu
```css
@media (max-width: 700px) {
  .nav-toggle:checked ~ .site-nav,
  .nav-toggle:checked ~ nav {
    transform: translateY(0);
    opacity: 1;
    pointer-events: auto;
    transition: transform .25s ease, opacity .2s ease;
  }

  .nav-toggle:not(:checked) ~ .site-nav a,
  .nav-toggle:not(:checked) ~ nav a {
    pointer-events: none;
    visibility: hidden;
  }

  .nav-toggle:checked + .hamburger span:nth-child(2) { opacity: 0; }
  .nav-toggle:checked + .hamburger span:nth-child(1) { transform: translateY(0) rotate(45deg); }
  .nav-toggle:checked + .hamburger span:nth-child(3) { transform: translateY(0) rotate(-45deg); }
} 
```

### Gallery Image Focus/Hover
```css
.nft-card a:hover img,
.nft-card a:focus img {
  transform: scale(1.03);
  filter: brightness(0.85);
}

.gallery a:focus-visible { outline: none; }

.nft-card a:focus-visible img {
  transform: scale(1.03);
  filter: brightness(0.85);
}
```


### Visible focus outline
```css
a:focus-visible {
  outline: 2px solid #fff;
  outline-offset: 2px;
}
```
**Jim H. Björklund**

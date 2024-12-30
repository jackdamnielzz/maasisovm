# Styling System Documentation

This document outlines the current styling system that must be preserved during CMS integration. The styling system is built on a modular architecture using vanilla CSS.

## CSS Architecture

### File Organization
```
css/
├── Base
│   ├── reset.css          # CSS reset and normalization
│   ├── base.css           # Base element styles
│   └── utilities.css      # Utility classes
│
├── Layout
│   ├── grid.css          # Grid system
│   ├── layout.css        # Layout structures
│   └── sections.css      # Section styling
│
├── Components
│   ├── navigation.css    # Navigation styles
│   ├── footer.css        # Footer styles
│   ├── forms.css         # Form elements
│   ├── buttons.css       # Button styles
│   ├── cards.css         # Card components
│   └── cookie-banner.css # Cookie notice
│
├── Features
│   ├── iso-blocks.css    # ISO certification blocks
│   ├── iso-27001.css     # ISO 27001 specific styles
│   ├── hover-tiles.css   # Interactive tiles
│   └── hero.css          # Hero section styles
│
├── Responsive
│   ├── responsive-global.css     # Global responsive styles
│   ├── responsive-navigation.css # Navigation responsive
│   ├── responsive-layout.css     # Layout responsive
│   └── responsive-components.css # Component responsive
│
└── Animations
    └── animations.css    # Animation definitions
```

## Naming Conventions

### BEM Methodology
- Block: Standalone entity (e.g., `.card`)
- Element: Part of block (e.g., `.card__title`)
- Modifier: Block/element variant (e.g., `.card--featured`)

### Utility Classes
- Prefix-based naming:
  - Layout: `l-*` (e.g., `l-container`)
  - Spacing: `m-*`, `p-*` (margin, padding)
  - Typography: `t-*` (e.g., `t-heading`)
  - Display: `d-*` (e.g., `d-flex`)

## Component Styling

### Base Components
Each component follows these principles:
- Self-contained styles
- Minimal external dependencies
- Responsive by default
- Accessible styling

### Modular Scale
Typography and spacing use a consistent scale:
```css
:root {
  --space-xs: 0.25rem;
  --space-sm: 0.5rem;
  --space-md: 1rem;
  --space-lg: 2rem;
  --space-xl: 4rem;
}
```

## Color System

### Primary Colors
```css
:root {
  --color-primary: #007bff;
  --color-secondary: #6c757d;
  --color-accent: #28a745;
}
```

### Semantic Colors
```css
:root {
  --color-success: #28a745;
  --color-warning: #ffc107;
  --color-error: #dc3545;
  --color-info: #17a2b8;
}
```

## Typography

### Font Families
```css
:root {
  --font-primary: 'Arial', sans-serif;
  --font-secondary: 'Georgia', serif;
  --font-monospace: 'Courier New', monospace;
}
```

### Font Sizes
```css
:root {
  --text-xs: 0.75rem;
  --text-sm: 0.875rem;
  --text-base: 1rem;
  --text-lg: 1.125rem;
  --text-xl: 1.25rem;
}
```

## Responsive Design

### Breakpoints
```css
/* Mobile First Approach */
@media (min-width: 576px) { /* Small devices */ }
@media (min-width: 768px) { /* Medium devices */ }
@media (min-width: 992px) { /* Large devices */ }
@media (min-width: 1200px) { /* Extra large devices */ }
```

### Responsive Patterns
- Mobile-first approach
- Fluid typography
- Flexible grids
- Responsive images
- Adaptive layouts

## Animation System

### Transition Defaults
```css
:root {
  --transition-fast: 150ms ease-in-out;
  --transition-normal: 300ms ease-in-out;
  --transition-slow: 500ms ease-in-out;
}
```

### Animation Classes
- `.fade-in`: Opacity transition
- `.slide-up`: Upward slide animation
- `.scale-in`: Scale animation
- `.rotate`: Rotation animation

## Integration Guidelines

### CSS Isolation
1. Use specific class prefixes for CMS content
2. Maintain separation of concerns
3. Avoid global style pollution
4. Use CSS modules where appropriate

### Style Inheritance
1. Define clear parent-child relationships
2. Use CSS custom properties for theming
3. Maintain consistent spacing system
4. Preserve responsive patterns

### Performance Considerations
1. Minimize CSS specificity conflicts
2. Optimize selector performance
3. Reduce redundant styles
4. Maintain current minification

## Testing and Validation

### Style Testing
- Cross-browser compatibility
- Responsive design verification
- Animation performance
- Style isolation validation

### Performance Metrics
- CSS file size monitoring
- Selector complexity analysis
- Rendering performance
- Animation frame rates

## Documentation Updates
This document should be updated when:
- New styling patterns are introduced
- Color schemes are modified
- Typography system changes
- Animation patterns are added
- Responsive breakpoints are adjusted

# Fixed Components Documentation

This document details the fixed components that must be preserved during CMS integration. These components are essential to the website's functionality and design consistency.

## Header Component
**Location:** components/header.html
**Related Files:**
- CSS: css/navigation.css, css/responsive-navigation.css
- JavaScript: None (pure HTML/CSS implementation)

### Structure
- Main navigation menu
- Mobile-responsive hamburger menu
- Logo placement
- Contact information display

### Integration Requirements
- Preserve responsive behavior
- Maintain current navigation structure
- Keep existing styling and animations
- Ensure mobile menu functionality remains intact

## Footer Component
**Location:** components/footer.html
**Related Files:**
- CSS: css/footer.css, css/responsive-components.css

### Structure
- Contact information section
- Social media links
- Legal links (Privacy Policy, Terms, etc.)
- Copyright information

### Integration Requirements
- Maintain current layout and styling
- Preserve responsive design
- Keep all external links functional

## Cookie Banner
**Location:** Injected via JavaScript
**Related Files:**
- JavaScript: js/cookie-banner.js
- CSS: css/cookie-banner.css

### Functionality
- GDPR-compliant consent management
- Local storage for user preferences
- Customizable messaging
- Accept/Reject options

### Integration Requirements
- Preserve all current functionality
- Maintain GDPR compliance
- Keep preference persistence
- Retain current styling and animations

## Scroll-to-Top Button
**Location:** Injected via JavaScript
**Related Files:**
- JavaScript: js/scroll-to-top.js
- CSS: css/scroll-to-top.css

### Functionality
- Appears after scrolling threshold
- Smooth scroll animation
- Responsive design
- Accessibility features

### Integration Requirements
- Maintain current behavior
- Preserve smooth scrolling
- Keep responsive design
- Retain accessibility features

## Common CSS Dependencies
All fixed components rely on these base CSS files:
- css/reset.css: Base CSS reset
- css/base.css: Global styles
- css/utilities.css: Utility classes
- css/responsive-global.css: Global responsive styles

## JavaScript Dependencies
Key JavaScript files that must be preserved:
- js/main.min.js: Combined and minified core functionality
- Individual component scripts (cookie-banner.js, scroll-to-top.js)

## Integration Considerations

### Component Isolation
1. Each fixed component should be isolated as a standalone module
2. CSS should be scoped to prevent conflicts with CMS styles
3. JavaScript functionality should be encapsulated
4. Dependencies should be clearly documented

### Style Preservation
1. Maintain current CSS architecture
2. Preserve class naming conventions
3. Keep responsive breakpoints consistent
4. Retain current animation implementations

### Performance Optimization
1. Maintain current minification process
2. Preserve lazy loading where implemented
3. Keep current caching strategies
4. Retain performance optimization techniques

### Accessibility
1. Preserve ARIA attributes
2. Maintain keyboard navigation
3. Keep screen reader compatibility
4. Retain current accessibility features

## Testing Requirements

### Functional Testing
- Verify all interactive elements work as expected
- Test responsive behavior across breakpoints
- Validate form submissions where applicable
- Check all external links

### Cross-browser Testing
- Test in all major browsers
- Verify mobile functionality
- Validate responsive design
- Check animations and transitions

### Performance Testing
- Monitor load times
- Check resource usage
- Verify caching behavior
- Test under different network conditions

## Documentation Updates
This document should be updated when:
- New fixed components are added
- Existing components are modified
- Integration requirements change
- New dependencies are introduced

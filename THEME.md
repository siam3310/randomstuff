# Theme System Documentation

## Overview

This project now uses an ultra-fast and lightweight theme system with minimal color variables supporting two main themes: bright white (light) and true black (dark).

## Theme Structure

### Core Files
- `src/assets/theme.css` - Main theme definitions and utility classes
- `src/layouts/base.astro` - Theme application and imports
- `src/assets/style.css` - Legacy variable mappings for compatibility
- `src/assets/global.css` - Global styles using theme variables
- `src/assets/item.css` - Content-specific styles using theme variables

### Theme Variables

#### Background Colors
- `--bg-primary` - Main background color
- `--bg-secondary` - Secondary background (cards, inputs)
- `--bg-tertiary` - Tertiary background (subtle highlights)

#### Text Colors
- `--text-primary` - Main text color
- `--text-secondary` - Secondary text (labels, captions)
- `--text-tertiary` - Tertiary text (subtle/disabled text)

#### Border Colors
- `--border-primary` - Main border color
- `--border-secondary` - Subtle border color

#### Accent Colors
- `--accent-primary` - Primary accent color
- `--accent-secondary` - Secondary accent color
- `--link-color` - Link color
- `--link-hover` - Link hover color

## Theme Classes

### Main Themes
- `.light-theme` - Bright white theme
- `.dark-theme` - True black theme

### Accent Color Utilities
- `.accent-blue` - Blue accent color scheme
- `.accent-green` - Green accent color scheme
- `.accent-red` - Red accent color scheme
- `.accent-purple` - Purple accent color scheme
- `.accent-orange` - Orange accent color scheme

### Utility Classes
- `.bg-primary`, `.bg-secondary`, `.bg-tertiary` - Background utilities
- `.text-primary`, `.text-secondary`, `.text-tertiary` - Text color utilities
- `.border-primary`, `.border-secondary` - Border utilities
- `.minimal-shadow` - Minimal shadow for subtle depth

## Usage

### Applying Themes
The theme is applied to the `<html>` element in `base.astro`:
```html
<html lang="en" class="light-theme">
```

To switch themes, change the class:
```javascript
document.documentElement.className = 'dark-theme';
```

### Using Accent Colors
Apply accent color classes to containers:
```html
<div class="accent-blue">
  <!-- Content will use blue accent colors -->
</div>
```

### Using Variables in CSS
```css
.my-component {
  background-color: var(--bg-secondary);
  color: var(--text-primary);
  border: 1px solid var(--border-primary);
}
```

## Performance Features

- **Minimal CSS footprint** - No heavy shadows or complex effects
- **CSS custom properties** - Efficient theme switching
- **Simple transitions** - Smooth but lightweight animations
- **Clean markup** - Semantic HTML structure
- **Mobile-ready** - Foundation prepared for responsive design

## Theme Switching

The theme system supports:
- Manual theme switching via JavaScript
- System preference detection (`prefers-color-scheme`)
- Theme persistence via localStorage
- Smooth transitions between themes

## Migration Notes

- Heavy shadows replaced with minimal shadow system
- Complex gradients and visual effects removed
- Hardcoded colors replaced with theme variables
- Components refactored to use CSS custom properties
- Lightweight design prepared for mobile/responsive enhancements
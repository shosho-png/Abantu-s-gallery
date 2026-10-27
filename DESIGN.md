# Abantu's Gallery Design System

## Brand Overview

Abantu's Gallery is a science communication consultancy specializing in participatory visual, sonic, and arts-based methods for social science and humanities research in South Africa. We bridge the gap between experts and the public through innovative, accessible communication approaches.

**Core Values**
- Decolonising knowledge systems
- Contributing to quality education and reducing inequality (SDG 4 & 10)
- Maintaining participatory two-way communication between experts and public

**Target Audience**
- Primary: Institutions, researchers, and NGOs seeking science communication services
- Secondary: Students interested in disseminating research creatively

## Color Palette

The design uses a grayscale palette to maintain focus on content and accessibility.

| Token | Value | Usage |
|-------|-------|-------|
| `--color-black` | `#000000` | Primary text, headings, high-contrast elements |
| `--color-gray-900` | `#1a1a1a` | Secondary headings, emphasized text |
| `--color-gray-700` | `#404040` | Body text, subtitles |
| `--color-gray-500` | `#808080` | Supporting text, captions, borders |
| `--color-gray-300` | `#cccccc` | Disabled states, subtle borders |
| `--color-gray-100` | `#f5f5f5` | Backgrounds, section dividers |
| `--color-white` | `#ffffff` | Primary backgrounds, cards, containers |

**Contrast Requirements**
- Body text vs background: ≥ 4.5:1
- Large text (≥ 18px) and icons: ≥ 3:1
- All color combinations meet WCAG AA standards

## Typography

### Type Scale

| Role | Size | Line Height | Letter-spacing | Weight |
|------|------|-------------|----------------|--------|
| Display | 72px | 1.1 | -0.02em | 600 |
| H1 | 48px | 1.2 | -0.01em | 600 |
| H2 | 32px | 1.25 | -0.01em | 550 |
| H3 | 24px | 1.3 | 0 | 550 |
| Body | 16px | 1.6 | 0 | 400 |
| Small | 14px | 1.5 | 0.01em | 400 |
| Caption | 12px | 1.5 | 0.02em | 400 |

### Font Families

```css
--font-display: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
--font-body: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
```

**Type Usage Rules**
- Headings use negative letter-spacing for tight, modern appearance
- Body text uses default letter-spacing for readability
- Small text and captions use positive letter-spacing for clarity
- Max line length for body copy: 65ch (≈ 65 characters)

### Three-Weight System

- **Read (400)**: Body copy, descriptions
- **Emphasize (550)**: UI text, labels, navigation, subheadings
- **Announce (600)**: Headlines, buttons, emphasized content

## Spacing System

Based on 8px grid for consistency and rhythm.

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | 8px | Small gaps, icon spacing |
| `--space-2` | 16px | Paragraph spacing, padding |
| `--space-3` | 24px | Section padding, card spacing |
| `--space-4` | 32px | Container margins |
| `--space-5` | 48px | Section margins |
| `--space-6` | 64px | Large section spacing |
| `--space-8` | 96px | Hero section spacing |

## Components

### Buttons

**Primary Button**
- Background: `--color-black`
- Text: `--color-white`
- Padding: 12px 24px
- Border-radius: 4px
- Letter-spacing: 0.02em
- Hover: Darken background to `--color-gray-900`
- Transition: 200ms ease-out

**Secondary Button**
- Background: transparent
- Text: `--color-black`
- Border: 1px solid `--color-gray-500`
- Padding: 12px 24px
- Border-radius: 4px
- Letter-spacing: 0.02em
- Hover: Background `--color-gray-100`

### Cards

**Project Card**
- Background: `--color-white`
- Border: 1px solid `--color-gray-300`
- Border-radius: 8px
- Padding: `--space-3`
- Hover: Border `--color-gray-500`, slight lift (transform: translateY(-2px))
- Transition: 300ms ease-out

**Service Card**
- Background: `--color-gray-100`
- Border-radius: 8px
- Padding: `--space-4`
- Hover: Background `--color-gray-300`

### Navigation

**Top Navigation**
- Background: `--color-white`
- Border-bottom: 1px solid `--color-gray-300`
- Height: 64px
- Logo: 24px font-weight 600
- Links: 14px font-weight 550, letter-spacing 0.02em
- Active state: Border-bottom 2px solid `--color-black`

### Forms

**Input Fields**
- Background: `--color-white`
- Border: 1px solid `--color-gray-500`
- Border-radius: 4px
- Padding: 12px 16px
- Font-size: 16px
- Focus: Border `--color-black`, outline none
- Error: Border color red (if needed in future)

## Interactive Elements

### Node Network Visualization

The zettelkasten-inspired node network represents connections between research projects, stakeholders, and services.

**Visual Properties**
- Nodes: Circular, gray-700 background, white text
- Edges: Thin gray-300 lines
- Active node: Black background, white text
- Hover state: Gray-500 background
- Animation: Smooth 300ms transitions

**Interaction Rules**
- Click node to navigate to related content
- Hover shows connection preview
- Responsive to touch and mouse
- Canvas-based for performance

### Motion Timing

- Small interactions: 150-200ms
- Hover states: 200ms
- Page transitions: 300ms
- Large animations: 400ms

**Easing**
- Enter: ease-out
- Exit: ease-in (60-70% of entrance duration)

## Layout

### Container System

- Max-width container: 1200px
- Centered with auto margins
- Mobile padding: 16px
- Desktop padding: 32px

### Grid System

- 12-column grid for complex layouts
- Desktop: 4-column layout for project cards
- Tablet: 2-column layout
- Mobile: 1-column layout

### Section Spacing

- Standard section spacing: `--space-6` (64px)
- Hero section: `--space-8` (96px)
- Tight sections: `--space-4` (32px)

## Accessibility

- All interactive elements have visible focus states
- Images include alt text
- Color never used alone to convey meaning
- Text remains readable at 150% zoom
- Keyboard navigation supported throughout
- Minimum touch target: 44×44px for mobile

## Safe Areas

Keep key information within central 70-80% of canvas, ≥ 50px from edges to avoid platform UI overlays and crop zones.

## Iconography

Use consistent icon family with:
- 2px stroke width
- 4px corner radius
- No mixing filled and outlined icons at same hierarchy level
- Icons for actions: navigation, search, menu, contact

## Anti-Cliché Rules

Avoid these common AI-generated patterns:
- Warm beige/cream/orange-brown backgrounds (use neutral grays)
- Purple gradient washes
- Inter/Roboto/Arial as display typefaces without intentional pairing
- Rounded cards with colored left-border accents
- Icons beside every heading
- Multiple solid buttons for same action in one viewport
- Hover states that turn text gray
- Hand-drawn SVG people as decoration
- Invented metrics or meaningless filler copy

## Responsive Breakpoints

- Mobile: < 640px
- Tablet: 640px - 1024px
- Desktop: > 1024px

## File Structure

```
/
├── index.html          # Main prototype website
├── DESIGN.md           # This design system
├── css/
│   └── styles.css      # Main stylesheet (if extracted)
├── js/
│   └── main.js         # Interactive scripts (if extracted)
└── assets/
    └── images/         # Project images and assets
```

## Content Guidelines

### Voice and Tone

- Professional yet accessible
- Academic but not overly formal
- Clear, direct communication
- Emphasize participatory, collaborative approach
- Use plain language where possible

### Copy Rules

- Headlines: Concise, action-oriented
- Body: 15-18 words per sentence average
- Avoid jargon unless necessary for research context
- Explain technical terms when first used
- Active voice preferred

## Implementation Notes

This design system is intended for:
1. Prototype website development
2. Future marketing materials
3. Client-facing presentations
4. Training materials and workshops

All values are CSS custom properties for easy theming and maintenance. The grayscale palette can be extended with accent colors in future iterations if brand requirements evolve.

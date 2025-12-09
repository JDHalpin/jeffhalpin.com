# Responsive Portfolio Website

## Overview
Create a responsive portfolio website featuring a home page with 5 accordions. Greek placeholder titles for each section. When each accordion is opened, content contains cards for case studies (4 cards per accordion). When cards are tapped, they expand to full width and variable height. Code is commented for easy updates and uses Tailwind CSS.

## Requirements
- Single-page HTML with Tailwind CSS (via CDN)
- 5 accordion sections with Greek placeholder titles (Αλφα, Βήτα, Γάμμα, Δέλτα, Έψιλον)
- Each accordion contains 4 case study cards
- Card click expands to full-width modal overlay
- Fully responsive (mobile → desktop)
- Well-commented code for maintainability

## Structure
```
├── Header (sticky, logo/name)
├── Main
│   ├── Accordion 1 – Αλφα
│   │   └── Grid of 4 cards
│   ├── Accordion 2 – Βήτα
│   │   └── Grid of 4 cards
│   ├── Accordion 3 – Γάμμα
│   │   └── Grid of 4 cards
│   ├── Accordion 4 – Δέλτα
│   │   └── Grid of 4 cards
│   └── Accordion 5 – Έψιλον
│       └── Grid of 4 cards
└── Modal (hidden, full-width expanded card view)
```

## Tailwind Classes Used
- Layout: `max-w-5xl`, `mx-auto`, `px-4`, `py-8`, `space-y-4`
- Grid: `grid`, `gap-4`, `sm:grid-cols-2`, `lg:grid-cols-4`
- Cards: `bg-gray-50`, `rounded-lg`, `p-4`, `hover:shadow-md`, `transition`
- Modal: `fixed`, `inset-0`, `z-50`, `bg-black/60`, `w-full`, `min-h-screen`

## JavaScript Behavior
1. Accordion toggle: add/remove `.open` class, rotate chevron icon
2. Card click: populate modal with `data-title` and `data-body`, show modal
3. Modal close: X button, backdrop click, or Escape key

## Customization Points
- Accordion titles: `<span>` inside `.accordion-trigger`
- Card content: `data-title`, `data-body` attributes + visible `<h3>`, `<p>`
- Add/remove cards: duplicate/delete `.card` divs
- Styling: modify Tailwind classes inline

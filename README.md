# Research Portal

A GitHub Pages site for personal research across software architecture and philosophy. Each research topic is self-contained in its own folder with independent styling and navigation.

## Repository Structure

```
/
├── index.html                 # Root landing page (research discovery hub)
├── README.md                  # This file
├── event-sourcing/            # Event sourcing architecture research
│   ├── index.html             # Topic landing page
│   ├── styles.css             # Topic-specific styles
│   ├── axon-framework-research.html
│   ├── manual-event-sourcing-research.html
│   ├── comparison.html
│   ├── event-sourcing-architecture-guide.html
│   └── greenfield-spring-boot-event-sourcing.html
└── spring-boot-three-tier/    # Spring Boot architecture research
    ├── index.html             # Topic landing page
    └── spring-architecture-guide.html
```

## Research Topics

### Event Sourcing (`event-sourcing/`)
Exploratory research into implementing event sourcing in a Spring Boot application. Compares framework-driven (Axon) vs. manual implementation approaches, with focus on CQRS patterns, concurrency control, and production trade-offs.

- **Landing page:** `./event-sourcing/index.html`
- **Key pages:** Architecture guide, Axon Framework analysis, manual implementation guide, greenfield implementation, comparison matrix

### Spring Boot Three-Tier Architecture (`spring-boot-three-tier/`)
Research into traditional three-tier architecture patterns for Spring Boot applications, exploring layered design principles, dependency management, and best practices for building maintainable enterprise applications.

- **Landing page:** `./spring-boot-three-tier/index.html`
- **Key pages:** Spring architecture guide

## Adding a New Research Topic

To add a new research area:

### 1. Create the Topic Folder

```bash
mkdir -p {topic-name}
```

### 2. Add Topic Files

Create these minimal files in the new folder:

**`{topic-name}/index.html`** — Topic landing page
```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Your Topic Title</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
<main class="shell">
  <section class="hero">
    <div class="eyebrow">Research Category</div>
    <h1>Topic Name</h1>
    <p class="lead">Brief description of research area</p>
  </section>
  <!-- Add your research content here -->
  <footer style="margin-top: 60px; text-align: center; font-size: 0.9rem; color: var(--muted); padding-bottom: 40px;">
    &copy; 2026 {Topic Name} Research
  </footer>
</main>
</body>
</html>
```

**`{topic-name}/styles.css`** — Copy from an existing topic folder (e.g., `event-sourcing/styles.css`)

### 3. Update Root Landing Page

Add a new card to `index.html` in the `.grid.auto` section:

```html
<article class="card home">
  <span class="card-kicker">Category</span>
  <h2 class="card-title">Topic Name</h2>
  <p class="card-description">
    Brief description of what this research covers.
  </p>
  <ul class="card-features">
    <li>Key point 1</li>
    <li>Key point 2</li>
    <li>Key point 3</li>
  </ul>
  <a href="./{topic-name}/index.html" class="card-link">Explore Topic</a>
</article>
```

## Design System

All pages share a cohesive visual design:

- **Color palette:** Blues, grays, accents (defined as CSS variables in `styles.css`)
- **Typography:** Georgia/Palatino for headings, system UI sans-serif for body
- **Components:** Hero sections, card grids, tables, code blocks, collapsible sections
- **Responsive:** Mobile-first approach with breakpoints at 600px and 900px

### CSS Variables (per topic's `styles.css`)
```css
--bg: background color
--text: text color
--muted: secondary text
--accent: primary call-to-action color
--line: border/divider color
--radius: border-radius for cards
```

Each topic folder contains its own `styles.css` to maintain independence, though the variables and class names follow the same pattern for consistency.

## Deployment

This repo is hosted on GitHub Pages. The site is automatically deployed when changes are pushed to the main branch.

**Live site:** https://david-stuart-justice.github.io

## Writing Guidelines

Research pages should:
- Lead with the main insight or question
- Support claims with specific examples or data
- Acknowledge trade-offs and limitations
- Use clear headings to guide readers
- Avoid marketing language ("cutting-edge," "robust," "seamless")
- Structure arguments step-by-step

See individual research pages for examples of expected tone and depth.

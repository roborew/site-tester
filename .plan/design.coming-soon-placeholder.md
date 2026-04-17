```markdown
# Design Brief: Digital Pulse Coming Soon

## 1. Purpose & Audience
*   **Core Goal:** Provide a professional "Coming Soon" landing page for DNS and hosting verification.
*   **Target Audience:** General web traffic, stakeholders, and developers checking deployment status.
*   **Tone:** Intentional, polished, and "alive." It should look like a deliberate choice rather than a default server page.

## 2. Visual Style & Aesthetic
*   **Concept:** "The Digital Pulse" — A minimalist dark-mode aesthetic featuring a central interactive/animated element that represents activity and progress.
*   **Feel:** Slick, Creative, Minimal.
*   **Theme:** Modern Dark Mode.

## 3. Color Palette (Tailwind Classes)
*   **Primary Background:** `bg-slate-950` (Deep, premium dark)
*   **Secondary Surface:** `bg-slate-900/50` (Subtle depth)
*   **Accent Color:** `text-indigo-500` / `bg-indigo-500` (Trust and tech)
*   **Primary Text:** `text-slate-100` (High contrast)
*   **Muted Text:** `text-slate-400` (Hierarchy)

## 4. Typography
*   **Font Stack:** Clean Sans-serif (Inter or Geist via Tailwind default).
*   **Headings:** `font-bold tracking-tight`
*   **Body:** `font-light`

## 5. Iconography
*   **Set:** Lucide Icons (via CDN).
*   **Key Icons:**
    *   `Zap` or `Activity`: To represent the "pulse."
    *   `Globe`: For the domain/DNS context.
    *   `Mail`: For the contact hint.

## 6. Layout & Sections
*   **Hero Section (Full Screen):**
    *   A centered vertical stack using `flex flex-col items-center justify-center min-h-screen`.
    *   **The Visual Element:** A central "Pulse" — an SVG circle with a slow, breathing CSS scale animation and a soft `shadow-indigo-500/20` outer glow.
    *   **Messaging:** Large, crisp "Coming Soon" heading followed by a muted sub-text: "We're currently configuring our digital home. Stay tuned."
*   **Subtle Creative Element:** 
    *   A background grid pattern (`bg-[grid-white/0.05]`) or a soft radial gradient flare in the corner to break the flat black.
*   **Footer:**
    *   Small, centered text: "Domain Verified & Active" with a small green `check-circle` icon.
    *   Optional: "Inquiries: hello@yourdomain.com"

## 7. Interactive Elements
*   **Entrance Animation:** Fade-in for text elements using Tailwind's `animate-pulse` (subtle) or custom CSS transitions for the central orb.
*   **Hover States:** Subtle glow increase on the central element when the mouse is nearby.

## 8. Accessibility & Performance
*   **Contrast:** Slate-100 on Slate-950 exceeds WCAG AAA.
*   **Semantics:** Use `<main>` for the hero and `<footer>` for the bottom links.
*   **Performance:** Zero external dependencies beyond Tailwind CSS and Lucide Icons.

---

## Prototype Generation Template

> **For ux-dev execution only.** This section is consumed by the orchestrator to generate the prototype.

### Slug
`coming-soon-placeholder`

### Output Directory
`.prototype/coming-soon-placeholder/`

### Stack
- Vanilla HTML5 (framework-agnostic)
- Tailwind CSS (via CDN)
- Lucide Icons (via CDN)

### Page Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Coming Soon</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://unpkg.com/lucide@latest"></script>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen flex flex-col items-center justify-center">
  <!-- Background subtle grid or radial gradient -->
  
  <main class="flex flex-col items-center justify-center text-center px-4">
    <!-- Central Pulse Element -->
    <!-- Animated SVG circle with breathing scale + indigo glow -->
    
    <!-- Heading -->
    <h1 class="text-5xl md:text-6xl font-bold tracking-tight mt-8">Coming Soon</h1>
    
    <!-- Subtext -->
    <p class="text-slate-400 font-light mt-4 text-lg max-w-md">
      We're currently configuring our digital home. Stay tuned.
    </p>
  </main>
  
  <footer class="absolute bottom-8 text-center">
    <!-- "Domain Verified & Active" with check-circle icon -->
    <!-- Optional contact email -->
  </footer>
  
  <script>lucide.createIcons();</script>
</body>
</html>
```

### Rationale
By choosing a deep slate and indigo palette, we convey stability and technical competence. The "Pulse" animation serves a functional purpose: it visually confirms the page is "live" and the browser is rendering correctly, which is the primary goal of a DNS verification placeholder. The minimal footprint ensures near-instant load times across all global regions.
```

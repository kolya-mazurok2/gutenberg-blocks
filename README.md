# 📦 Custom Gutenberg Blocks

This repository contains a set of **custom WordPress Gutenberg blocks** built without relying on ACF.  
The goal is to demonstrate advanced Gutenberg development concepts such as custom attributes, Inspector/Toolbar controls, InnerBlocks, dynamic server-side rendering, block variations, and theme.json integration.

---

## 🚀 Blocks Overview

### 1. Testimonial Block
A structured testimonial card with rich editing options and schema.org support.

**Requirements:**
- Quote text (RichText, multiline, ~300 chars).
- Author name (inline RichText).
- Author position (inline RichText, e.g. “CEO at Company”).
- Avatar image (MediaUpload).
- Alignment control (left / center / right).
- Inspector toggle: “Show company logo instead of avatar.”
- Background color from theme.json palette.
- **Extra challenge:**
  - Output schema.org structured data (`Review`).
  - Responsive design: handle missing avatar gracefully.

---

### 2. Call-to-Action (CTA) Block
A flexible marketing block with background options and responsive behavior.

**Requirements:**
- Heading (RichText).
- Subheading (multiline RichText).
- Button text (RichText).
- Button URL (URLInput + toggle: open in new tab).
- Inspector controls:
  - Background color & gradient support.
  - Block height (auto / full viewport).
- Toolbar: text alignment options.
- **Extra challenge:**
  - Different background images for desktop vs mobile.
  - Button style variations (primary / secondary).
  - Support wide/full alignments.

---

### 3. Hero Section Block (with InnerBlocks)
A locked hero layout with predefined slots for content.

**Requirements:**
- InnerBlocks template:
  - Heading (H1).
  - Subheading (paragraph).
  - CTA button (reusable CTA block).
- Layout locked: user cannot remove/reorder slots.
- Background image upload + focal point picker.
- Overlay option: color + opacity slider.
- **Extra challenge:**
  - Integration with template parts (site-wide “Hero” pattern).
  - Style presets (minimal / overlay / split layout).

---

### 4. Dynamic Recent Posts Block
A server-rendered block that fetches and displays posts dynamically.

**Requirements:**
- Inspector controls:
  - Number of posts (1–10).
  - Select category (dynamic dropdown).
  - Toggle: show featured image.
- Editor preview: placeholder posts if none exist.
- Front-end rendered via PHP `render_callback`.
- **Extra challenge:**
  - Support custom post types.
  - Layout options: grid vs list.
  - Pagination toggle (show more / next link).
  - Semantic & accessible markup (`<article>`, `<h2>`, `<time>`).

---

### 5. Notice / Alert Block (with Variations)
A flexible alert component with multiple variations and transforms.

**Requirements:**
- Base block: Notice with RichText content.
- Variations:
  - Info (blue + info icon).
  - Warning (yellow + warning icon).
  - Success (green + check icon).
  - Error (red + X icon).
- Toolbar: convert between variations (transform).
- Inspector: toggle “Dismissible” (close button on front-end).
- **Extra challenge:**
  - Semantic markup: `<aside role="alert">`.
  - Styles applied via theme.json instead of inline CSS.
  - Nested InnerBlocks support (optional extra content).
  - Persist dismiss state per user (via `localStorage`).

---

## 🏆 Skills Demonstrated
- Attributes & RichText usage
- InspectorControls & BlockControls
- MediaUpload and URLInput handling
- InnerBlocks with template locking
- Server-side rendering (`render_callback`)
- Block variations & transforms
- theme.json integration
- Accessibility and semantic HTML
- Real-world responsive/editor challenges

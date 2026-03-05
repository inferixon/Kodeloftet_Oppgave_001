# Portfolio Dev Plan (Learning Project)

Goal: build a single-page portfolio with a centered page frame, a sticky header, clear sections, and responsive layout from mobile up to 4K.

Non-goals (for now): real project content, complex JS features, heavy animations.

---

## Information Architecture

Single page (one `index.html`):
- **Header (sticky)**: logo + horizontal nav + social icons (GitHub, LinkedIn).
- **Main**:
	- **Hero**: big “Velkommen” line.
	- **About** (“Om meg”): text + photo.
	- **Projects**: 3 cards in a row (placeholders), with a hover effect.
	- **Background**: an image + a simple animated effect (parallax is optional).
- **Footer**: horizontal flex bar with closing text + contacts.


---

## Design / Layout Rules

### Page frame
- Use a centered container for the whole page (max width) so content does not stretch too wide on 2K/4K.
- Keep consistent horizontal padding.
- Keep readable line length for paragraphs.

### Responsive strategy
Breakpoints (simple):
- **Mobile**: 1 column, stacked layout. (optional)
- **Tablet / small desktop**: 2 columns where it makes sense. (optional)
- **Desktop / 2K-4K**: 3 project cards in one row, comfortable spacing.

Projects grid behavior:
- Mobile: 1 card per row
- Tablet: 2 cards per row
- Desktop+: 3 cards per row

### Accessibility baseline
- All nav links are real anchors (`href="#..."`) and match section `id`s.
- Visible focus state for keyboard navigation.
- Images have meaningful `alt` text.

---

## Step-by-step Build Plan

### 0) Prep
- Decide final section ids: `#hjem`, `#om`, `#prosjekter`, `#kontakt` (if added).
- Decide logo text (name or short brand).
- Decide social links (GitHub for sure; optionally add more later).

Definition of done:
- You can describe the page structure from memory.

### 1) Header (sticky)
What to build:
- A header that stays at the top while scrolling.
- Inside header: 3 parts in one row:
	1) logo (left)
	2) nav list (center)
	3) social icons/links (right)

Layout notes:
- Use Flexbox for the header row.
- Nav itself is a horizontal flex list.

Definition of done:
- Header remains visible when scrolling.
- Logo, nav, social links are aligned nicely.
- On small screens: nav can wrap or stack (keep it simple).

### 2) Hero
What to build:
- Hero section with a strong “Velkommen” headline.
- Short intro text.

Definition of done:
- Clear visual hierarchy: headline > text.
- Hero works on mobile and large screens.

### 3) About (Om meg)
What to build:
- A section with text + photo.

Layout notes:
- Mobile: photo stacked.
- Desktop: two-column layout (text + image).

Definition of done:
- Image scales correctly (no overflow).
- Text stays readable (not too wide).

### 4) Projects (3 cards + hover)
What to build:
- 3 placeholder project cards.
- Each card has: title, short text, and a placeholder link/button.

Hover effect goal (Steam-like, but simple):
- On hover: slight lift + smoother shadow + subtle background/scale.

Definition of done:
- Desktop shows 3 cards in a row.
- Hover effect feels responsive but not distracting.
- Mobile shows 1 card per row.

### 5) Background image + animated effect
Two options (pick one):
- **Option A (simple, recommended)**: background image on `body`/main container + subtle CSS animation (e.g. slow gradient overlay).
- **Option B (parallax, optional later)**: fixed background (`background-attachment: fixed`) on desktop only, with a fallback for mobile.

Definition of done:
- Background does not reduce readability.
- Performance stays OK on mobile.

### 6) Footer (flex bar)
What to build:
- A horizontal footer bar with:
	- closing text / signature
	- contacts (at least GitHub link)

Definition of done:
- Footer content aligns horizontally on desktop.
- Footer stacks neatly on mobile.

### 7) Final responsive pass (mobile → 4K)
Checklist:
- No horizontal scrolling at any width.
- Container stays centered on wide screens.
- Spacing scales nicely.
- Images stay sharp and properly sized.

---

## Task Checklist (practical)
- [ ] Sticky header with 3 areas (logo / nav / social)
- [ ] Hero “Velkommen”
- [ ] About section (text + photo)
- [ ] Projects section (3 cards + hover)
- [ ] Background image + simple animated effect
- [ ] Footer (flex, closing text + contacts)
- [ ] Responsive layout (mobile, tablet, desktop, 2K-4K)

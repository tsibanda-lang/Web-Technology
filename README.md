# Profile & Mini-Portfolio

A one-page semantic HTML5 profile and mini-portfolio website for the Web Technologies (CIS2103) practical assignments.

## Project files

- `index.html` contains the semantic page structure and the profile, skills, portfolio and contact sections.
- `style.css` contains the site's custom mobile-first CSS, box-model spacing, Flexbox, Grid and media queries.
- `PROMPT_LOG.md` records the AI prompt, raw output, edited version and reflection from Assignment 1.
- `profile-picture.jpg` should contain the profile image used in Assignment 1. The image was not included in the ZIP recovered for Assignment 2, so add the original image file before submitting.

## Styling approach

Custom CSS is used for the overall colour palette, typography, card appearance, spacing, form controls, focus styles and responsive layout. Tailwind utilities are used intentionally for two sections:

- **Main navigation:** Tailwind Flexbox, wrapping, alignment and responsive gap utilities keep navigation links tidy on narrow screens.
- **Contact form:** Tailwind Grid utilities arrange fields in one column by default and two columns from the medium breakpoint.

This division avoids repeating every style in both systems: custom CSS controls the overall design and detailed component appearance, while Tailwind handles the layout utilities in the navigation and contact form. Tailwind is loaded using its CDN, so an internet connection is needed for those utility classes to apply.

## Responsive Notes

### Breakpoints tested

The page is designed for these target viewport widths:

- Mobile: approximately 375px
- Tablet: approximately 768px
- Desktop: approximately 1280px

**Before submission:** open the page in a browser, use Developer Tools' device toolbar, check all three widths, and confirm there is no horizontal overflow, overlapping text or broken navigation. Only state that testing is complete after you have performed these checks.

### Flexbox vs. Grid

- **Flexbox** is used for the profile header, which aligns the profile image and introduction. The navigation also uses Tailwind Flexbox utilities to wrap and space links.
- **CSS Grid** is used for the Skills & Interests and Portfolio cards. `repeat(2, minmax(0, 1fr))` creates two equal columns at tablet/desktop widths, with a single column on mobile.
- **Tailwind Grid** is used in the Contact Me form to make fields one column on small screens and two columns at the `md` breakpoint.

### Custom responsive CSS

The base styles are mobile-first. A custom `min-width: 48rem` media query adjusts the header, card grid and contact form for tablet and desktop screens. A second `min-width: 80rem` query adjusts spacing on wide desktop screens.

## Accessibility and testing checklist

- Semantic HTML landmarks and section headings are retained.
- The navigation has an accessible label.
- The profile image has alternative text.
- Contact fields have labels and browser validation attributes.
- Keyboard focus is visibly highlighted.
- [ ] Test at approximately 375px.
- [ ] Test at approximately 768px.
- [ ] Test at approximately 1280px.
- [ ] Check the browser console for errors.
- [ ] Restore `profile-picture.jpg` before submitting.

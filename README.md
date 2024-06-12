# Odin Admin Dashboard
## About
This admin dashboard design attempts to recreate the design provided inside the TOP assignment.
It features:
- A dark theme
- Responsive features
- Multiple grid layouts
- Custom design for hover and focus states
- Simple color schemes defined using CSS custom properties
## What I learned
- CSS `fill` and `stroke` properties for SVG icons cannot be used on `<img>` elements.
- Using Emmet shortcuts helped tremendously when adding wrapper links, for example.
- `border-radius: 50%` did not act how I expected for some reason, so I used `border-radius: 9999px` for rounded corners instead.
- Using `rem` instead of `px` made scaling much easier. It also prevented me from using strange pixel values. Effectively forcing me to use a system of paddings and margins.
- Using the `grid-template` shortcut can make the code more confusing to read.
- I used a linear gradient that switches colors instantly to create the backgrounds for the focused sidebar links and the cards.
```css
background: linear-gradient(to right, var(--accent), var(--accent) .5rem, var(--white) .5rem, var(--white));
```
- Nesting makes this behaviour much easier to understand (in my opinion):
```css
.card {
  /* ... */
  .icon {
    opacity: 0;
  }
  &:hover {
    .icon {
      opacity: 0.5;
      &:hover {
        opacity: 1;
      }
    }
  }
}
```
## Todos
- [ ] Responsive design
- [ ] Accessibility
- [ ] Semantic HTML
- [ ] SEO
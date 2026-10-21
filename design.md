# UI Design System --- Visual Reference Specification

> Purpose: Recreate the same overall visual style shown in the reference
> screenshots. This is a reusable visual design guide for a website or
> app. It describes appearance and layout patterns only, not
> product-specific features or content.
>
> **Colour accuracy:** Hex values are close visual estimates from
> screenshots. Exact original source tokens cannot be confirmed from
> raster images alone. Colours inside supplied logos and illustrations
> are intentionally excluded.

## 1. Overall visual style

-   Soft, modern, friendly interface with generous whitespace.
-   Near-white cool background, dark navy-charcoal text, pale pastel
    surfaces, and restrained accent colours.
-   Large rounded corners, thin low-contrast borders, and broad, subtle
    shadows.
-   Large headings with a clean, slightly rounded sans-serif appearance.
-   Cards use spacious internal padding and clear visual hierarchy.
-   Use a consistent spacing, radius, typography, and colour-token
    system throughout the project.
-   Preserve original supplied logo and illustration artwork without
    recolouring or applying global tints.

## 2. Core colour tokens

  ------------------------------------------------------------------------
  Token                    HEX                     Usage
  ------------------------ ----------------------- -----------------------
  `color.background`       `#F9FAFC`               Main page background

  `color.surface`          `#FFFFFF`               Panels, input fields,
                                                   dialogs, floating
                                                   navigation

  `color.surface.warm`     `#FEFBF6`               Warm off-white card
                                                   surfaces

  `color.text.primary`     `#171B2B`               Main headings and
                                                   important labels

  `color.text.secondary`   `#626B7D`               Supporting text and
                                                   inactive navigation

  `color.text.muted`       `#A5A7AA`               Placeholder text and
                                                   disabled content

  `color.border`           `#E4E5EA`               Default outlines and
                                                   separators

  `color.accent.orange`    `#F6A04A`               Selected states and
                                                   warm highlights

  `color.accent.blue`      `#3767D8`               Search and selected
                                                   blue interface details

  `color.accent.teal`      `#64C5CC`               Small decorative
                                                   accents

  `color.success`          `#5EAD69`               Success and
                                                   confirmation indicators

  `color.danger`           `#D92F32`               Destructive or exit
                                                   actions

  `color.overlay`          `#20212A` at 30--40%    Scrim behind modal
                           opacity                 dialogs

  `color.shadow`           `#243044` at 8--12%     Soft elevation under
                           opacity                 floating surfaces
  ------------------------------------------------------------------------

### Pastel card palette

Use these as reusable card-background options. Keep text contrast
accessible and do not apply these colours to the artwork inside cards.

  Token           HEX         Optional decorative circle   Small accent
  --------------- ----------- ---------------------------- --------------
  `card.blue`     `#BDD3FC`   `#B1C7F6`                    `#83A9E8`
  `card.indigo`   `#5F6FE0`   `#7173C6`                    `#F0A45B`
  `card.mint`     `#C4EBF0`   `#B3E2E8`                    `#64C5CC`
  `card.sky`      `#CEE7FD`   `#BBDFF4`                    `#78B4D8`

### Soft gradient palette

For large welcome/hero surfaces, use a subtle gradient made from pale
peach, blush, cream, and mint. Avoid sharp transitions or high
saturation.

-   `gradient.peach`: `#F8D8C6`
-   `gradient.blush`: `#E9DDF0`
-   `gradient.cream`: `#FFF0D8`
-   `gradient.mint`: `#DDF1E7`

A low-contrast diagonal or horizontal gradient is suitable. Optional
oversized circles can be placed inside the hero surface with low opacity
and clipped to its bounds. Keep this treatment limited to selected hero
areas rather than every page.

## 3. Typography

Use the original font if available. Otherwise, use **Poppins** or a
similar clean, rounded sans-serif family.

  ------------------------------------------------------------------------
  Text style                Approx. size Weight           Use
  ---------------- --------------------- ---------------- ----------------
  Hero heading                 40--46 px 600--700         Main
                                                          introductory
                                                          heading

  Large page                   30--35 px 500--600         Page title
  heading                                                 

  Section heading              30--34 px 500--600         Content section
                                                          titles

  Card title                   26--30 px 500--600         Main card labels

  Body text                    22--27 px 400              Descriptions and
                                                          supporting copy

  Input                        24--28 px 400              Search/input
  placeholder                                             hints

  Navigation label             19--22 px 500              Bottom
                                                          navigation text

  Small helper                 16--19 px 400              Supporting hints
  text                                                    where space is
                                                          limited
  ------------------------------------------------------------------------

These sizes are visual-reference estimates for a large screenshot scale.
In implementation, use responsive CSS units and adapt sizes to the
actual viewport. Recommended line-height: `1.2–1.35` for headings and
`1.35–1.5` for body copy. Avoid excessively thin text weights.

## 4. Spacing and layout

Use a consistent spacing scale rather than unrelated one-off values.

  Token          Value Typical use
  ------------ ------- ---------------------------
  `space.1`       4 px Tiny icon/text gap
  `space.2`       8 px Tight internal gap
  `space.3`      12 px Compact component spacing
  `space.4`      16 px Standard small gap
  `space.5`      20 px Input and card spacing
  `space.6`      24 px Standard layout gap
  `space.7`      28 px Card/grid gap
  `space.8`      32 px Page and panel padding
  `space.10`     40 px Large section spacing
  `space.12`     48 px Hero-to-content spacing
  `space.14`     56 px Major vertical separation

-   Typical horizontal page padding: `24–36 px`, responsive to viewport
    width.
-   Standard two-column grid gap: `20–30 px`.
-   Use equal-width grid cards with consistent heights when the content
    allows.
-   Use enough bottom padding that scrollable content is not hidden
    behind fixed navigation.
-   Prefer flexible sizing and content-driven heights over fixed heights
    that may clip text.

## 5. Corner radius, borders, and shadows

  Component                       Recommended treatment
  ------------------------------- -------------------------------
  Hero/header surface             44--52 px lower corner radius
  Main content card               26--32 px radius
  Input/search field              26--32 px radius
  Grouped panel                   24--30 px radius
  Floating navigation container   Fully pill-shaped
  Selected navigation item        Fully pill-shaped
  Modal/dialog                    34--42 px radius
  Primary action button           18--24 px radius
  Circular icon button            50% radius
  Border                          1--2 px, low contrast
  Shadow                          Soft, broad, low opacity

Use shadows to gently lift floating surfaces from the page. Avoid dark,
sharp, or overly prominent shadows. A white surface plus a faint outline
is usually enough for grouped panels.

## 6. Cards and decorative surfaces

-   Use large pastel cards with generous padding and a clear title.
-   If a card includes artwork, place it inside a lighter translucent
    inset panel near the top and keep its original colours unchanged.
-   Decorative oversized circles may sit near the lower corner of a
    card; use a related colour with slightly different brightness and
    clip it to the card.
-   A short underline or small accent mark can sit below a card title.
-   Keep card text and controls aligned consistently across a grid.
-   Make the whole card interactive when it represents a single action.
-   Use subtle pressed states, such as a small brightness change,
    without changing the visual identity of the card.

## 7. Inputs and search fields

-   White surface on a near-white page background.
-   Large rounded corners, subtle border/shadow, and generous horizontal
    padding.
-   Leading icon aligned vertically with the input text.
-   Placeholder text uses `color.text.muted`; entered text uses
    `color.text.primary`.
-   Use an accent blue for the search icon where it matches the
    reference style.
-   Provide a visible clear action when a field contains text.
-   Maintain a minimum touch target of 44--48 px and ensure text remains
    legible at increased accessibility sizes.

## 8. Buttons and icon controls

-   Icon-only actions should use a rounded square or circular surface
    with adequate spacing.
-   On pale surfaces, use dark navy-charcoal icons.
-   Hero-area utility controls may use translucent white fills.
-   Keep icon sizes and stroke weights consistent across the interface.
-   Selected actions may use the warm orange accent.
-   Destructive actions use the danger red token and white text.
-   Disabled controls must be visibly muted and non-interactive; do not
    communicate disabled state through colour alone.
-   Every icon-only button should have an accessible label.

## 9. Floating bottom navigation

-   White, pill-shaped outer container with a soft shadow.
-   Three equal-width navigation items as a reusable pattern.
-   Each item places its icon above its label and centers both
    horizontally.
-   Use thin, pale vertical separators between items.
-   Selected item: pale warm-orange capsule (`#FFE2C4` approximate) with
    orange icon and label (`#F6A04A`).
-   Unselected items: muted slate (`#626B7D`) on the white container.
-   Inset the selected capsule evenly within the outer container.
-   Keep the navigation pinned to the bottom while scrolling, but
    respect the device/browser safe area.
-   Add enough page-bottom padding so content remains reachable behind
    the floating navigation.
-   Always indicate selection through more than one visual cue, such as
    background plus icon/label colour.

## 10. Hero/header surfaces

-   Use a pastel multi-stop gradient with a smooth transition.
-   Keep primary text dark for readability.
-   Align a brand/image area and utility controls near the top, then
    place the main heading and supporting line below.
-   Add optional translucent circles or abstract shapes for depth; keep
    them low contrast and clipped within the header.
-   Use large rounded lower corners and avoid heavy borders.
-   The header should adapt to content height instead of clipping on
    small screens or with larger text settings.

## 11. Modal and confirmation dialog

-   Dim the page behind the dialog with a neutral dark scrim at
    approximately 30--40% opacity.
-   Use a centered white dialog with a large radius and soft shadow.
-   Stack the icon, title, supporting text, and actions with generous
    vertical spacing.
-   An icon may sit inside a pale tinted circular holder.
-   Place two actions side-by-side when there is enough width: a quiet
    neutral action and a clear primary/destructive action.
-   Use a pale grey fill and dark text for the quiet action.
-   Use `#D92F32` with white text for a destructive confirmation.
-   Suggested width: `82–88%` of the viewport, with a maximum width
    around `560–600 px`.
-   Ensure the dialog fits shorter screens; allow internal scrolling if
    needed.
-   Keep keyboard/accessibility focus inside the dialog while open and
    return focus to the triggering control when it closes.

## 12. Grouped settings or form panels

-   Use white rounded panels with a thin pale border.
-   Place a section icon and heading above each panel.
-   Inside each panel, stack rows with a title, a supporting
    description, and a right-aligned control or status icon.
-   Use dark text for titles, medium grey for descriptions, and muted
    grey for disabled rows.
-   Give rows enough vertical padding for wrapped descriptions.
-   Align controls vertically with the row content.
-   Use thin separators only when needed; spacing can provide separation
    without adding many lines.
-   On mobile, allow row text to wrap while preserving a usable control
    area.

## 13. Iconography and supplied artwork

-   Use one consistent icon family for interface icons.
-   Keep icons simple, clear, and visually balanced.
-   Do not replace interface icons with emoji.
-   Do not recolour supplied logos, illustrations, or other full-colour
    artwork.
-   Avoid applying a global tint, opacity, or filter to assets unless
    that effect is part of the reference.
-   Use appropriate `object-fit` / image-fit rules to avoid stretching
    artwork.
-   Treat artwork colours as part of the asset itself, not as app-wide
    design tokens.

## 14. Responsive behaviour and accessibility

-   Build using responsive CSS, `rem`/`em`, flexible grids, and
    viewport-aware constraints instead of copying screenshot pixel
    dimensions literally.
-   Maintain two columns where cards remain comfortable to read;
    collapse to one column only when the available width requires it.
-   Keep dialog widths capped on large displays.
-   Respect status bars, browser safe areas, and bottom gesture areas.
-   Support text zoom and long labels without clipping.
-   Provide visible focus states for keyboard navigation.
-   Aim for at least 44--48 px interactive targets.
-   Check text/background contrast, especially on saturated pastel
    cards.
-   Do not use colour as the only indicator of selection, success,
    error, or disabled state.
-   Verify both short and tall screens and test scrolling behind fixed
    elements.

## 15. Suggested CSS custom properties

``` css
:root {
  --app-background: #F9FAFC;
  --surface-primary: #FFFFFF;
  --surface-warm: #FEFBF6;

  --text-primary: #171B2B;
  --text-secondary: #626B7D;
  --text-muted: #A5A7AA;

  --border-default: #E4E5EA;

  --accent-orange: #F6A04A;
  --accent-blue: #3767D8;
  --accent-teal: #64C5CC;

  --status-success: #5EAD69;
  --status-danger: #D92F32;

  --card-blue: #BDD3FC;
  --card-indigo: #5F6FE0;
  --card-mint: #C4EBF0;
  --card-sky: #CEE7FD;

  --radius-card: 30px;
  --radius-input: 30px;
  --radius-panel: 28px;
  --radius-dialog: 40px;
  --radius-pill: 999px;

  --shadow-soft: 0 12px 32px rgb(36 48 68 / 10%);

  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-5: 20px;
  --space-6: 24px;
  --space-7: 28px;
  --space-8: 32px;
  --space-10: 40px;
  --space-12: 48px;
}
```

## 16. Final visual QA checklist

-   [ ] Main page background is a very light cool neutral.
-   [ ] Main surfaces are white or warm ivory, with thin low-contrast
    borders.
-   [ ] Headings use dark navy-charcoal and supporting text uses muted
    slate.
-   [ ] Pastel cards have large rounded corners and consistent spacing.
-   [ ] Gradients are soft and restricted to selected hero surfaces.
-   [ ] Supplied logo and illustration colours remain unchanged.
-   [ ] Inputs have rounded edges, generous padding, and readable
    placeholders.
-   [ ] Floating navigation uses a white pill, soft shadow, separators,
    and a warm selected state.
-   [ ] Dialogs have a dimmed background, white rounded surface, and
    clear action hierarchy.
-   [ ] Disabled and status states are visually distinguishable and
    accessible.
-   [ ] Layout adapts without clipping on different screen sizes.
-   [ ] Scrollable content is not hidden behind fixed navigation or
    system UI.

------------------------------------------------------------------------

**Reference limitation:** This is a reusable reconstruction of the
visible design language, not the original app's source design file.
Solid colours are close estimates; exact font, gradient stops, opacity,
shadows, and dimensions may differ from the original implementation.

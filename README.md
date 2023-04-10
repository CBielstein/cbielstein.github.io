# cbielstein.github.io

A personal website for Cameron Bielstein.

Currently hosted at [bielstein.dev](https://bielstein.dev).

Built with [Hugo](https://gohugo.io/), based on the the [xaviablaza/hugo-lodi-theme](https://github.com/xaviablaza/hugo-lodi-theme) theme, and hosted using [GitHub Pages](https://pages.github.com/).

## Adding new icons

To create, size, and color a new icon for links used on this site, use the following steps:

1. Find a source for an SVG of the image you want (ensure it's appropriately licensed for reuse)
1. Open a new document in [Inkscape](https://inkscape.org/)
1. Resize to 17 px tall:
    1. Select all elements by dragging a box around the full window
    1. Object (Menu) > Transform > Scale
    1. Height: 17pt, ✔ scale proportionally
    1. Edit (Menu) > Resize Page To Selection
    1. Save
1. Mask to appropriate color. This can either be done in Inkscape or directly on the resulting SVG XML content. Color should be `#505050`. If there are white bits (letters, etc.) in the image, careful not to mask them as well.
1. Open with VS Code and copy the XML
1. Put in places where needed (e.g. `hero.html`, `footer.html`, etc.)
1. Set height and width, remove additional unnecessary bits (inkscape saves a lot of metadata we don't need here)

## Analytics Reporting

Visitor analytics reporting is handled by [Plausible.io](https://plausible.io).
A script is added during deployment to report analytics data to them.
When forking this repository, please remove or update [deploy/plausible.html](deploy/plausible.html).

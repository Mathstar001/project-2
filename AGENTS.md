# Repository Guidelines

## Project Structure

This repository is a small, framework-free storefront for Khadijah Wears. The root contains the two pages, `index.html` (home and featured shop) and `collections.html` (collection browsing), with shared behavior in `script.js` and shared presentation in `styles.css`. There are no separate source, asset, or test directories; product and editorial images are currently referenced from remote Unsplash URLs.

## Build, Test, and Development

There is no build step or package manager configuration. Serve the repository root locally to test page navigation and browser behavior:

- `python -m http.server 8000` starts a local static server; open `http://localhost:8000`.
- `npx serve .` is an alternative when Node.js is available.

Stop the server with Ctrl+C. Open `collections.html` directly as well as through the home page to verify both entry points.

## Coding Style

Keep the existing plain HTML, CSS, and JavaScript approach; do not introduce a framework or build tooling without a clear need. Match the current formatting: two-space indentation in HTML and JavaScript, readable semantic markup, and CSS declarations grouped by component with responsive rules near the end of `styles.css`. Use descriptive camelCase for JavaScript identifiers, kebab-case for CSS classes and IDs, and meaningful alt text for content images. Keep shared storefront behavior and styling in the existing shared files.

## Testing Guidelines

No automated test framework or coverage target is configured. After a change, manually check relevant flows in a browser at desktop and narrow/mobile widths. For UI changes, verify both pages, category/search/sort interactions, cart and dialogs when affected, and that links and images behave as expected. Check the browser console for errors.

## Commits and Pull Requests

The Git history uses short, plain subject lines (for example, `collection`); no stricter convention is established. Keep each commit focused and describe its user-visible change. A pull request should summarize the change, list manual checks performed, link a related issue when applicable, and include before/after screenshots for visual updates.

## Configuration and External Assets

The site currently depends on Google Fonts and remote Unsplash images. Keep external URLs intentional and provide useful fallbacks or alt text; avoid adding secrets or credentials to this static repository.

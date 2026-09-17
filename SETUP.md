# Setup

1. Extract the ZIP on your computer.
2. Open or create your public GitHub profile repository. Its repository name must match your GitHub username. The owner of the supplied portfolio repository is `MuhammadWaleedMalik`, so the matching profile repository name is `MuhammadWaleedMalik`.
3. Upload `README.md` and the entire `assets` directory to the root of that repository. Do not upload only the ZIP or only the README. Preserve the filenames and directory structure.
4. Commit the files. Open your profile to view the README.

No package installation, API keys, GitHub Actions, image-generation endpoints or scheduled jobs are required for these animations. All SVG assets are included.

Open `PREVIEW.html` locally after extracting the archive to preview the desktop and mobile layouts. It is a local preview, not an exact reproduction of GitHub's rendering and image-proxy behaviour.

## Files

```text
README.md
assets/
  profile.svg
  profile-mobile.svg
  profile-static.svg
  profile-mobile-static.svg
  button-portfolio.svg
  button-github.svg
  button-email.svg
```

`SETUP.md`, `LINK-NOTES.md` and `PREVIEW.html` are reference files. Uploading them is optional.

## GitHub background limitation

GitHub sanitizes inline styles, scripts and CSS classes in rendered README HTML. A README cannot force GitHub's surrounding page background to black. The main SVG artwork has a solid `#000000` background in both GitHub light and dark themes; GitHub controls the margins, gaps and page chrome outside the images.

The CSS animations are contained in external SVG files referenced using ordinary image elements, not in README HTML. They do not use JavaScript, foreignObject or external fonts. Browsers or viewer settings can suppress animations; the full static content remains available. The picture element selects separate, genuinely static SVG files when the browser reports a reduced-motion preference. The animated SVGs also contain a reduced-motion CSS fallback. Contact buttons are static, and wrap naturally on narrow screens.

## Editing the design

Open the SVG files in any text editor. Search for the text you want to change and update BOTH `profile.svg` and `profile-mobile.svg`. Keep the visible wording consistent with the text version in `README.md`.

Palette:
- Black: `#000000`
- Antique gold: `#c8b48a`
- Warm ivory: `#eee8dd`
- Muted text: `#aaa59a`

The typefaces use the visitor's system serif, sans-serif and monospace fonts. No font files are required or included.

## Sources

- GitHub profile README requirements: https://docs.github.com/en/account-and-profile/how-tos/profile-customization/managing-your-profile-readme
- GitHub relative images and picture support: https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax
- GitHub markup sanitization: https://github.com/github/markup
- Reduced-motion preference: https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/prefers-reduced-motion

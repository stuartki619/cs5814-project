# Project Proposal Website Template

A lightweight, responsive landing-page template for presenting an academic project proposal on GitHub Pages. It uses plain HTML and CSS, with no build tools or third-party dependencies.

## Customize the template

Open `index.html` and replace every square-bracketed placeholder. Searching for `[` is a quick way to find them all. The main placeholders cover:

- Project title, short name, subtitle, and focus
- Course, institution, and term
- Overview and proposal-description copy
- Team-member names, roles, initials, and email addresses
- Footer year and institutional details

The three team cards are examples. Duplicate or remove the complete `<article class="team-member">...</article>` blocks to match your team size.

The circular initials work without image files. To use a team photo instead, place the image in `assets/team/` and replace the relevant initials block with:

```html
<img class="avatar" src="assets/team/member-name.jpg" alt="Portrait of Team Member Name">
```

Use a square image for the best crop. The existing `.avatar` style will display it as a circle.

## Add the proposal

Create the `assets` folder if it does not exist, then place your finished PDF at:

```text
assets/project-proposal.pdf
```

Both proposal buttons already point to that relative path. Keeping the link relative ensures it also works when GitHub Pages publishes the repository beneath a project subpath.

## Preview locally

For a quick check, open `index.html` in a browser. To preview it through a local web server instead, run this command from the repository folder:

```sh
python3 -m http.server 8000
```

Then visit `http://localhost:8000`. Stop the server with `Ctrl+C`.

## Publish with GitHub Pages

1. Commit `index.html`, `styles.css`, and the `assets` folder to the repository's `main` branch.
2. On GitHub, open the repository and select **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the `main` branch and the `/ (root)` folder, then save.
5. Wait for GitHub to provide the published project URL on the same settings page.

Because the template uses relative URLs, no path changes should be required for a standard GitHub Pages project site.

## Final checklist

- Replace all square-bracketed placeholders.
- Update both sample email addresses and their `mailto:` values.
- Add `assets/project-proposal.pdf` and confirm both proposal links open it.
- Update the page `<title>` and description in the `<head>`.
- Remove any unused team cards.
- Check the page on a phone-sized screen before publishing.

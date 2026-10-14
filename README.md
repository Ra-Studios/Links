# RaStudios Links

[Open the profile page](https://ra-studios.github.io/Links/) · [Open the resource shelf](https://ra-studios.github.io/Links/downloads.html)

The Instagram link-in-bio page and free resource library for RaStudios, hosted on GitHub Pages.

## Add a new resource

Uploading a file by itself does **not** create a card. Add its information to `downloads.html` using the existing card template. The shared stylesheet automatically applies the same design, spacing, and phone layout to each card; you do not need to redesign it.

### 1. Upload the file

- **Google Drive:** Upload the PDF or other file, set its sharing to **Anyone with the link → Viewer**, and copy the file's share link. Only use this setting for a resource you intend to share publicly.
- **This repository:** Upload the file into a `resources` folder. For example, a file named `git-basics.pdf` will use `resources/git-basics.pdf` as its card link. Files committed to this public repository are publicly accessible.

### 2. Copy the card

1. Open [`downloads.html`](downloads.html) on GitHub and click the pencil icon to edit it.
2. Find `<!-- START RESOURCE: Docker -->`.
3. Copy the complete block from that line through `<!-- END RESOURCE: Docker -->`, including both comments.
4. Paste the copy at `<!-- ADD YOUR NEXT RESOURCE HERE -->`, **before** the closing `</section>` tag. Leave the original Docker block intact.

### 3. Change the copied card's content

For example, to add a Git guide:

| Field in the copied block | Change it to |
| --- | --- |
| `START RESOURCE: Docker` and `END RESOURCE: Docker` | `START RESOURCE: Git` and `END RESOURCE: Git` |
| `aria-labelledby="docker-title"` | `aria-labelledby="git-title"` |
| `id="docker-title"` | `id="git-title"` |
| `01` in `art-top` | `02` |
| `DOCKER` in `art-bottom` | `GIT` |
| `A practical beginning.` | Your short cover subtitle |
| `PDF GUIDE` | The correct file type, such as `PDF GUIDE`, `TEMPLATE`, or `ZIP FILE` |
| Heading and description | Your resource title and summary |
| `Beginner friendly` | The appropriate audience label |
| Google Drive address in `href` | Your new share link or `resources/git-basics.pdf` |
| Download button's `aria-label` | A description such as `Open the free Git PDF guide` |
| `Get the guide` | Your button text, such as `Get the template` |
| `Opens in Google Drive · No sign-up on this site` | An accurate note, such as `PDF file · Opens in your browser` |

Use a different title ID for each card, and keep `aria-labelledby` and the matching heading's `id` identical. Use `&amp;` for an ampersand in your title or description.

The cover illustration is already included. Keep `href="#box"` for the cube illustration, or change just that illustration to `href="#file"` for a document icon. You do not need to upload a new cover image.

### 4. Publish

Click **Commit changes** and commit to `main`. GitHub Pages rebuilds the website. Wait for the latest **pages build and deployment** run in the repository's **Actions** tab to finish, then refresh the resource page.

Cards appear in the order of their blocks in `downloads.html`. Each new card appears **below the previous card**, with matching spacing. Inside each card, the cover and description sit side by side on larger screens and stack on phones.

## Update the social links

Edit the three links inside `<nav class="social-links">` in `index.html`. Change only each link's `href` to the new profile URL.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Profile, studio links, and social destinations |
| `downloads.html` | Resource cards and their download links |
| `styles.css` | Shared design and responsive layouts |
| `brand-logo.webp` | Current brand artwork |

This is a static site with no build tools or account dashboard. You can preview it by opening `index.html` in a browser or serving this folder with a local static web server.

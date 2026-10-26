# Unknown Kumar Portfolio

Static site: no build step. Works on GitHub Pages (user site or project site) because every path is relative.

## Publish on GitHub Pages
1. Create a repository and upload **everything inside this folder** (including `.nojekyll`) to the repository root.
2. Repository **Settings > Pages**. Under Source choose **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
3. After a minute the site is live at `https://YOUR-USERNAME.github.io/REPO-NAME/`.

## Images and assets
Upload images to the repository **root, `assets/` or `images/`**. You never type a folder path: the site searches those places, and also tries `.jpg/.jpeg/.png/.webp` and upper-case spellings (GitHub Pages is case-sensitive, so `PHOTO.JPG` is not `photo.jpg`).
- **Profile character:** name the file `avatar.jpg` (or change the name in `avatar:[...]` in `js/data.js`).
- **Project thumbnails:** write only the file name in `js/data.js`, e.g. `thumb:"my-edit.jpg"`. You can list fallbacks: `thumb:["my-edit.jpg","IMG_1234.jpg"]`.
- The four phone-named files (`1000048804.jpg` etc.) already work if uploaded instead of the renamed ones.

## Add a project
In `js/data.js`, inside `projects:[ ... ]`, add:
```
{title:"My Edit",cat:"Vlog Editing",platform:"YouTube",desc:"Short description.",thumb:"my-edit.jpg",alt:"Describe the thumbnail",link:"https://youtu.be/..."}
```
`cat` must match a name in `categories`. `platform` is `"YouTube"` or `"Instagram Reel"`.
Filter buttons appear automatically for categories that have projects.

## Contact form
Paste a Formspree or Web3Forms URL into `formEndpoint` in `js/data.js`. Until then the form opens the visitor's email app.

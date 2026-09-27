# Editing your website

Everything on the site lives in this `content/` folder. Each page = one folder.

    content/
      site.md            menu (which pages, in what order), name, footer
      home/              content.md, photo.jpg, icons/
      education/         content.md
      research/          content.md, icons/
      publications/      content.md
      cv/                content.md, cv.pdf
      contact/           content.md, icons/, FORM-SETUP.md
      _templates/        ready-made page folders: gallery, list, text
      favicon.svg        browser tab icon
      share-preview.jpg  image shown when the link is shared

- **Text:** open the page's `content.md` and change the text after `key:`. Don't rename keys.
- **Add / remove items:** copy or delete a whole `## ...` block.
- **Photos / files / icons:** replace the file keeping the same name, or add a new file and update its name in `content.md`.
- **New page (gallery, news, …):** copy a folder from `_templates/`, then add one `## Section` block in `site.md`. Nothing else changes.
- **Contact form log:** see `contact/FORM-SETUP.md`.
- Lines between `<!--` and `-->` are notes and are ignored.

The site reads these files when it loads, so it must be served by a web host (GitHub Pages, Netlify, …). Double-clicking index.html won't load the content.

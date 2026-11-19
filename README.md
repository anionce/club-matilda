# Club Matilda

The website of a small book club: a reading map where each stop is one of the club's books, and a page per book with a summary, a cast of characters, a note on the author and discussion questions (hidden behind a spoiler toggle). The content is in Catalan.

**Stack:** a single static `index.html` with inline CSS and a few lines of vanilla JavaScript. No build step and no dependencies. Fonts come from Google Fonts.

## Structure

```
index.html            page markup, styles and the hash router
logo.png              club logo
favicon.png           favicon
apple-touch-icon.png  home screen icon
*.jpg                 book covers and author photos
```

Navigation uses the URL hash: `#mapa` shows the reading map and `#<book-id>` shows that book's page, so each book can be shared with a direct link.

## Running locally

Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

## Adding a book

1. Add the cover image next to `index.html`.
2. Turn the next locked stop in the `.route` list into a link to `#<book-id>` with the cover, title and author.
3. Add an `<article id="<book-id>" class="book-view" hidden>` with the book's sections, following the existing one.

## Deploying

It is deployed on Netlify as a static site, publishing the repository root.

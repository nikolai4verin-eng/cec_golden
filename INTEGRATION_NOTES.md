# ECE Golden Catalog Landing Integration Notes

## Pages

- `index.html` is the Spanish/root catalog page.
- `en/index.html` is the English catalog page.

Both pages are static HTML files. Product images are embedded in the HTML; shared files are in `assets/`.

## Shared assets

- `assets/flags/en.svg`
- `assets/flags/es.svg`
- `assets/size-guides/ece-golden-size-guide.pdf`
- `assets/hero/kids-horses-hero.jpg`

## Menu URLs

Menu links are controlled in the `navUrls` object inside each HTML file.

If the active WordPress/WPML site uses different English slugs, update only this object:

```js
const navUrls = {
  es: { ... },
  en: { ... }
};
```

## Language switching

The language buttons navigate between:

- Spanish: `./`
- English: `en/`

Inside `en/index.html`, the Spanish button points back to `../`.

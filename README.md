# sumadhwa-vijaya
Translation of the great kavya - Sumadhwa Vijaya by Sri Narayana Panditacharya

### Customizing the hugo-book theme
- Install hugo-book theme as instructed
- Get `noto-devanagari.ttf` variable font (downloaded from google fonts) and copy into `themes/hugo-book/static/fonts` folder
- Add the following to `themes/hugo-book/assets/_fonts.scss`
```
@font-face {
  font-family: 'noto-devanagari';
  font-weight: 100 900; /* Variable weight range */
  font-style: normal italic;
  font-display: fallback;
  src: url('fonts/noto-devanagari.ttf') format('truetype');
}

.shloka-num {
  font-family: 'noto-devanagari';
  font-weight: 500;
  font-stretch: 100%;
  font-size: 1.0rem;
  padding: 0;
  margin: 0 0;
  color: #41463D;
}

.saara-heading,
.shloka {
  font-family: 'noto-devanagari';
  font-weight: 500;
  font-stretch: 100%;
  font-size: 2.0rem;
  color: #403233;
}

.vyakhya, .anvaya, .artha, .vyakarna, .vyakarna th, .vyakarna td {
  font-family: 'noto-devanagari';
  font-weight: 400;
  font-stretch: 100%;
  font-size: 1.25rem;
}

k {
  font-weight: 600;
  font-stretch: 100%;
  font-size: 1.0rem;
  padding: 0.75rem 0rem 0.5rem 0rem; 
  --text-decoration: underline;
  opacity: 0.35;
  display: block;
}

.artha h {
  font-weight: 500;
  color: #CC4E00;
}
```
- Add these to _custom.scss of hugo-book theme
```
.book-menu {
  display: none;
}

.book-page {
  margin-left: 0;
}

.header-links {
  text-align: right;
  font-family: 'noto-devanagari';
  font-weight: 700;
  font-stretch: 90%;
  font-size: 0.9rem;
  margin: 1.0rem 2.0rem 1.0rem 1.0rem;
}

.header-links a {
  text-align: center;
}

p {
  padding: 0;
  padding-top: 0.25rem;
  padding-bottom: 0.25rem;
  margin: 0;
}
```
- Add the header part to `themes/hugo-book/layouts/partials/docs/inject/head.html`
```
<div class="header-links">
  <a href="{{ "/sumadhwa-vijaya/" | relURL }}">मुख्यपुटः</a>
</div>
```

### Hugo config
The hugo.toml file is as configured. It should remain the same even on a fresh theme install, or when another theme is installed

# relaxed-broken-assets

```bash
npm install
npm run pdf:working # should open PDF with rendered image
npm run pdf:bug # should open PDF with broken (not rendered) image
```

To fix `npm run pdf:bug`, path to image in `src/test.pug` should be changed from

```pug
h1 Image should be rendered below
img(src='assets/image.jpg')

style
  include:scss test.scss
```

to

```pug
h1 Image should be rendered below
img(src='./../src/assets/image.jpg')

style
  include:scss test.scss
```

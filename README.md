# Techathon website

This is the website for Techathon, using the [Bootstrap framework](https://getbootstrap.com/docs/5.3/getting-started/introduction/) and [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site). The site sticks as close to built-in Bootstrap classes and elements as possible, but some additional theme styles are set in `custom.css`.

**Making changes to the `main` branch of this repository will update the [live website](https://techathon.live).**

The header background image is served in WebP or JPEG format for lower data usage. Given a `background.png` image in the media directory and [imagemagick](https://formulae.brew.sh/formula/imagemagick) installed, the WebP and JPEG versions can be made like this:

```
magick background.png -strip -define webp:sns-strength=25 -define webp:filter-sharpness=6 -define webp:filter-strength=10 background.webp

magick background.png -strip -interlace Plane -gaussian-blur 0.05 -quality 85% background.jpg
```

The social card images are also optimized:

```
magick social-card.png -strip -resize 1280x720 -quality 90 social-card.png

magick social-card-date.png -strip -resize 1280x720 -quality 90 social-card-date.png
```
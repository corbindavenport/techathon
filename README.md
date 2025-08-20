# techathon
This is the website for Techathon: https://techathon.live

Optimized background images with ImageMagick:

```
magick background.png -define webp:sns-strength=25 -define webp:filter-sharpness=6 -define webp:filter-strength=10 background.webp
```
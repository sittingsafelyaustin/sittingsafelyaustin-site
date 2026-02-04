# Hero image upload & optimization instructions

You provided a hero image to use as the site hero. To use it responsively and efficiently, add these files to the repository under `assets/`:

Required filenames (ensure exact names):
- hero-1200.jpg  (1200px width)
- hero-800.jpg   (800px width)
- hero-1200.webp (1200px width, WebP)
- hero-800.webp  (800px width, WebP)

Recommended ImageMagick commands (replace `source.jpg` with your source file):
- Resize and generate JPEG:
  magick source.jpg -resize 1200x -strip -quality 78 assets/hero-1200.jpg
  magick source.jpg -resize 800x -strip -quality 78 assets/hero-800.jpg
- Generate WebP:
  magick assets/hero-1200.jpg -quality 80 assets/hero-1200.webp
  magick assets/hero-800.jpg -quality 80 assets/hero-800.webp

Tips:
- Aim for quality 60–80 for JPEGs and ~80 for WebP for a good balance.
- Center crop or select an appropriate focal area if you need a tighter aspect ratio.
- If you prefer I generate these from the source image you uploaded, I can do that and include the binaries — I will add them to the branch if you confirm.

# Hero image upload & optimization instructions

Required filenames (exact names):
- hero-1200.jpg  (1200px width)
- hero-800.jpg   (800px width)
- hero-1200.webp (1200px width, WebP)
- hero-800.webp  (800px width, WebP)

Recommended ImageMagick commands (replace SOURCE with your photo path):

# Create JPEG variants (1200px and 800px width)
magick SOURCE -resize 1200x -strip -quality 78 assets/hero-1200.jpg
magick SOURCE -resize 800x -strip -quality 78 assets/hero-800.jpg

# Create WebP variants from the JPEGs
magick assets/hero-1200.jpg -quality 80 assets/hero-1200.webp
magick assets/hero-800.jpg -quality 80 assets/hero-800.webp

Tips:
- On Windows Git Bash convert a path like C:\Users\Janeth\Downloads\file.jpg to /c/Users/Janeth/Downloads/file.jpg.
- If the filename or path has spaces, wrap it in quotes, e.g. SOURCE="/c/Users/Janeth/Downloads/Thinkery Event.JPG"
- Aim for JPEG quality 60–80 and WebP ~80 for a good balance of size and quality.
- If you want me to generate the optimized images, say "Generate images for me" and I will prepare downloads for you to add.

# Magick


## Combine images to gif with transparency
```bash
magick.exe convert -delay 0 -loop 1 -alpha set -dispose previous *.png output.gif
```
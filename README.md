# Gentoo ebuild

This builds urxvt-unicode with the patch from https://github.com/blueyed/rxvt-unicode/tree/display-wide-glyphs to display glyhps that are too wide instead of a square.

urxvt considers the font to be broken, e.g. if the glyph is wider than the number of cells that wcwidth(3) reports. This gets better with Unicode 9 (since e.g. more characters are assigned a width of 2), but it does not help with characters from the Private Use Area (e.g. Font Awesome).

More information :
https://github.com/blueyed/PKGBUILD-rxvt-unicode-wide

# Gentoo usage

Place directory in your local overlay and emerge `rxvt-unicode`  
If you don't already have `~amd64` for `rxvt-unicode` then you should put this in `package.accept_keywords` :  
`x11-terms/rxvt-unicode ~amd64`

In your `package.use` you have to enable `wide-glyphs` USE flag


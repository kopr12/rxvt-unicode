# Info

rxvt-unicode with patches for glyph support (Powerline fonts, Nerd Fonts) and truecolor support

# Gentoo usage

Copy `x11-terms/rxvt-unicode` directory in your local overlay and emerge `rxvt-unicode`  
You should have this line in `package.accept_keywords` :  
`x11-terms/rxvt-unicode ~amd64`

If you want glyph support `wide-glyphs` USE flag should be enabled

If you want truecolor support enable both `24-bit-color` and `256-color` USE flags

http://tex.stackexchange.com/questions/117543/animation-using-a-sequence-of-images-in-a-single-pdf-file

You can produce an animated.gif file via:

pdfcrop animation.pdf
and then use convert from ImageMagick to obtain a .gif file. So something like:

 convert -verbose -delay 100 -loop 0 -density 400 animation-crop.pdf animation.gif
2. Include .gif:

As per How to add a gif file to my LaTeX file? the .gif file can be included by including the movie15 package in the preamble:

\includemovie{1cm}{1cm}{animation.gif}

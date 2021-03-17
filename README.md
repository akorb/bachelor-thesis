### Prerequisites for compiling

Since I use the [minted](https://ctan.org/pkg/minted) package for Syntax highlighting, [Pygments](https://pygments.org/) needs to be installed:

`sudo python3 -m pip install Pygments`

### Getting precompiled PDF

The PDF file of the latest code is automatically generated and uploaded to: https://andreas-korb.de/downloads/my-bachelor-thesis.pdf

### Cool commands

Trims all images to its content but pads it with one pixel line on the top and bottom. The padding is needed, because sometimes the `\includegraphics` command is trimming a pixel line.

`mogrify -trim -gravity north -splice 0x1 -gravity south -splice 0x1 *.png`


Convert *.puml file (PlantUML) to a PDF file containing vectorized data.

`plantuml -tsvg myfile.puml && inkscape myfile.svg --export-type="pdf" myfile.pdf`


Rotate a PDF file containing vector data clockwise with 90°. The vector data stays vectorized instead of getting rasterized.

`pdfjam --angle 90 myfile.pdf`

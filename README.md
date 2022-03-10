# Filter
A program that applies filters to a BMP, as described below.

# Grayscale
One of the common filters is the grayscale filter when we take an image and want to convert it to black and white. If all red, green and blue values are set to 0x00(hexadecimal for 0) then the pixel will be black. And if all values are set to 0xff(hexadecimal for 255), then the pixel is white. As long as the red, green and blue values are equal, the result will be different shades of gray in the black and white spectrum, with higher values meaning lighter shades (closer to white) and lower values meaning darker shades (closer to white).

So, to convert a pixel to grayscale, we just need to make sure that the red, green and blue values have the same value. To make sure that each pixel in the new image still has the same overall brightness or darkness as the old image, we can take the average value of red, green and blue to determine which shade of gray to make for the new pixel.

make filter

./filter -g infile.bmp outfile.bmp

# Sepia
A "sepia" filter that gives images an old-fashioned look by making the whole image look a bit reddish brown.

make filter

./filter -s infile.bmp outfile.bmp

# Reflection
An image reflection is a filter in which the resulting image is what you would get by placing the original image in front of a mirror. So any pixels on the left side of the image should end up on the right, and vice versa.

make filter

./filter -r infile.bmp outfile.bmp

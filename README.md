# colorblindness-processing
This is a library to simulate and correct images for Processing Org

You can find the full source for the library [here](http://www.google.com)


## Importing the library
Start with importing the library to your code
```Java
import colorblindness.colorblindness;
import processing.glu.*;
import processing.glu.tessellator.*;
```

## Simulating/Correcting using color difference method (Daltonization)

The "colorblindness.simulate() takes 4 parameters
1) Type of colorblindness
2) Absolute address of input file
3) Absolute Address of output file
4) Simulate or Correct the image

```Java
colorblindness.simulate(int type, string inputAddress, string outputAddress, boolean correct);

//For example, the following line simulates the image at /Desktop/input.jpg 
//as per protanopia and stores the output at /Desktop/output.jpg

colorblindness.simulate(1,"/Desktop/input.jpg","/Desktop/output.jpg",false);
```
Options for type - 
1 -> Protanopia
2 -> Deutranopia
3 -> Tritanopia

## Correcting the image using RGB Color Contrast method

There are two possible function calls for this

```Java
colorblindness.rgbContrast(string inputFile, string outputFile, float factor);
//The factor range from 0 to 1

colorblindness.rgbContrast(string inputFile, string outputFile);
```
When no factor is defined, the library uses predetermined optimum factor of 0.28


### Three more methods to be added soon

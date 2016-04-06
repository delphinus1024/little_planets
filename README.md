# little_planets

Creates so called "little planets" photo from given image.

## Description

little_planets is command line tool that Creates so called "little planets" photo from given image.
This program is hugely inpired by Matlab code of following site.

http://www.semifluid.com/2014/04/20/equirectangular-to-stereographic-projections-little-planets-in-matlab/

Before

<img src="" style="width: 600px;"/>

After ( ./little_planets.exe -W=2.4 ./original.jpg result.jpg)

<img src="" style="width: 600px;"/>

## Features

- Creates "little planets" photo.
- Image flip, camera distance and rotation can be specified with command option.

## Requirement

- OpenCV 3.0.0 or above is preferable.
- C++11 feature.
- Checked with win7 32bit&64bit + msys2 + gcc

## Usage

$ ./little_planets.exe [params] image result

        -?, -h, --help, --usage (value:true)
                show help
        -D, --dist (value:8)
                camera distance
        -F, --flip (value:0)
                flip horizontally
        -S, --show
                should show result
        -W, -w (value:2.4)
                world rotation

        image (value:./original.jpg)
                input image file
        result (value:result.jpg)
                output image file

camera distance: controls size of center region. Larger camera distance gives smaller center region.

flip: Without this option, the bottom side of the input image comes to the center of the output image. This option flips it horizontally.

world rotaion: rotates the origin of theta of polar coordinates. If this value is 2.4, discontinuity comes to the bottom of the result image.

	
## Installation

1. Modify Makefile according to your OpenCV inludes and libs environment.
2. make

## Author

delphinus1024

## License

[MIT](https://raw.githubusercontent.com/delphinus1024/little_planets/master/LICENSE.txt)


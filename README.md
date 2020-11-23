# DESCRIPTION

Point your laptop web cam at a piece of paper
and the program will stretch the writable area
over the whole screen.

![](demo.gif)

# DOWNLOAD

Below are links to download the operating system specific executables
from [release](https://github.com/kacpertopol/one_cam_board/releases/tag/0.1).
These files contain all dependencies bundled into one file using [pyinstaller](https://www.pyinstaller.org/).
This release is experimental, use at your own risk :-) If you decide to try I would be very happy to read your feedback!

## Linux

[DOWNLOAD](https://github.com/kacpertopol/one_cam_board/releases/download/0.1/camBoard)

## Windows

[DOWNLOAD](https://github.com/kacpertopol/one_cam_board/releases/download/0.1/camBoard.exe)

# USAGE

## Prepare paper

Print [**a4.pdf**](https://github.com/kacpertopol/one_cam_board/releases/download/0.1/a4.pdf) or [**a4.svg**](https://github.com/kacpertopol/one_cam_board/releases/download/0.1/a4.svg)
on A4 paper. The small circle marks
the top left part of the page.
If the aspect ratio of your web cam is different
from 16:9 or you want to use paper with a different size
see [setting up page with markers](#custom-page)

## Setup web cam 

- run *Zoom*, *Skype*, *MS Teams*, ... (**IMPORTANT**: to use *camBoard* with these programms
  disable the camera in them first - 
  otherwise a "camera busy" error will be thrown)
- share screen in *Zoom*, *Skype*, *MS Teams*, ...
- run *camBoard* on the screen that is being shared, the application will go full screen
- tilt your web cam so that all 4 ARUCO markers are in it's field of view

## Key bindings

- "q" - quit
- "k" - turn sharpening kernel on/off
- "i" - turn color inversion on/off
- "s" - save screen to PNG files to create slide show
  - the names are chosen automatically **0001.png**, **0002.png**, ...
  - by default the files are saved in the current working directory

## Custom page

You can make your own marker page with the markers
from **to_print/symbols**. They should be placed
in corners of a rectangle that matches the
aspect ratio of your web cam. Careful: the
orientation of the symbols is important and
they might require rotation - see **a4.svg**
for reference.

## Conserve printer ink / toner

- tape one printout with the 4 markers to desk surface (make sure the circle is positioned correctly and use tape that can later be removed from the desk 
  surface without damaging it)
- once the script recognizes the 4 ARUCO markers and stretches them to the whole screen 
  place a blank sheet of paper over the taped printout
- if the camera moves, remove any paper covering the printout and the program will recalculate
  how to warp the camera image
  
## Better resolution at the bottom

- laptop stands that allow tilting might help position the camera more perpendicular to the printout with markers resulting in better resolution
  at the bottom of the printable area
- manipulating the position of the laptop might damage it, be careful :-)

# MISCELLANEOUS 

- ArUco markers made using [this](https://chev.me/arucogen/)
- This is a simple script bodged togather from various opencv tutorials, [here](https://docs.opencv.org/master/d9/df8/tutorial_root.html) is a good place to start
- Sharpening kernel see [wiki](https://en.wikipedia.org/wiki/Kernel_(image_processing)) and [this](https://www.codingame.com/playgrounds/2524/basic-image-manipulation/filtering)
- Executables bundled with dependencies using [pyinstaller](https://www.pyinstaller.org/)

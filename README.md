# ColorScope [![Travis CI](https://travis-ci.org/michalkielan/ColorScope.svg?branch=master)](https://travis-ci.org/michalkielan/ColorScope) [![Build status](https://ci.appveyor.com/api/projects/status/92q4lasei6qnrlkk/branch/master?svg=true)](https://ci.appveyor.com/project/michalkielan/colorscope/branch/master) [![Coverage Status](http://coveralls.io/repos/github/michalkielan/ColorScope/badge.svg?branch=master)](https://coveralls.io/github/michalkielan/ColorScope?branch=master)


![Logo](res/logo.png)

Tool for analyze the image quality

## Requirements
* python-opencv
* matplotlib

```
$ sudo pip install opencv-python matplotlib
```

## Usage
Output format supported: `rgb`, `yuv`, `hsv`, `hls`

```
$ ./colorscope.py -i image.jpeg -out_fmt=rgb
R      G      B
23     24     232
255    255    255
...
```

Raw input images
```
$ ./colorscope.py -i image.yuv -pix_fmt=nv21 -s 640x480 -out_fmt=rgb
```

Measure and plot data
```
$ ./colorscope.py -i reference.jpeg -out_fmt=hls -o ref.json
$ ./colorscope.py -i capture.jpeg -out_fmt=hls -o cap.json
$ ./colorscope.py -gen ref.json cap.json
```

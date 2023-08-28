---
redirect_from: /_posts/2023-08-28-How to compile OpenCV with Gstreamer [Ubuntu&Windows].md/
title:  How to compile OpenCV with Gstreamer [Ubuntu&Windows]
tags:  
  - Gstreamer
---

# How to compile OpenCV with Gstreamer [Ubuntu&Windows]

## ##WINDOWS

### My setup

```
Windows 10 1903
python 3.7.0
OpenCV 4.1.0
Gstreamer 1.16.4
Cmake 3.14.5
Visual Studio 2019
```

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_tVfMGGTADXzIP_YPlcaNEQ.4eolp8f94ku0.webp)

## 1. Uninstall old opencv-python

```
pip uninstall opencv-python
```

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_xsF1YaF52vUJ5uBL_p_4zg.5yyawdom15w0.webp)

## 2. Install numpy

```
pip install numpy
```

## 3. Download gstreamer and opencv

◾ Install **both** gstreamer-runtime and gstreamer-development package in the same location

\>> https://gstreamer.freedesktop.org/download/

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_0imPwh9RbmrO4xbHfuYVSQ.filpg2xmfrs.webp)

​													Install both runtime and development package!

◾ Download opencv release sources (.zip file) and extract.
\>> https://github.com/opencv/opencv/archive/4.1.0.zip

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_NlG0zVt5y5BZcR3n99Q9fg.2bct052oubrw.webp)

## 4. Set Path Variable

◾ Add gstreamer to Path variable

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_iWn1XktT9U5UT2NqzFuGdA.6nhtj2m69gc0.webp)

◾ Add system variable “GSTREAMER_DIR” “C:\gstreamer\1.0\x86_64”

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_2nOzcr19lNxtYFCZn01_QA.5yl0d48u79g0.webp)

## 5. CmakeGUI

◾ install CmakeGUI 3.14.5
CmakeGUI >> https://cmake.org/download/

Visual Studio 2019(Community version is fine)
\>> https://visualstudio.microsoft.com/downloads/

◾ Open CmakeGUI.
◾ Select opencv source and build folder.

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1__KyykDayHWfsfhUk609Vkw.6tiu22u6e7c0.webp)

◾ Click “Configure” the new window will show up then select your Visual Studio version then click Finish.

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_uSKSIS1IAr87rjBWMn4YNA.3z5bs4ne26m0.webp)

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_0s9JTknFMw8HqcZoISzIuQ.6fphr9680is0.webp)

◾ Click Configure again, the red value will change to white.

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_t4NXRqqzxZzEwljoTXxpJA.7egdofhgg400.webp)

◾ Click Generate

◾ Click “Open Project” to open visual studio 2019

## 6. Visual Studio

◾ in Visual Studio:
switch from DEBUG to RELEASE and x64

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_i0MWwkVK4sM4n48phaHEuw.2ebcdggcyu3o.webp)

◾ Right click on INSTALL and select Build

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_4SzMM8DGgUPwWF_O3QJyag.4mvlmuf1cxs0.webp)

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_FNPjOaV9EAOKHqYIxwXdYQ.7flqgcujrbg0.webp)

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_kqeg9jemG2jtPQzwaNEPLQ.nyraq6dswxc.webp)

◾ Finally, add bin & lib folder to your env PATH , (from C:\opencv-4.1.0\build\install\x64\vc16)

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_UbncaWkwTPo-Dw0G_6_76Q.4co1955xhmc0.webp)

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_EeGo_77M5MLD8OWKT1fedw.4tq949jtmpe0.webp)

## 7. Final check

◾ Identify the location of a cv2 module

```
import cv2
print(cv2.__file__)"
```

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_UTGwftBV74A13l3fpCSNHw.3v1q0bbol3s.webp)

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_FOoepjdXwDaSVtRG7tg74g.50uum8a0fzk0.webp)

◾ Check build information

```
print(cv2.getBuildInformation())
```

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_vEEVcDTw8Zw-vDjvfcy5bA.3y6ki11camc0.webp)

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_VcM6AkHtnuQKTLyNfRGxuA.1jp8i0bc6rpc.webp)

```
import cv2
cap = cv2.VideoCapture('autovideosrc ! videoconvert ! appsink')
while True:
    ret,frame = cap.read()
    cv2.imshow('',frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cv2.destroyAllWindows()
cap.release()
```

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_TOU1DVFOtpkXTrePrZpzXA.1intigexbtj4.webp)

# for python 3.8+

later versions of python don’t load .dll from PATH due to new policy.
you need to add gstreamer DLL dir to config.py.



> D:\Python_3.8\Lib\site-packages\cv2\config.py

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/1_qlAduUjtwbU3SQeYNUYa0A.6wcna59fyb80.webp)





## 转载：[How to compile OpenCV with Gstreamer [Ubuntu&Windows\] | by Galaktyk 01 | Medium](https://galaktyk.medium.com/how-to-build-opencv-with-gstreamer-b11668fa09c)
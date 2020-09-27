# Facial_Detection

OpenCV is the most popular library for computer vision. Originally written in C/C++, it now provides bindings for Python.

OpenCV uses machine learning algorithms to search for faces within a picture. Because faces are so complicated, there isn’t one simple test that will tell you if it found a face or not. Instead, there are thousands of small patterns and features that must be matched. The algorithms break the task of identifying the face into thousands of smaller, bite-sized tasks, each of which is easy to solve. 

# Installing OpenCV

1. If you have previous/other manually installed (= not installed via pip) version of OpenCV installed (e.g. cv2 module in the root of Python's site-packages), remove it before installation to avoid conflicts.

2. Make sure that your pip version is up-to-date (19.3 is the minimum supported version): pip install --upgrade pip. Check version with pip -V. For example Linux distributions ship usually with very old pip versions which cause a lot of unexpected problems especially with the manylinux format.

3. Select the correct package for your environment:

     Do not install multiple different packages in the same environment.There is no plugin architecture: all the packages use the same namespace (cv2). If you installed              multiple different packages in the same environment, uninstall them all with      
     
       pip uninstall and reinstall only one package.

  a. Packages for standard desktop environments (Windows, macOS, almost any GNU/Linux distribution)

    Option 1 - Main modules package: pip install opencv-python
    Option 2 - Full package (contains both main modules and contrib/extra modules): pip install opencv-contrib-python 

4. Import the package:

    import cv2

    All packages contain haarcascade files. cv2.data.haarcascades can be used as a shortcut to the data folder. For example:

    cv2.CascadeClassifier(cv2.data.haarcascades + "haarcascade_frontalface_default.xml")


# TL;DR to get set with OpenCV on Mac M1
- Install homebrew with info from https://brew.sh/
- Install Cmake with homebrew: `brew install cmake`
- Clone opencv under Open_CV and build (not included here as the build was done for Mac M1) 
    - git clone https://github.com/opencv/opencv.git
    - mkdir build
    - cmake ../opencv/ .
    - Set Cmake flags with `arch -arm64 flag to enable arm64 instructions`
    - Run Cmake `arch -arm64 cmake ../opencv/ -DWITH_QT=OFF -DWITH_OPENGL=OFF -DFORCE_VTK=OFF -DWITH_TBB=OFF -DWITH_GDAL=OFF -DWITH_XINE=OFF -DBUILD_EXAMPLES=OFF -DBUILD_ZLIB=OFF -DBUILD_TESTS=OFF .`
    - Build opencv library using X (use 4 here) cpu cores under the build directory by `arch -arm64 sudo make -j 4`
- Install opencv/C++ by running the following command from the build directory `arch -arm64 sudo make install`

# OpenCV 
Main doc page https://docs.opencv.org/4.x/d9/df8/tutorial_root.html
Introduction to OpenCV - build and install OpenCV on your computer https://docs.opencv.org/4.x/df/d65/tutorial_table_of_content_introduction.html

# Credit
See https://github.com/kylehounslow/opencv-tuts for the original code with Windows OS
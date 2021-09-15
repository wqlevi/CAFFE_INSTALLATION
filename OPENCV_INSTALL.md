### Download pre-requisites
~~~bash
apt install cmake
~~~
### Downloading source
~~~bash
git clone https://github.com/opencv/opencv.git
git -C opencv checkout master
~~~
### Build
~~~bash
# outside opencv source dir:
mkdir build && cd build

# assuming the source dir called 'opencv', and configure & generate it
cmake -DCMAKE_INSTALL_PREFIX=/PATH/YOU/WANT/TO/INSTALL\
      -DOPENCV_EXTRA_MODULES=/PATH/YOUR/OPENCV_CONTRIB/module\
      ../opencv
# make them
make -j8
~~~

_now binaries should be built into referred directories_
### Environment
This part is optional as per usage, but take notice to `set(Opencv_DIR /dir/contains/OpencvConfig.cmake)` thus `find_package(Opencv_DIR found)` won't report error.

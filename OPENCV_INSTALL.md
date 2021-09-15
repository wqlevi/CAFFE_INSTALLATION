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

# assuming the source dir called 'opencv'
cmake -D -DCMAKE_INSTALL_PREFIX=/PATH/YOU/WANT/TO/INSTALL ../opencv
make -j8
~~~

_now binaries should be built into referred directories_

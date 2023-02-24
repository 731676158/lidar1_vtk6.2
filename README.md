VTK6.0 for PCL1.7 in lidar1 project

build and install:
```
mkdir build
cd build
cmake .. -DBUILD_TESTING=OFF
sudo make -j8
sudo make install
```

if error occures at:
```
CMake Error at CMake/GenerateExportHeader.cmake:177 (if):
  if given arguments:
    "cc (Ubuntu 7.5.0-3ubuntu1~18.04) 7.5.0
    ...balabala
```
find files that are told, modify
```
string(REGEX MATCH "[345]\\.[0-9]\\.[0-9]*
```
into
```
string(REGEX MATCH "[3456789]\\.[0-9]\\.[0-9]*
```

# cmake-integration

Minimal example using slsDetectorPackage from cmake

### First compile and install the slsDetectorPackage

```bash
#Clone the slsDetectorPackage and switch tho the correct branch
git clone https://github.com/slsdetectorgroup/slsDetectorPackage.git
git branch xxxxx

#Create a build directory and configure the project
mkdir build && cd build
cmake ../slsDetectorPackage -DCMAKE_INSTALL_PREFIX=/where/to/install
make -j12

#Make sure you set CMAKE_INSTALL_PREFIX in the last step unless you want to install to the system location
make install
```

### Now we can build this example

```bash
git clone https://github.com/slsdetectorgroup/cmake-integration.git

mkdir build && cd build
cmake ../cmake-integration -DCMAKE_PREFIX_PATH=/path/where/you/installed
make

# If you configured a virtual (or real) Jungfrau detector the example should give a similar output

./example
Detector type is: [Jungfrau]
Hostname: [localhost]
The value of vb_comp is 1220 for all modules
```
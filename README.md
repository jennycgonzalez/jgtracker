#Jgtracker

Real time object tracking system in videos. Employs a particle filter to estimate the centroid location and keypoint tracking and matching to estimate scale and rotation.

## Install Dependencies

```bash
sudo apt-get install build-essential
sudo apt-get install libtcmalloc-minimal4 libboost-system-dev libboost-filesystem-dev libboost-iostreams-dev
sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev

```

## Download and Install OpenCV with Extra Modules

```bash
git clone https://github.com/Itseez/opencv_contrib.git
wget https://github.com/Itseez/opencv/archive/3.1.0.zip
unzip 3.1.0.zip
cd opencv-3.1.0
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=RELEASE -DOPENCV_EXTRA_MODULES_PATH=../../opencv_contrib/modules -DWITH_IPP=OFF -DCMAKE_INSTALL_PREFIX=/usr/local ..
make -j4
sudo make install
sudo ldconfig
```

## Compile and Run

```bash
qmake
make
./jgtracker track path-to-video delay-in-seconds


### Install h264 library

Open a terminal window on the raspberrypi (or via SSH connection) and type in the following commands:
Download h264 library: 
```
git clone --depth 1 http://git.videolan.org/git/x264.git
```
Change directory to the x264 folder: 
```
cd x264
```
Configure installation: 
```
./configure --host=arm-unknown-linux-gnueabi --enable-static --disable-opencl
```
Create the installation: 
```
make -j4
```
Install h264 library on your system: 
```
sudo make install
```

### Install ffmpeg with h264

Change to home directory: 
```
cd ~
```
Download ffmpeg: 
```
git clone git://source.ffmpeg.org/ffmpeg --depth=1
```
Change to ffmpeg directory: 
```
cd ffmpeg
```
Configure installation: 
```
./configure --arch=armel --target-os=linux --enable-gpl --enable-libx264 --enable-nonfree
```
Make the installation: 
```
make -j4  
```
Now finally run the installation: 
```
sudo make install
```

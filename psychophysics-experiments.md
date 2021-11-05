% Title: Installing a Linux workstation with psychtoolbox, psychopy, expyriment
% Author: christophe@pallier.org
% Date: 05 Nov 2021


Software tools to generate psychophics experiments:


* expyriment (python scripting)
* psychopy (gui or python scripting)
* psychtoolbox (octave/matlab)


# Installation instructions for Ubuntu 20.04 LTS focal


## install basic packages

```
sudo apt update
sudo apt upgrade -y
sudo apt-get install linux-lowlatency
sudo apt install vim emacs git subversion mc tmux openssh-server htop
sudo apt install build-essential
sudo apt install octave
sudo apt install libportaudio2 libportmidi-dev
sudo apt install  libsdl-2* 
```

## Expyriment

### Download and install Anaconda Python
```
wget https://repo.anaconda.com/archive/Anaconda3-2021.05-Linux-x86_64.sh
chmod +x Anaconda3-2021.05-Linux-x86_64.sh
./Anaconda3-2021.05-Linux-x86_64.sh 
conda update -n base -c defaults conda
```
### Expyriment environment
```
conda create -n expyriment python=3.8
conda activate expyriment
conda install ipython numpy pyopengl
pip install mediadecoder
pip install sounddevice
pip install pygame
mkdir git
cd git
git clone https://github.com/expyriment/expyriment.git
cd expyriment/
python setup.py install
```

### Checking expyriment
```
conda activate epxyriment
cd $HOME/git
git clone https://github.com/chrplr/PCBS.git
cd PCBS/experiments/expyriment/parity
python parity.py
```


## Psychopy
```
sudo apt-get install libusb-1.0-0-dev portaudio19-dev libasound2-dev
sudo add-apt-repository 'deb http://archive.ubuntu.com/ubuntu bionic main universe'
sudo apt install -t bionic libwebkitgtk-1.0-0
wget https://raw.githubusercontent.com/psychopy/psychopy/master/conda/psychopy-env.yml
conda env create -n psychopy -f psychopy-env.yml
conda activate psychopy
conda install ipython numpy
```
## Test 
```
psychopy
```

## Psychtoolbox

### Add [Neurodebian](https://neuro.debian.net/)  repository for your ubuntu distribution

```
wget -O- http://neuro.debian.net/lists/focal.de-m.full | sudo tee /etc/apt/sources.list.d/neurodebian.sources.list
sudo apt-key adv --recv-keys --keyserver hkps://keyserver.ubuntu.com 0xA5D32F012649A5A9
```
### activate sources
``` 
sudo sed -Ei 's/^# deb-src /deb-src /' /etc/apt/sources.list
sudo apt update

sudo apt build-dep octave-psychtoolbox-3
sudo apt install libdc1394-22-dev libfreenect* libgstreamer1.0-dev libgstreamer-plugins-*

wget https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/master/Psychtoolbox/DownloadPsychtoolbox.m.zip
unzip DownloadPsychtoolbox.m.zip 

mkdir $HOME/PTB3

octave
DownloadPsychtoolbox('/home/neurostim/PTB3')
PsychLinuxConfiguration()

# test 
DrawingSpeedTest()
``` 

# Compiling_Python_from_Source_Reference
## This is nothing special, just a short guide for reference
<br><br>
This has commands you can copy and paste when you want to compile Python from source.
I use this as a reference when I have a freshly installed GNU/Linux Operating System, because you need certain packages when compiling

## Instructions
### This was made while Compiling Python3.8 from source
### Should work for newer versions

### Required for building
sudo apt install zlib1g-dev libffi-dev libreadline-gplv2-dev libreadline5 libssl-dev

### Optional Dependences
sudo apt install libbz2-dev libncursesw5-dev libgdbm-dev liblzma-dev libsqlite3-dev tk-dev uuid-dev libreadline-dev

### get source, this is 3.9 alpha
git clone https://github.com/python/cpython.git
cd cpython
./configure
make
### make altinstall is to prevent from over-writing previous python versions
### For example, my Debian has Python3.7
### make altinstall will let me install python3.11, without over-writing python3.7
make altinstall

# Notebook Instance Setup Tutorial
How to setup the GCP instance notebook with python3.6

The GCP notebook instance is currently running Debian GNU/Linux 9.11 (stretch) and comes with Python 2.7 and Python 3.5. The following instruction will help you install Python 3.6 and its kernel so you can change between python versions in your notebook.

1. Update repositories and packages

```sudo apt-get upgrade```

2. Install the following dependencies:

```sudo apt-get install -y do build-essential libssl-dev zlib1g-dev```

```sudo apt-get install -y libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm```

```sudo apt-get install -y libncurses5-dev libncursesw5-dev xz-utils tk-dev```

```sudo apt install build-essential checkinstall```

```sudo apt install libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev```

```sudo apt-get install liblzma-dev```

3. Install Python 3.6:

Download from the official website :

```wget https://www.python.org/ftp/python/3.6.4/Python-3.6.4.tgz```

Extract compressed file:

```tar xvf Python-3.6.4.tgz```

Change into python3.6.4 directory :

```cd Python-3.6.4```

Configure, make and install :

```./configure --enable-optimizations```
```sudo make-j8```
```sudo make altinstall```

4. Jupyter Kernel

Check which kernels are currently installed:

```jupyter kernelspec list```

Upgrade pip3.6 to the latest version and install ipykernel:

```sudo pip3.6 install --upgrade pip```
```sudo pip3.6 install ipykernel```

Let --name equal the name you want for your kernel

```sudo python3.6 -m ipykernel install --user --name=Python3.6```

Running jupyter kernelspec list should display your new kernel.



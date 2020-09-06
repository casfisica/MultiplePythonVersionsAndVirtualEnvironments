# Multiple Python Versions and Virtual Environments

<par>
In order to install Python 3.7 in your Ubuntu 18.04 system, you need to follow a different procedure— You need to install from the source.
In your terminal, run the following command to update your system and upgrade your existing packages:
</par>

```bash
sudo apt-get update  
sudo apt-get upgrade -y
```
<par>
Install the build tools and Python 3.7 dependencies using the following command:
</par>

```bash
sudo apt-get install build-essential libssl-dev zlib1g-dev libncurses5-dev libncursesw5-dev libreadline-dev libsqlite3-dev libgdbm-dev libdb5.3-dev libbz2-dev libexpat1-dev liblzma-dev tk-dev libffi-dev
```
<par>
Download the source code of Python 3.7 using the wget tool, decompress the tar file and inside your decompressed Python-3.7.0 folder
</apr>

```bash
wget https://www.python.org/ftp/python/3.7.0/Python-3.7.0.tar.xz
tar xf Python-3.7.0.tar.xz
cd Python-3.7.0
```
<par>
Build the Python 3.7 code using the configure and make tools
</par>
 
```bash
./configure --enable-optimizations
sudo make -j 8
```

<par>
To install the Python 3.7, run the following command:
</par>

```bash
sudo make altinstall
```
<par>
Now Python 3.7 can be run using:
</par>

```bash
python3.7
```

## Virtual Env
<par>
To install a virtual enviroment run
</par>

```bash
python3 -m venv tutorial-env
```
By default it will setup the current python version in the system. In order to use a different version (like the 3.7 installed before), Just use the --python (or short -p) option when creating your virtualenv instance to specify the Python executable you want to use, e.g.:

```bash
virtualenv --python=/usr/bin/python3.7 <path/to/new/virtualenv/>
```

__Note:__ For Python 3.3 or later, refer to README_pyenv.md.

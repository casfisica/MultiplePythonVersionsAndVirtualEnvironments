# Multiple Python Versions and Virtual Environments

<par>
In order to install an old Python  in your Debian based system, you need to follow a different procedure— You need to install from the source.
In your terminal, run the following command to update your system and upgrade your existing packages:
</par>

```bash
sudo apt-get update && sudo apt-get upgrade -y
```
<par>
Install the build tools and Python 3.7.9 dependencies using the following command:
</par>

```bash
sudo apt-get install build-essential libssl-dev zlib1g-dev libncurses5-dev libncursesw5-dev libreadline-dev libsqlite3-dev libgdbm-dev libdb5.3-dev libbz2-dev libexpat1-dev liblzma-dev tk-dev libffi-dev
```
<par>
Download the source code of Python 3.X using the wget tool, decompress the tar file and inside your decompressed Python-3.X folder
</apr>

```bash
PYTHON_VERSION=3.7.9
BASEDIRECTORY=$(pwd)
PYTHON_URL=https://www.python.org/ftp/python/${PYTHON_VERSION}/Python-${PYTHON_VERSION}.tar.xz
wget $PYTHON_URL
tar xf Python-${PYTHON_VERSION}.tar.xz
mkdir -p ${BASEDIRECTORY}/Python-${PYTHON_VERSION}-build
cd ${BASEDIRECTORY}/Python-${PYTHON_VERSION}

```
<par>
Build the Python 3.X code using the configure and make tools
</par>
 
```bash
#--prefix=/path/where/you/want/python/installed
./configure --enable-optimizations --prefix=${BASEDIRECTORY}/Python-${PYTHON_VERSION}-build --cache-file=${BASEDIRECTORY}/Python-${PYTHON_VERSION}/cache-file
make -j 8
```

<par>
To install the Python 3.X, run the following command:
</par>

```bash
make altinstall
# If you don't use the --prefix, it will try to install on the user/bin, then you should use altinstall in order to evade compatibility isues
#sudo make altinstall
```
</par>
Add the Old Python directory to the PATH if you need
</par>

```bash
#export PATH=$PATH:${BASEDIRECTORY}/Python-${PYTHON_VERSION}-build
#If 
```

<par>
Now Python 3.X can be run using:
</par>

```bash
$PATH:${BASEDIRECTORY}/Python-${PYTHON_VERSION}-build/python${PYTHON_VERSION}
```

## Virtual Env
<par>
To install a virtual enviroment run
</par>

```bash
#python3 -m venv tutorial-env
```
By default it will setup the current python version in the system. In order to use a different version (like the 3.7 installed before), Just use the --python (or short -p) option when creating your virtualenv instance to specify the Python executable you want to use, e.g.:

```bash
$PATH:${BASEDIRECTORY}/Python-${PYTHON_VERSION}-build/python${PYTHON_VERSION} -m venv Name-env
```

__Note:__ For Python 3.3 or later, refer to README_pyenv.md.

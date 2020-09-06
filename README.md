# Multiple Python Versions and Virtual Environments using pyenv

<par>
Install all the dependencies to pyenv [The installation wiki](https://github.com/pyenv/pyenv/wiki/Common-build-problems)
<par/>

```bash
sudo apt-get install -y build-essential libssl-dev zlib1g-dev libbz2-dev \
libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
xz-utils tk-dev libffi-dev liblzma-dev python3-openssl git libedit-dev
```

<par>
 Clone the pyenv installer from the GitHub page to your system [pyenv-installer](https://github.com/pyenv/pyenv-installer)
</par>  

```bash
git clone git@github.com:pyenv/pyenv-installer.git
cd pyenv-installer
```
## Installation

Install:
```bash
$ curl https://pyenv.run | bash
```
pyenv.run redirects to the install script in this repository and the invocation above is equivalent to:

```bash
curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash
```
Restart your shell so the path changes take effect:

```bash
$ exec $SHELL

```
You can now begin using pyenv.

### Update

```bash
pyenv update
```

### Uninstallation
<par>
For uninstallation go to 
</par>

```'bash

```

# Multiple Python Versions and Virtual Environments using pyenv

<par>
Install all the dependencies to pyenv [The installation wiki](https://github.com/pyenv/pyenv/wiki/Common-build-problems)
<par/>

```bash
sudo apt-get install -y build-essential libssl-dev zlib1g-dev libbz2-dev \
libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
xz-utils tk-dev libffi-dev liblzma-dev python3-openssl git libedit-dev
```

## Installation

Install:
```bash
$ curl https://pyenv.run | bash
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

### Install Python versions into $(pyenv root)/versions. 
<par>
  For example, to download and install Python 2.7.8, run:
</par>
```bash
pyenv install 2.7.8
```

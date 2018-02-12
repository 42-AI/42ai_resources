# How to...

Here you will find tutorials to set up your environment and various useful things to do AI on school Macs.

## Environment setting

### Install Python and dependencies

The school's Macs already have python. A `python` command starts python 2.7 and `python3` starts python 3.4.4.

We suggest you work with a more recent version of python. For that we will use Anaconda3 which is a package with python and multiple scientific libraries including: Numpy, Scikit, Jupyter, etc.

For reasons of space on your `dump`, we will install [Anaconda3](https://www.anaconda.com/download/#macos) on `goinfre` (`/Users/login/goinfre`, or directly on the Mac's disk).

> Be careful at each step to properly replace `login` with your own login.

Okay, follow these commands to setup everything:

```bash
cd ~/goinfre
curl -o anaconda3.sh https://repo.continuum.io/archive/Anaconda3-5.0.1-MacOSX-x86_64.sh
sh anaconda3.sh
```

Follow the instructions. __Warning!__ When it asks you to specify the location put:

```
/Users/login/goinfre/anaconda3
```

It takes few minutes to install everything. Once it is done, the install asks you to add Anaconda3 install location to PATH in your `.bash_profile`: hit _return_.

If you are not using Bash, add this line manually to your `.zshrc` (for example):

```
export PATH="/Users/login/goinfre/anaconda3/bin:$PATH"
```

Then reload the shell:

```bash
source ~/.zshrc
```

Now Python is installed on your Mac. Each time you change Macs you will have to repeat the operation to reinstall it if it is not installed. To check which python is bound on the `python` command, just do:

```bash
which python
```

And if the answer is:

```
/Users/login/goinfre/anaconda3/bin/python
```

You guys are good!

### Install Pytorch

Once you installed Python using Anaconda3, installing Pytorch is easy, just enter:

```bash
conda install pytorch torchvision -c soumith
```

#### Known issues

If this error appears when you launch a program using Pytorch:

```
[...]
ImportError: numpy.core.multiarray failed to import
```

Do:

```bash
pip install -U numpy
```

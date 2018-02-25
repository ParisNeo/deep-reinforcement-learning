# RL tools installation
This tutorial explains how to install the tools we will be using on this git
## Installation of gym environment
### Non windows
instructions are found here:
https://github.com/openai/gym
### Windows
On windows things are a little bit different from osx and linux
assuming you have installed anaconda 3 or higher.
Open a terminal using your environment and then type the following:
conda install git
conda install -c conda-forge ffmpeg
# Note: For video recording.
conda update --all
conda clean -a
pip install git+https://github.com/Kojoley/atari-py.git
pip install gym[all]
# Get all things done!

If you have a different codepage on your PC, then the pip installation would probably not work.
The solution would be to manually modify the pip code.
run a new cmd.exe console
type
chcp
it will show the system default code, for example 936.
open Lib/site-package/pip/compat/__init__.py
around 75 line, change return s.decode('utf_8') to return s.decode('cp936')

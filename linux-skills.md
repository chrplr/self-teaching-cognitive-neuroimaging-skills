Linux skills
============







## Learn to how to use a Terminal

1. You must learn how to launch programs from a command line and navigate file systems. See  http://linuxcommand.org/lc3_learning_the_shell.php

2. You must learn how to use `ssh` to connect to a remote computer. See https://www.howtogeek.com/311287/how-to-connect-to-an-ssh-server-from-windows-macos-or-linux/

3. You must learn `tmux` which allows you to keep a terminals always open on a remote station, even when you close the local Terminal and switch off your local computer. This is extremely useful to monitor long processes.  
 
    - https://github.com/tmux/tmux/wiki/Getting-Started
    - Brian P. Hogan. tmux2 Productive mouse-free development. The pragmatic programmer



## Learn a coding/text editor

1. learn touch typing: https://www.typingclub.com/
2. learn he text editor Vim

    * Video: *Mastering the vim language*: <https://www.youtube.com/watch?v=wlR5gYd6um0&t=1901s>
    * Book: Drew Neil, *Practical Vim: Edit Text at the speed of thought*

3. gui-based text editor: sublime text, microsoft visual code, atom, ...



## Learn Python

Resources:
- Automate the Boring Stuff with Python  https://automatetheboringstuff.com/


## Learn to write clean code and use version control

- https://software-carpentry.org/lessons/
- https://openclassrooms.com/en/courses/5671626-manage-your-code-project-with-git-github


## Learn Python Scientific libraries 

- numpy et al. : https://scipy-lectures.org/
- Pandas https://realpython.com/learning-paths/pandas-data-science/
- Wes McKinney (2017) Python for Data Analysis: Data Wrangling with Pandas, NumPy, and IPython. O'Reilly

The computing environment at Neurospin is based on a network of linux workstations linked to a centralized file server providing the file systems `/neurospin` and  `/i2bm`).

To use it efficiently, you must understand how it is organized and acquire several skills

## Connecting to a linux workstation

### Within neurospin:

- Log directly onto a linux workstation using your cea login and password

or

- log to Windows and then:
    - use putty and ssh to connect to a distant linux workstation (you must know its name on the network, e.g. isXXXXXX)
    - use x2go client to open a graphical session on a distant linux workstation (the x2go server must be up and running on the workstation)

### Outside of Neurospin:

- Use the VPN (Virtual Private Network). You need a "Mobipass", a little device that generates a onetime password.
- Then connect to a neurospin computer using ssh or x2go.


## conecting to the computing cluster

alambic *TODO*

## GPU

kraken  *TODO*




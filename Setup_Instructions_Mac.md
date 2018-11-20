# Mac

If you already have Python3 and pip installed, you can jump straight to the `Python Libraries` section on Page 2. If you are unsure of the state of your environment, run the following commands to see how much setup you need to do.

1. Open Terminal - you can do this by searching `Terminal` in Spotlight Search (Cmd+Space).

## GCC

1. Run: `gcc`
2. If you see `error: no input files`, GCC is installed. Go to the next section.
3. If instead you see `command not found`, you will need to install GCC - there are multiple ways to do this, depending on your OSX version (this might require an Internet search). One possibility, if you have an Apple account, is to download the Command Line Tools [here](https://idmsa.apple.com/IDMSWebAuth/login?appIdKey=891bd3417a7776362562d2197f89480a8547b108fd934911bcbea0110d07f757&path=%2Fdownload%2Fmore%2F&rv=1).

## Homebrew

1. Run: `brew -v`
2. If you see `Homebrew x.x.x`, Homebrew is installed. Go to the next section!
3. If you don't see this, you will need to install Homebrew. To do this, go to [https://brew.sh/](https://brew.sh/).
4. Copy the first line under `Install Homebrew`. Paste it into Terminal, and hit Enter.
5. Enter your password when prompted and wait for Homebrew to finish installing. 
6. If you now see `Homebrew x.x.x` when you run `brew -v`, go to the next section! 
7. If you don't see this, you might need to add Homebrew to PATH.  Run `touch ~/.bash_profile; open ~/.bash_profile`
9.  A text editor should pop up.
10.  Copy the following line to bottom of the file in the text editor: `export PATH=/usr/local/bin:/usr/local/sbin:$PATH`
11.  Close and re-open Terminal.

## Python 3

1. We will be using Python 3 in the workshop. To check which version of Python is installed on your machine, run: `python3 --version`, or `python --version`. If you see `Python 3.x.x`, Python 3 is installed. Go to the next section! If you see `Python 2.x.x`, you will need to install Python 3.
2. To install Python 3, run `brew install python`. Brew installs Python 3 when this command is run.
3.  Run `python3 --version`. You should see something like `Python 3.x.x`.

## Pip

1. Run: `pip3 --version`, or `pip --version`
2. If you see `pip xx.x from … (python 3.x)`, pip is installed. Go to the next section!
3. If you don't see this, please reinstall Python 3 (using the instructions in the above section). Pip is automatically installed with newer versions of Python 3.

## Python Libraries

We will be using several libraries during the workshop. To install them, you can use `pip` or `pip3`, depending on which command is linked to your Python 3 installation. 
To check, run `pip3 --version` or `pip --version`. The command that outputs `(python 3.x)` is the command linked to Python 3.

Create a file called `requirements.txt` and copy the following text to it:

```
pandas
numpy
cufflinks
cognite-sdk
plotly
cython
tslearn
jupyter
```

Then, navigate to the folder with this file on Terminal (if you are unfamiliar with navigating the Terminal, have a look at [these](http://mally.stanford.edu/~sr/computing/basic-unix.html) commands!), and run the following command, using either pip or pip3:

`cat requirements.txt | xargs pip3 install --upgrade --force-reinstall --user`

_The reason we need to run this command instead of `pip3 install -r requirements.txt -U --user`, the usual command, is because the dependencies must be installed in a specified order and updated to the latest versions._

Now, when you run `jupyter notebook` in Terminal a new page should open up on your Internet browser.

You're all set! We're excited to see you in a few weeks :)

_If you run into any setup issues that can’t be resolved, please consider arriving 10-15 minutes early for the workshop so we can help you get set up!_


# Ubuntu

The following instructions will be used to install Python 3, Jupyter Notebook, and several Python libraries.

1. Open Terminal.
2. Run `python --version`. If you do not see `python 3.x.x`, run  `python3 --version`. If you still do not see `python 3.x.x`, run `sudo apt install python3` 
3. Then, run `pip3 --version`. If pip is not installed, run  `sudo apt install python3-pip`
4. You will also need to install the IPython shell. To do this, run `sudo apt install ipython3`
5. Now you're ready to install Jupyter! Run `pip3 install jupyter`
6. Once you have installed Jupyter, you will need to add it to the execution path. To do this, open `~./bashrc` in your favourite text editor and add the following line to the bottom of the file: `export PATH=$PATH:~/.local/bin/`
7. To confirm that Jupyter Notebook was installed properly, close and re-open Terminal, then run `jupyter notebook`. If a new tab opens in your browser, you're all set! You can close this tab and continue on to install some other Python libraries.


## Python Libraries

We will be using several libraries during the workshop. 

Create a file called `requirements.txt` and copy the following text to it:

```
pandas
numpy
cufflinks
cognite-sdk
plotly
cython
```


Then, navigate to the folder with this file on Terminal, and run the following command:

`pip3 install -r requirements.txt -U`

Then, we will have to install one more library (this library has a dependency on `cython` which was installed above):

`pip3 install tslearn`

You're all set! We're excited to see you soon :)

_If you run into any setup issues that can’t be resolved, please consider arriving 10-15 minutes early for the workshop so we can help you get set up!_

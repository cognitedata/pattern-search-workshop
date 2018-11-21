# Windows

  

We will be using Jupyter Notebook with Python 3 for this workshop - if you already have these installed, you can skip to the `Python Libraries` section. If you are unsure of the state of your environment, follow the steps below to see how much setup you need to do.

  

## Python 3

We suggest installing Python 3 through Anaconda, because Anaconda comes packaged with Jupyter Notebook. The process to install and run Jupyter Notebook without Anaconda may cause problems that will require extensive troubleshooting.

## Anaconda

1.  Check if Anaconda is installed: search `Anaconda Prompt` in your search bar. If you see the following screenshot, then Anaconda is already installed on your machine - skip to **Step 3**. Otherwise, go to the next step.
    

![](https://lh3.googleusercontent.com/wnU3gOIvpdyvMfUVclTagQvan5J34JpBtedVkP1Ogt2PZ6SHwDqdkwqBqy6zOPBg7wL2evNRL5tzEHQ4v8DKGTjtS7g3x1MKEedrGiMw9KZ6Vs5fQtCoXtCbc-urIsEs5IPf3RWz)

  

2. If Anaconda Prompt does not show up, please download Anaconda for Python 3.7 from this link (use the recommended settings in the installer): [https://www.anaconda.com/download/#windows](https://www.anaconda.com/download/#windows)

![](https://lh6.googleusercontent.com/ZArXWRrWPBVu9eal-FeFRK2EtDAKgAIz_37voXQH56-KypeaXc13YGH1X59xYmRVItgUhGg4xvKZklBa9NUC_GENFo6Qt_DBfhYQKgH18fh1fSPi_juCjEAsnFJstX1Ut2GkzCTx)

3. After Anaconda is installed, open Anaconda Prompt by selecting it from your Start menu. Type `python --version` and hit Enter - if you see `Python 3.x.x` in the output, you’re good to move onto the next step! If instead you see `Python 2.x.x`, run `pip install python --upgrade`.



## Python Libraries
The following steps can be run directly in Anaconda Prompt.

1.  Upgrade pip, the Python package manager. `python -m pip install --upgrade pip`
2.  Type `notepad requirements.txt` and hit Enter. A Notepad window will pop up, asking you if you want to create a new file. Click ‘Yes’.
3.  Copy the following text to the new file:
```
pandas
numpy
plotly
cython
```
3. Save and close the file.
4. Run `pip install -r requirements.txt --upgrade` in Command/Anaconda Prompt.
5. After the last step is done, run `pip install cufflinks --upgrade`.
6. Then, run `pip install cognite-sdk`.
7. After the last step is done, run `pip install tslearn --upgrade`. If you run into the following error message (in white), go to the steps in `Troubleshooting`. Ignore that section if tslearn installs successfully.:

![](https://lh3.googleusercontent.com/Wm2WC6bki240ZhnUJ51kv4yukkU3z8HMg4PTw-knSKI6cnjFctdDKZGAFP18TqVP--rit6v3ieUSj7_usDOA4tcLx4jborLIaAF8GH-3s7u9vcIOEAfKoaeNPhwpku-1MT80sf5z)

You're all set! We're excited to see you soon :)

_If you run into any setup issues that can’t be resolved, please consider arriving 10-15 minutes early for the workshop so we can help you get set up!_

  


## Troubleshooting

### tslearn
When running`pip install tslearn`, you might run into the following error message: `error: Microsoft Visual C++ 14.0 is required. Get it with "Microsoft Visual C++ Build Tools": [https://visualstudio.microsoft.com/downloads/]`,

1.  If you see this, go to the following website: [https://visualstudio.microsoft.com/visual-cpp-build-tools/](https://visualstudio.microsoft.com/visual-cpp-build-tools/).
2. Click `Download Build Tools`
3. On the next screen, click download on `Build Tools for Visual Studio 2017`
4.  Run the executable file - on the following window, choose `Visual C++ build tools`.

![](https://lh5.googleusercontent.com/tM1rWFL1EbkBmJWip73eeE4YUkTKuqJk_5AzdDb3oAcetK9TjdiGuIuqbUeIL45NobvpCykjaqxjs3EQ5Bvyg2dtem_3pP8ALvvzFCGYwTPhUZY3lXTruDOZx_AwuQFSV70MyRqn)

4. Start the installation.
5. After installation is finished (takes a few minutes), run `pip install tslearn` in Command/Anaconda Prompt again - it should install successfully this time.

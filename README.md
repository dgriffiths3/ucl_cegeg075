# UCL Image Understanding Coursework Data

To download files open terminal and browse to the folder you want to store the data using the `cd` command.

Clone the repository by typing: 

`git clone https://github.com/dgriffiths3/ucl_cegeg075`

Next move into the folder and open jupyter notebook with: 

```
cd ucl_cegeg075
jupyter notebook
```

Finally, open the file `opencv_coursework.ipynb`. It is important you run `jupyter notebook` whilst in the `ucl_cege075` directory as otherwise the file paths will not work correctly.

### Coursework Task:

Your task is to use OpenCV and Numpy tools to extract a specific feature from a single (or group of) image(s). The feature(s) of choice as well as image(s) is up to you. It can be imagery acquired from satellite, aerial or terrestrial methods as well as your choice of spectral bands (i.e. R, G, B, NIR, SWIR etc.). You are encouraged to think outside-the-box and use internet resources such as tutorials to incorporate new methods not discussed within these practicals. 

You should assess the accuracies of your proposed solution, highlighting the strengths and weaknesses. The accuracy assessment should be undertaken both on images you designed the solution around, as well as new images your system has not seen before. You should comment on why you think the solution is performing the way it is.

**Delivery**

The coursework comprises two components. First, a 2000 word research report style write up (i.e. Introduction, Methodology, Results, Discussion, Conclusion), where the segmentation problem is presented as a research problem that is investigated through the methods outlined and solved in the analysis. The discussion should connect to the wider literature to consider the approaches used by others to solve similar problems.

Second, a file (preferrably .py / .ipynb) containing the source code for your solution. This should be properly annotated and commented. For advice on how to correctly format code for delivery take a look [here](https://www.python.org/dev/peps/pep-0008/). It is important to provide frequent in-line comments to explain what your code is doing. Finally, if you use functions, they should be properly commented showing their input and output arguments as well as a brief description of the function.

**Deadline**

Both documents should be uploaded to moodle by **28th March 2018**.


**Installation on your own machine**

***Mac***
The easiest way to install OpenCV on a mac is through a package manager. There are two popular package managers for mac `HomeBrew` and `MacPorts`. Here we will show you how to install the required dependencies using `HomeBrew`.

If you have never done any programming on your mac you may need to first install xcode from the app store:
The open terminal and type:
`sudo xcode-select --install`
`sudo xcodebuild -license`

To install HomeBrew open your terminal and enter:
`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

Add HomeBrew to your path (here I use nano but you can use which ever command line text editor you like):
`nano ~/.bash_profile`
Append this text to the end of your file and save:
`export PATH=/usr/local/bin:$PATH`
To refesh your profile type:
`source ~/.bash_profile`

Next install a local version of python:
`brew update`
`brew install python`

Then we will install `pip` a python specific package installer:
`curl -O http://python-distribute.org/distribute_setup.py`
`python distribute_setup.py`
`curl -O https://raw.github.com/pypa/pip/master/contrib/get-pip.py`
`python get-pip.py`

Once we have pip we can install the required dependencies:
`pip install jupyter numpy opencv-python matplotlib`

To be able to clone the content from `github` as described above type:
`brew install git`

***Windows***

To install with windows and to programme in general with python on a windows machine I would reccommend using [Anaconda](https://conda.io/docs/user-guide/install/windows.html). Follow the link and click the `Anaconda Installer for Windows` link. Then follow all the necessary steps.

Once Anaconda is installed you can open the `anaconda` prompt that will now be in your start menu. `pip` comes installed with Anaconda so you can go ahead and install the dependencies:

`pip install jupyter numpy opencv-python matplotlib`

Finally, to install git to allow us to clone the content:
`conda install git`






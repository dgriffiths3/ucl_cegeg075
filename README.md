# UCL Image Understanding Coursework Data

The repository is now tested using Python 3.5+ although should also be backwards compatible with Python 2.7+.

To download files open terminal and browse to the folder you want to store the data using the `cd` command.

Clone the repository by typing: 

`git clone https://github.com/dgriffiths3/ucl_cegeg075`

Next move into the folder and open jupyter notebook with: 

```
cd ucl_cegeg075
jupyter notebook
```

Finally, open the file `opencv_coursework.ipynb`. It is important you run `jupyter notebook` whilst in the `ucl_cege075` directory as otherwise the file paths will not work correctly.

### Running on Google Colab ###

This notebook can be run on google colab with a few minor alterations to avoid the need for setting up a local python environment. First navigate to [Google Colab](https://colab.research.google.com/). If you have not already, you will need to create a google account.

On the top bar navigate to `GITHUB` and enter the user `dgriffiths3`. Open the file `opencv_coursework.ipynb` under the `ucl_cege075` respository. 

Next, run the following code cell at the top of the notebook:

`!git clone https://github.com/dgriffiths3/ucl_cegeg075 data`

Open the files tab (small arrow below CO logo in top left) and click `refresh` if you do not see the folder `data`. These are all the files required for the practical.

To enable the new file structure to work, you will need to append the string `data/` infront of any file paths. For example, `file = 'images/newyork.jpg''` becomes `file = 'data/images/newyork.jpg'`. 

The rest of the practical will now work as normal.


### Task

Your task is to use OpenCV and Numpy tools to extract a specific feature(s) from a single (group of) image(s). The feature(s) of choice as well as image(s) is up to you. It can be imagery acquired from satellite, aerial or terrestrial methods as well as your choice of spectral bands (i.e. R, G, B, NIR, SWIR etc.). You are encouraged to think outside-the-box and use internet resources such as tutorials to incorporate new methods not discussed within these practicals. 

You should assess the accuracies of your proposed solution, highlighting the strengths and weaknesses. To achieve this you should design/incorporate some form of accuracy indicator. The accuracy assessment should be undertaken both on images you designed the solution around, as well as new images your system has not seen before. You should comment on why you think the solution is performing the way it is. A good start here would be to look at the Intersection Over Union (IOU) method. [Here](https://www.pyimagesearch.com/2016/11/07/intersection-over-union-iou-for-object-detection/) is a good write up of how you could incorporate this into your project. Remember how we generated the bounding box for the segmentation above. Any accuracy assessment is acceptable providing it is justified.

### Delivery

The coursework comprises two components. First, a 2000 word research report style write up (i.e. Introduction, Methodology, Results, Discussion, Conclusion), where the segmentation problem is presented as a research problem that is investigated through the methods outlined and solved in the analysis. The discussion should connect to the wider literature to consider the approaches used by others to solve similar problems.

As a general guideline the report could be structured (although not restricted to) as follows:

**1. Introduction**
   * What am I trying to detect? 
   * What application would this be useful for? 
   * What methods will I incorporate with the solution
   * What are the initial obstacles in my way


**2. Methodology**
   * What is my approach to solving the problem
   * Why have I chosen certain algorithms
   * Briefly, how do these algorithms work (you would not need to go to a mathematical level here)
   * How will you assess accuracy


**3. Results**
   * Display images of your results (the good and the bad)
   * Comment on what you see
   * Record accuracy assessment results and initial comments
    
    
**4. Discussion**
   * How do you feel your proposed solution performed
   * If it was good why?
   * If it was bad why?
   * How does this compare to other solutions are there?
   * What could be done to improve the solution?
    
    
**5. Conclusion**
   * Short conclusion outlining the key components of your report

Second, a file (preferrably .py / .ipynb) containing the source code for your solution. This should be properly annotated and commented. For advice on how to correctly format code for delivery take a look [here](https://www.python.org/dev/peps/pep-0008/). It is important to provide frequent in-line comments to explain what your code is doing. Finally, if you use functions, they should be properly commented showing their input and output arguments as well as a brief description of the function.

## Installing OpenCV on your own machine ##

Here we describe the easiest ways to get opencv and python working on your own machine. If you get stuck there is a wide range of resources available online.

***Mac***

The easiest way to install OpenCV on a mac is through a package manager. There are two popular package managers for mac `HomeBrew` and `MacPorts`. Here we will show you how to install the required dependencies using `HomeBrew`.

If you have never done any programming on your mac you may need to first install xcode from the app store:
The open terminal and type:

```
sudo xcode-select --install
sudo xcodebuild -license
```

To install HomeBrew open your terminal and enter:

`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

Add HomeBrew to your path (here I use nano but you can use which ever command line text editor you like):

`nano ~/.bash_profile`

Append this text to the end of your file and save:

`export PATH=/usr/local/bin:$PATH`

To refesh your profile type:

`source ~/.bash_profile`

Next install a local version of python:

```
brew update
brew install python
```

Then we will install `pip` a python specific package installer:

```
curl -O http://python-distribute.org/distribute_setup.py
python distribute_setup.py
curl -O https://raw.github.com/pypa/pip/master/contrib/get-pip.py
python get-pip.py
```

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

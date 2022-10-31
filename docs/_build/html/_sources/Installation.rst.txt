Installation
------------

Methods of Installation
#######################

AtlasXbrowser is both available to be downloaded and run as an executable file, with compatible files for MacOS and Windows.
The application is also able to be run from source code, using the open source repo.

Running Executable
##################

* To download the appropriate executable file, navigate to the releases page of the Github repo https://github.com/atlasxomics/AtlasXbrowser/releases.
* From there find the desired release version. We recommend using the latest release version.
* There exists AtlasXbrowser.tgz to be run on MacOS and AtlasXbrowser.exe to be run on Windows. Download the appropriate file.
* Once downloaded click on the file, or execute it from the command line and the application should launch.


Running from Source
###################

* Open a terminal window and navigate to the directory where you want to download AtlasXbrowser to.

* Run the following commands into the terminal:

.. code-block::

   git clone https://github.com/atlasxomics/AtlasXbrowser.git


Managing Dependencies
#####################

* AtlasXbrowser requires the usage of Python 3.7 as well as the installation of multiple outside packages. For these reasons we HIGHLY recommend the usage of a virtual environment, specifically Anaconda.


* If an Anaconda distribution is not currently installed on your system see the installation guide here, `Anaconda`_.


   * To check that anaconda was properly installed open a Terminal window and check the version installed by running:

      .. code-block::

         conda --version
   
   * Once conda is installed, ensure it is running the latest distribution by running:

   .. code-block::

      conda update conda

* With conda installed with an up to date version, create a python 3.7 environment with the command:

   .. code-block::

      conda create --name py37 python=3.7

   Where "py37" can be any name of the environment.

* Once created, navigate to the directory where AtlasXbrowser is cloned to and run:

   .. code-block::

      conda deactivate
      conda activate py37


* To check this conda environment is running the proper python version run:

   .. code-block::

      python --version

   This should return Python 3.7.xx. If this is not the case, deactivate the conda environment using "conda deactivate'. Repeat this command until there is no conda environment listed at the left side of the terminal and then reactivate the environment.

* To install all the necessary packages for AtlasXBrowser run the following commands in the activated conda environment.

   .. code-block::

      conda install -c conda-forge scipy
      conda install -c conda-forge seaborn
      conda install -c conda-forge tifffile
      conda install -c conda-forge jsbeautifier
      conda install -c conda-forge pandas
      conda install -c conda-forge pillow
      conda install -c conda-forge matplotlib
      conda install -c fastai opencv-python-headless
   

Running AtlasXbrowser
#####################

* To ensure the version on your machine is the latest update, run:

.. code-block::

   cd AtlasXbrowser
   git pull https://github.com/atlasxomics/AtlasXbrowser.git
   
* Once ready, run AtlasXbrowser with the following command:

.. code-block::

   python ABrowser.py
    

.. _Anaconda: https://docs.anaconda.com/anaconda/install/index.html

.. _AtlasXbrowser: https://github.com/atlasxomics/AtlasXbrowser.git







Installation
------------

To use AtlasXbrowser, please download the most recent release: https://github.com/atlasxomics/AtlasXbrowser/releases. Executable file (AtlasXbrowser.tgz) is available for Mac OSX. Follow steps below if you prefer to run AtlasXbrowser as a python application from source code.

Downloading
###########

* Open a terminal window and navigate to the directory where you want to download Atlas Browser to.

* Run the following commands into the terminal:

.. code-block::

   git clone https://github.com/atlasxomics/AtlasXbrowser.git


Managing Dependencies
#####################

* AtlasXbrowser requires the usage of Python 3.7 as well as the installation of multiple outside packages. For these reasons we HIGHLY reccomend the usage of a virtual enviroment, specifcally Anaconda.


* If an Anaconda distribution is not currently installed on your system see the installation guide here, `Anaconda`_.


   * To check that anaconda was properly installed open a Terminal window and check the version isntalled by running:

      .. code-block::

         conda --version
   
   * Once conda is installed, ensure it is running the latest distribution by running:

   .. code-block::

      conda update conda

* With conda installed with an up to date version, create a python 3.7 enviroment with the command:

   .. code-block::

      conda create --name py37 python=3.7

   Where "py37" can be any name of the enviroment.

* Once created, navigate to the directory where AtlasXbrowser is cloned to and run:

   .. code-block::

      conda deactivate
      conda activate py37


* To check this conda enviroment is running the proper python version run:

   .. code-block::

      python --version

   This should return Python 3.7.xx. If this is not the case, deactivate the conda enviroment using "conda deactivate'. Repeat this command until there is no conda enviorment listed at the left side of the terminal and then reactivate the enviroment.

* To install all the necessary packages for AtlasXBrowser run the following commands in the activated conda enviroment.

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







Installation
------------

Before running AtlasXbrowser, the software must be available to run on your local machine.
Luckily the codebase for AtlasXbrowser is open source and freely hosted on Github.

Downloading
###########

* Open a terminal window and navigate to the directory where you want to download Atlas Browser to.

* Run the following commands into the terminal:

.. code-block::

   git clone https://github.com/atlasxomics/AtlasXbrowser.git
   cd AtlasXbrowser
   git clone https://github.com/formazione/Azure-ttk-theme


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

      conda activate py37

   





.. code-block::

   pip install scipy
   pip install seaborn
   pip install tifffile
   pip install jsbeautifier
   pip install pandas
   pip install pillow
   pip install matplotlib
   pip install opencv-python

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






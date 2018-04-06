***********************************
Practical Data Analysis with Python
***********************************

:Author: Dr. Andreas Hilboll
:Email:  hilboll@uni-bremen.de
:Date:   Summer term 2018


Setting up a Python environment on your computer
================================================

There are several different Python *distributions*. I recommend to use
the Python 3 version of the `Anaconda Python Distribution
<https://www.anaconda.com/download/>`__. The installation is very well
`documented
<https://docs.anaconda.com/anaconda/install>`__. Additional help can
be found `here
<http://swcarpentry.github.io/python-novice-gapminder/setup/>`__.

Also, I recommend to use `conda environments
<https://conda.io/docs/user-guide/getting-started.html#managing-environments>`__
within Anaconda.

Usually, the installation of Anaconda Python is pretty
straightforward, but can sometimes be tricky depending on your
computer environment.

   If you run into problems with the installation, feel free to contact
   me and I'll try to help out!


Using the command line
----------------------

You can create a new environment from the *Anaconda Navigator*, or on
the command line with the command

.. code:: shell

   conda create --name pdap2018 python=3 anaconda

This will create a new environment called *pdap2018*, with the most
recent *Python3* release.  Also, a number of important packages for
scientific computing will be installed into that environment.

Next, you need to add the conda-forge_ channel to your Anaconda installation:

.. code:: shell

   conda config --append channels conda-forge

.. _conda-forge: https://anaconda.org/conda-forge

When working on the command line, you now want to change into your new
environment:

.. code:: shell

   conda activate pdap2018

You should now see ``(pdap2018)`` at the left of your command prompt.

Next, we need to install some additional libraries:

.. code:: shell

   conda install netcdf4 xarray basemap cartopy shapely

Now, we need to update one package:

.. code:: shell

   conda update pyzmq

Finally, you can now start the Jupyter interface with the command

.. code:: shell

   jupyter-lab


Using the Anaconda Navigator
----------------------------

The `Anaconda Navigator
<https://docs.anaconda.com/anaconda/navigator/>`__ is a desktop
graphical user interface to your Anaconda installation.

After installation of the Anaconda distrbibution, there should be an
entry *Anaconda Navigator* in your computer.  Click it to launch the
application.  You can follow the documentation at the Anaconda
Navigator website to perform the following tasks:

1. Create a new environment ``pdap2018`` based on *Python3*.
2. Add the ``conda-forge`` channel *to the bottom* of your channel
   list.
3. Install the following packages into the ``pdap2018`` environment:
   * anaconda
   * netcdf4
   * xarray
   * basemap
   * cartopy
   * shapely
   * ffmpeg
4. Update the package ``pyzmq``
5. Launch the ``jupyterlab`` app in that environment.


Verifying your installation
---------------------------

After you launched JupyterLab, open the file
``PDAP2018_Test_Python_Installation.ipynb`` (you first need to
download it from here_ to your computer).

.. _here: https://gitlab.com/iup-bremen/pdap-2018/raw/master/PDAP2018_Test_Python_Installation.ipynb

Then, from the *Run* menu, select *Run All Cells*.  If everything
works, you should see a total of five plots in the Notebook:

1. an empty canvas
2. an animation of a moving sine curve
3. a Mandelbrot image
4. a map of Australia
5. a map of the World, focused on Europe

If you see all these, your setup was successful.  Otherwise, please
contact me.

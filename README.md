[![Actions Status](https://github.com/ome/EMBL-EBI-imaging-course-05-2022/workflows/repo2docker/badge.svg)](https://github.com/ome/EMBL-EBI-imaging-course-05-2022/actions)

# EMBL-EBI-imaging-course-05-2022

This repository contains materials for the May 2022 virtual course [Microscopy data analysis: machine learning and the BioImage Archive]( https://www.ebi.ac.uk/training/events/microscopy-data-analysis-machine-learning-and-bioimage-archive-2022).

Day 3 *Distributed/Cloud computing practical* contains a collection of notebooks with code and text.

Day 4 *Image data resource practical* contains a collection of notebooks with code and text. It also contains the presentation
[Image Data Resource: Data Submission and Curation](Day_4/EMBL_EBI_Workshop.pdf)


## Running the notebooks

### Running on cloud resources

* Run [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ome/EMBL-EBI-imaging-course-05-2022/main)
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ome/EMBL-EBI-imaging-course-05-2022/)

### Running in Docker


Alternatively, if you have Docker installed, you can use the [repo2docker](https://repo2docker.readthedocs.io/en/latest/)
tool to run this repository as a local Docker instance:

    $ git clone git://github.com/ome/EMBL-EBI-imaging-course-05-2022
    $ cd EMBL-EBI-imaging-course-05-2022
    $ repo2docker .

Then follow the instructions that are printed after the Docker image is built.


### Running locally

Finally, if you would like to install the necessary requirements locally,
we suggest using conda:

Install Anaconda https://www.anaconda.com/products/individual#Downloads

Then, create the environment:

    $ git clone git://github.com/ome/EMBL-EBI-imaging-course-05-2022
    $ cd EMBL-EBI-imaging-course-05-2022
    $ conda env create -n imaging_course -f binder/environment.yml

and activate the newly created environment:

    $ conda activate imaging_course

The following steps are only required if you want to run the notebooks

* If you have Anaconda installed:
  * Start Jupyter from the Anaconda-navigator
  * Select the notebook you wish to run and select the ``Kernel>Change kernel>Python [conda env:imaging_course]``
* If Anaconda is not installed:
  * In the environment, install ``jupyter`` e.g. ``pip install jupyter``
  * Add the virtualenv as a jupyter kernel i.e. ``ipython kernel install --name "imaging_course" --user``
  * Open jupyter notebook i.e. ``jupyter notebook`` and select the ``imaging_course`` kernel or ``[conda env:imaging_course]`` according to what is available


An additional benefit of installing the requirements locally is that you
can then use the tools without needing to launch Jupyter itself.

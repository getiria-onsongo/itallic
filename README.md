# ITALLIC: A tool for automatically identifying and correcting errors in location based plant breeding data

One of the challenges of integrating plant breeding data to collectively analyze it with other sources of 
data such as genotype, environment, management, and socioeconomic data is errors in location data. Collectively, 
this data could be used to inform genetic predictive models for maize, wheat, and other crops. Typical errors in
plant breeding location data include flipped latitude and longitude values, missing negative signs, and, in some 
cases, missing data. This tool, an **I**ntegrated **T**ool for **A**utomatic **L**at **L**ong **I**mputation 
and **C**leaning (ITALLIC), automatically detects and corrects errors in location data and imputes missing values 
for location-dependent data, such as region name.    

This page contains instructions for installing and uaing ITALLIC. These instructions assume familiarity working on a [terminal](https://itconnect.uw.edu/learn/workshops/online-tutorials/web-publishing/what-is-a-terminal/). 

## Pre-Installation
ITALLIC is a [Python 3](https://www.python.org/downloads/) application. In addition to Python 3, we **highly recommend** also installing [Conda](https://docs.conda.io/en/latest/). Click [this link](https://docs.conda.io/projects/conda/en/latest/user-guide/install/) for more information on installing [Conda](https://docs.conda.io/en/latest/).

Even though you do not need Conda to use ITALLIC, using Conda has some advantages that will make life easier. It will not only make installation for ITALLIC and other Python packages easy, it also enables use of conda environments. Use of environments is a good way to prevent conflicts that might arise when working on different projects that require different versions of the same software package. [This blog](https://python-wrangler.com/how-and-why-you-should-use-conda-environments/) nicely summarizes some advantages of using environments.  


### Prepare working environment 

Create a conda environment for data cleaning and install ITALLIC in that environment. The command below uses "DataCleaning" as the environment name and Python 3.8 as the Python version to use. You can use a different name for your conda environment but we recommend sticking with Python 3.8. Any Python 3 version should work but since ITALLIC was tested on Python version 3.8, we recommend using the same Python version. 

* Create conda environment. 

```bash
$ conda create --name DataCleaning python=3.8 -y
```

* Activate the environment. 

```bash
$ conda activate DataCleaning
```

* Install Jupter Notebook. 
ITALLIC has a visualization tool that works well with [Jupyer Notebook](https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/what_is_jupyter.html). Use conda to install Jupter. 

```bash
$ conda install -c conda-forge jupyter -y
```

* Install dependencies needed to use jupyter. 

```bash
$ conda install -c conda-forge ipykernel -y
```

<!--
ITALLICs is written in pure Python, but has several dependecies such as GeoPandas that can be challenging to install. 
Therefore, we recommend installing ITALLIC using the "**Easy Install**". For those with experience using pip, we also 
provide instruction for installing using pip. 

#### Easy Install
The best and easiest way to install ITALLIC is using conda and conda-forge channel: 

```bash
$ conda install -c conda-forge itallic
```

If you do not have conda install, you can install it [here](https://docs.conda.io/projects/conda/en/latest/user-guide/install/). 

#### Pip Install
-->


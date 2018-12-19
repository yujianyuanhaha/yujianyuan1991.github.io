---
path: '/login'
title: 'Stochastic Nodes'

layout: nil
---


![Build](https://travis-ci.org/pemami4911/POMDPy.svg?branch=master) ![Python27](https://img.shields.io/badge/python-2.7-blue.svg) ![Tensorflow16](https://img.shields.io/badge/tensorflow-1.6-blue.svg)

README FILE  
Author: Jianyuan (Jet) Yu  
Affiliation: Wireless, ECE, Virginia Tech  
Email : *jianyuan@vt.edu*  
Date  : April, 2018 


# Configuration  🔧
We run codes on **Spyder** GUI under Anaconda(**version 2**), **tensorflow** is required as well as related tensorboard setup.  
For batch test, we run codes on ARC VT. 
* Python version 2.7, tensorflow version **1.6.0**. Notice tensorflow 1.5.0 is suggested on Linux OS else "keneral died, restart" error may appear. If the version would not fit, run command 
```
conda install -c conda-forge tensorflow=1.6.0
```  
Version would never be the big issue, since Anaconda support *virtual environment* easily without bothering current version setup.
e.g. setup Python 3.6    
1. python 3.5   
```
    conda create --name py3 python=3.5
```  
2. after py3 prompt show up, install any lib missing like numpy, tensorflow, matlibplot.  
``` 
    conda install numpy
    conda install tensorflow
    conda install matlibplot
```
Notice ipython does not support virtual environment as raw terminal; you can type `anaconda-navigator` after virtual environment is setup to launch the GUI, to apply feature like debugging in a virtual environment.


# Edit .gitignore to ignore non-programming file
This programmes automatically save down files, thus by default the Github would notice you about these non-programming file changes. Consider we only trace codes, a smart way is edit `.gitignore` file to rule out these files. e.g. in this case, edit  the .gitignore file (which is blanket by default) like 
``` shell
    *.pyc
``` 
to ignore local files ending with name `.pyc` and under any folder.  Refer to [bitbucks git ignore tutorial](https://www.atlassian.com/git/tutorials/saving-changes/gitignore) for more tricks.  
Notice if you have not edit `.gitignore` when init the repository, you need to remove all `.pyc` file by command `find . -name "*.pyc" -exec git rm -f "{}" \;`.

# How to run
Git Clone the codes by in terminal by `git clone https://github.com/yujianyuanhaha/DQN-DSA`, or in GUI app(Github or GitKraken). 


Parameter all configurable at header part of `multiNodeLearning.py` OR `setup.config` file. 
In terminal run below command for the import the default `setup.config` file. :  
```
python multiNodeLearning.py
```
 
OR
```
python multiNodeLearning.py --set setFileName.cfg
```
where `setupFileName` was file like `settingCaseXX` to save some significant progressive results.  
OR even further, if some modification is made on ```multiNodeLearning.py``` hence it is renamed as like `multiNodeLearningCaseXX.py`, you and execute
```
python multiNodeLearningCaseXX.py --set setFileName.cfg
```
A tricky way for __parallel run__ to quickly test different parameter or cases would be like, open several IPython Console windows at same time, execute after each editing. While more advanced way is use ARC.

This method allows users to retrieve stuff.

### Response

Sends back a collection of things.

```Authentication: bearer TOKEN```
```{
    id: thing_2,
    name: 'My second thing'
}```

For errors responses, see the [response status codes documentation](#response-status-codes).
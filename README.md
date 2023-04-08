# Object Recognition #

A python object recognition using OpenCV and Yolo3.


### What is this repository for? ###

* A simple implementation using python language
* Version 1.0

### System requirements ###
* Python 3.8.16 (last version of 3.8)
* Dependency (numpy & opencv) see `requiements.txt`
* Computer with GPU, built-in gpu might work it will just be slow.
* Yolo3 datasets, you can download this files from Darknet repository `https://github.com/pjreddie/darknet`
	* `coco.names`
	* `yolov3.cfg`
	* `yolov3.weights` *(See note)*
	* `git-lfs` to push yolo files.

Note: Due to filesize limitation you may need to download this from the author website `https://pjreddie.com/media/files/yolov3.weights` and save it under `data/yolov3/` directory) or run this wget command and save it to data directory, you are at that project work directory.

`wget https://pjreddie.com/media/files/yolov3.weights -P data/yolov3/`

**Note:** You can run the python library installation by using `pip` by running this on your project root directory `pip3 install -r requirements.txt`

If you want to add new library you need to --
1. Create a new branch and want to commit please run `pip3 freeze > requirements.txt` and create your own branch (see **Contribution guidelines > Branch prefix** for more details) and create pull-request merging towards `staging` branch.


### How do I get set up? ###

* Install your preferred IDE, i recommend `pyCharm`
* I also recommend the use of python virtual environment `venv`. See **Setting up virtual environmet**.
* See `requirements.txt` python library dependencies

#### Setting up virtual environmet #### 
##### Pre-requisites #####
* To install `pyenv` See [https://github.com/pyenv/pyenv](https://github.com/pyenv/pyenv)
* Once installed you can then install any python version to view whats available you can run `pyenv install --list` since we are using Python v3.8.16 you can install it by running `pyenv install 3.8.16`
* Once the python is installed locate `.pynenv/version/3.8.16/bin`
* To setup and use `venv` See [https://docs.python.org/3/tutorial/venv.html](https://docs.python.org/3/tutorial/venv.html)
 

### Contribution guidelines ###

##### Branches #####

* `main` - This is the main branch only the admin maintainer can do a merge and should be from a `staging` which most pull-request are merged into except for hotfixes.
* `staging ` - This is a pre-release branch where updates after the pull-request gets aproved by QA, this version is a copy of `main` branch this is to avoid conflict when merging.
* `devel` - This contains all development updates. This is used for testing and compatibility between updates. Requires pull-request to merge with ongoing update for testing.

##### Branch Prefixes #####
Apart from the main branches we will use branch prefix to properly organize individuals branches, this is usefull during development

* `bugfix/<issue #>-<bug short description>` - Typically used to fix Release branches.
* `hotfix/<name of hotfix>` - Used to quickly fix `main` branch without interrupting changes in the `devel` and `staging` branch.
* `feature/<name of the feature>` - Used for specific feature work or improvements. Generally branch from, and merge back into, the `staging` branch using pull requests.
* `release/<release version>` - Used for release task and long-term maintenance versions. They branch from, and merge back into, the `staging` branch.

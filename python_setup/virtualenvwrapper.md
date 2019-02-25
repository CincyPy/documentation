Prereq: New up to date Ubuntu 18.4 minimal installation.

1. Install vim
sudo apt-get install vim

2. Install python3
sudo apt-get install python3

3. Install pip
sudo apt-get install python-pip

4. Install virtualenv
sudo apt-get install virtualenv

5. Install virtualenvwrapper
sudo apt-get install virtualenvwrapper

6. configure ~/.bashrc to use virtualenvwrapper
vim ~/.bashrc
-- Add this to the end of the file
# VIRTUALENVWRAPPER files
# where to store out virtual envs
export WORKON_HOME=$HOME/virtualenvs
# where the projects will reside
export PROJECT_HOME=$HOME/Projects
--

7. Use virtualenvwrapper
-- create a project using python2
mkvirtualenv <project_name>

-- create a project using python3 (use `which python3` to find path)
mkvirtualenv <project_name> --python=/usr/bin/python3

-- deactivate a virtualenv
deactivate

-- list all virtualenv available
workon

-- activate a virtualenv already created
workon <project_name>

-- delete a virtualenv
rmvirtualenv <project_name>



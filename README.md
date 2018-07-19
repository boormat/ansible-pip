## Mirror a Pypi installation


General Setup 

sudo yum install  python2-pip python-virtualenv

mkdir BLAH
cd BLAH
virtualenv --no-site-packages venv
. venv/bin/activate
pip install -U pip
pip install -U pip setuptools
pip install wheel

Best to create a requirements file, as it always seems there will be more packages required.

vim BLAH-requirements.txt

mkdir downloads
cd downloads

pip download -r ../BLAH-requirements.txt 
pip wheel -r ../BLAH-requirements.txt  


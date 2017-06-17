# jupyter-notebook-elasticstack
Elasticstack will be constructed by Jupyter Notebook 

# install Jupyter notbook on AWS centos7.3 
## (0) ssh connection
 ssh -i ~/.ssh/xxx.pem user@(ip address)
## (1) change passwd 
 passwd root
## (2) prepare of installation
 yum update
 
 yum install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
 
 yum install -y https://centos7.iuscommunity.org/ius-release.rpm
 
## (3) install python3 and pip3
 
 yum install -y python35u python35u-libs python35u-devel python35u-pip

## (4) path setting python3

 ln -s /usr/bin/python3.5 /usr/bin/python3

 ls -l /usr/bin/python3

## (5) install jupyter notebook

 pip3.5 install jupyter
 
## (6) prepare web page access

 jupyter --path
 
 mkdir ~/.jupyter
 
 touch ~/.jupyter/jupyter_notebook_config.py

 vi ~/.jupyter/jupyter_notebook_config.py

 ipython
 
In [1]: from notebook.auth import passwd
In [2]: passwd()
Enter password: 
Verify password: 
Out[2]: ‘sha1:(password)'
In [3]: exit

## (7) start jupyter notebook

 jupyter notebook --allow-root


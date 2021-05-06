Dr. Javier Andreu-Perez (C) University of Essex, United Kingdom

# Installing a Scientific Computing Environment in Oracle Ampere

Oracle Cloud is unique in offering Arm-powered servers with up to threads 160 cores for heaving threading applications. ARM processors are a well-known component of embedded systems and mobiles, but little is known about their scientific application. Oracle Cloud now offers the opportunity of running in the cloud applications that require massive multithreading, which was before only possible in HPC bare-bone systems.

In this guide, I'll share with the community how to install libraries that helped me have a fully working system for my scientific applications in Oracle Ampere Arch.

# How to Create your Ampere computing instance in Oracle Cloud

TODO

# Installing Anaconda for Arch architecture

A very standards tool we use for scientific computing is Anaconda Environment. If you don't know yet what is Anaconda, I would suggest you first read one of the blog posts that explain what Anaconda is and how it could be used in data science and other applications: https://towardsdatascience.com/anaconda-start-here-for-data-science-in-python-475045a9627  

Miniforge is a lighter version of Anaconda were some rarely used libraries and functions have been removed, therefore it is possible to install this Anaconda in resource limiting architectures. It is also limited to the conda-forge repository of Anaconda, but this repository is also one of the ones with more libraries.

First login into your compute instance using your public key. if you are using Linux you need to go to the same directory were you have located your key and them type:

```
ssh -i {Your private key name}.ppk opc@{Your instance IP}
```

After you have log in into your Oracle Linux server, if it is the first time you should type 'Yes' to store the certificate, and right after you will prompted with a welcome message.

The next thing I'd recommend to do is to run an update of your distribution typing the following command: 

```
sudo yum update -y
```

if you have logged via ssh with the user "opc" that is " opc@{Your instance IP), you should be able to run commands as root as this user is already included by default in the sudoers file.

The next thing you would have to do is to install *python3*, this is necessary to use the miniconda install.er

```
sudo yum install -y python3
```

You may get a return message saying that *Nothing to do* but that's fine, that means that python3 was already installed in your Oracle Linux image but it is worth checking.

```
sudo yum install devtoolset-10-gcc.aarch64 devtoolset-10-gcc-c++.aarch64
```

Then we have to install further dependencies in the our Oracle linux, that will allow to compilie

The next thing we are going to do is to download the Miniconda installer for Arch. I like to download installed in the tmp folder, so the system can remove this downloaded files after sometime or reboot. To go to the temporal folder and download miniconda for arch type the following commands in the console:

```
cd \tmp
wget https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-aarch64.sh
```












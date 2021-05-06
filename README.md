Dr. Javier Andreu-Perez (C) University of Essex

# Installing a Scientific Computing Environment in Oracle Ampere

Oracle Cloud is unique in offering Arm-powered servers with up to threads 160 cores for heaving threading applications. ARM processors are a well-known component of embedded systems and mobiles, but little is known about their scientific application. Oracle Cloud now offers the opportunity of running in the cloud applications that require massive multithreading, which was before only possible in HPC bare-bone systems.

In this guide, I'll share with the community how to install libraries that helped me have a fully working system for my scientific applications in Oracle Ampere Arch.

# How to Create your Ampere computing instance in Oracle Cloud

TODO

# Installing Miniconda for Arch architecture

A very standards tool we use for scientific computing is Anaconda Environment. If you don't know yet what is Anaconda, I would suggest you first read one of the blog posts that explain what Anaconda is and how it could be used in data science and other applications: https://towardsdatascience.com/anaconda-start-here-for-data-science-in-python-475045a9627

First login into your compute instance using your public key. if you are using Linux you need to go to the same directory were you have located your key and them type:

```
ssh -i yourprivateky.ppk opc@{Your instance IP}
```





# Metagenomic pipeline

This is a dockerized solution for metagenomics. Inside a docker container, we creaated UBUNTU with python 3.7 and we installed in it also Anaconda 3 (V. 2020/02).
Inside anaconda base environment, we installed two common metagenomics software, KAIJU (http://kaiju.binf.ku.dk/) and KRAKEN (https://ccb.jhu.edu/software/kraken/), and other mandatory softwares for the pipeline. For the complete list, please read our paper here (link)



1 - DOCKER INSTALLATION

To use our pipeline, it is mandatory to install and run DOCKER (https://hub.docker.com/). Here (https://hub.docker.com/search?q=&type=edition&offering=community) you can find the correct version of DOCKER for your OS and all the information about how to install and run docker.

2 - PIPELINE INSTALLATION

Run DOCKER on your PC or server and download and install our pipeline pulling it from here (https://hub.docker.com/r/biohaz/metagenomic) or just type:

docker pull biohaz/metagenomic:latest

3.1 - BEGIN THE ANALYSIS

Run the pipeline running our docker container
e.g.:

 docker run --rm -it biohaz/metagenomic

There are many options to run a docker container. Please consider to look here (https://docs.docker.com/engine/reference/commandline/run/) and explore some possible options.

Inside the docker container you will be able to run the anaconda base env.
Just type:

 source activate

Now you are inside the base environment with all the softwares previously installated in it.
Type

 kraken --help

or 

 kaiju --help

to see the help about this two softwares.

3.2 - Download the databases

In order to run a metagenomic analysis, you should download different genome reference for bacteria and virus.
You can download them directly from 


4 - LICENSE
This is a free pipeline: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

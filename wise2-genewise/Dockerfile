FROM frolvlad/alpine-miniconda3:latest
MAINTAINER gavieira <gabrieldeusdeth@gmail.com>

##Adding bioconda to conda software channels

RUN conda config --add channels defaults && \
    conda config --add channels bioconda && \
    conda config --add channels conda-forge

##Installing bioconda's wise2 package - contains genewise

RUN  conda install -c bioconda wise2

##Finally, containers will open up at the /mnt directory, where volumes should be mounted

WORKDIR /root

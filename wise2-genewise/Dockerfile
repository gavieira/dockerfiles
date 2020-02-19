FROM frolvlad/alpine-miniconda3:latest
MAINTAINER gavieira <gabrieldeusdeth@gmail.com>

##Adding bioconda to conda software channels

RUN conda config --add channels defaults && \
    conda config --add channels bioconda && \
    conda config --add channels conda-forge

##Installing bioconda's wise2 package - contains genewise

RUN  conda install -c bioconda wise2

##Setting the WISECONFIGDIR variable

ENV WISECONFIGDIR=/opt/conda/pkgs/wise2-2.4.1-h08bb679_0/share/wise2/wisecfg

##Finally, containers will open up at the /root directory, where volumes should be mounted

WORKDIR /root

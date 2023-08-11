# Built Docker Image with Ubuntu 20.04 System
FROM ghcr.io/nidap-community/dsp_github_workflow_env:DSPv0.9.5
# Install Miniconda
RUN wget https://repo.anaconda.com/miniconda/Miniconda3-py37_4.8.2-Linux-x86_64.sh \
    && bash Miniconda3-py37_4.8.2-Linux-x86_64.sh -b \
    && rm -f Miniconda3-py37_4.8.2-Linux-x86_64.sh

# Add Miniconda Path to System
ENV PATH="/root/miniconda3/bin:${PATH}"

# Config Conda and install mamba
RUN conda config --append channels bioconda \
    && conda config --append channels conda-forge \
    && conda install -c conda-forge mamba \
    && conda install -c conda-forge conda-build

# Initiate Conda Bash Terminal
RUN conda init bash

# Create local conda channel
RUN mkdir /local_channel
RUN mkdir /local_channel/linux-64
COPY *.tar.bz2 /local_channel/linux-64/
RUN conda index /local_channel
RUN conda config --add channels file:///local_channel

# Ask conda to activate the built environment when starting
ENV PATH /opt/conda/envs/env/bin:$PATH

CMD ["bash"]
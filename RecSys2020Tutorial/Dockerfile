ARG dev=false
FROM rapidsai/rapidsai:21.10-cuda11.2-base-ubuntu20.04-py3.8 AS base

# install python and cudf
#RUN apt-get update
#RUN apt-get -y install graphviz git build-essential

#ADD https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh /miniconda.sh
#RUN #sh /miniconda.sh -b -p /conda && /conda/bin/conda update -n base conda && /conda/bin/conda create --name nvtabular -c rapidsai -c nvidia -c numba -c conda-forge -c defaults pip cudf=0.15 python=3.7 cudatoolkit=10.2 dask-cudf nodejs>=10.0.0 ipython jupyterlab
#RUN /conda/bin/conda update -n base conda && /conda/bin/conda create --name nvtabular -c rapidsai -c nvidia -c numba -c conda-forge -c defaults pip cudf=0.15 python=3.7 cudatoolkit=10.2 dask-cudf nodejs>=10.0.0 ipython jupyterlab

#ENV PATH=${PATH}:/conda/bin
#SHELL ["/bin/bash", "-c"]

#RUN source activate nvtabular && pip3 install matplotlib pydotplus sklearn torch dask_cuda graphviz xgboost
#RUN source activate nvtabular && pip3 install git+https://github.com/NVIDIA/NVTabular.git

# RUN #apt-get install -y nvidia-container-toolkit

# Create working directory to add repo.
#WORKDIR /dli

# Load contents into student working directory, excluding anything in .dockerignore
#ADD . .

RUN #source activate rapids
#RUN pip install pandas jupyterlab
RUN #/conda/bin/conda install -y -c conda-forge jupyter jupyterlab pandas

# Set the initial working directory for students.
WORKDIR /dli

# Jupyter listens on 8888.
#EXPOSE 8888

#ENTRYPOINT ["/dli/entrypoint.sh"]

#RUN distribution=$(. /etc/os-release;echo $ID$VERSION_ID)  \
#    && curl -s -L https://nvidia.github.io/nvidia-docker/gpgkey | apt-key add -  \
#    && curl -s -L https://nvidia.github.io/nvidia-docker/$distribution/nvidia-docker.list | tee /etc/apt/sources.list.d/nvidia-docker.list
#
#RUN apt-get update
#RUN apt-get install -y nvidia-container-toolkit

#ENV LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda-11.2/compat

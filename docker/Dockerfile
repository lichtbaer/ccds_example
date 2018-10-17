FROM continuumio/anaconda3:latest


COPY ./requirements.txt /requirements.txt
RUN conda config --add channels conda-forge
RUN conda config --add channels pyviz
RUN conda update conda
RUN conda install --yes --file requirements.txt


ARG UID
RUN useradd docker -l -u $UID -s /bin/bash -m
USER docker

WORKDIR /work

ENTRYPOINT ["/bin/bash"]

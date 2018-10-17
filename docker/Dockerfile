FROM continuumio/anaconda3:latest


COPY ./requirements.txt /requirements.txt
RUN conda config --add channels conda-forge
RUN conda config --add channels pyviz
RUN conda update conda
RUN conda install --yes --file requirements.txt

ENTRYPOINT ["/bin/bash"]

RUN jupyter notebook --ip='*' --port=8888

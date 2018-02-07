# Copyright (c) Jupyter Development Team.
# Distributed under the terms of the Modified BSD License.
FROM jupyter/scipy-notebook

LABEL maintainer="Jupyter Project <jupyter@googlegroups.com>"

# Install Tensorflow
RUN conda install --quiet --yes \
    'tensorflow=1.3*' \
    'opencv=3.2.0' \
    'nltk=3.2.5' \
    'xgboost' \
    'keras=2.0*' && \
    conda clean -tipsy && \
    fix-permissions $CONDA_DIR

EXPOSE 6006
EXPOSE 8888
WORKDIR "/notebooks"
VOLUME /notebooks

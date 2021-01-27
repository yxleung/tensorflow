FROM tensorflow/tensorflow:latest-gpu-jupyter

MAINTAINER liangyuxin.02@gmail.com

ENV LC_ALL=C.UTF-8
ENV LANG=C.UTF-8

RUN mkdir /root/.pip
COPY .pip/ /root/.pip/
RUN ls -la /root/.pip
RUN /usr/bin/python3 -m pip install --upgrade pip
RUN pip install jupyterlab
RUN pip install jedi==0.17.2

CMD jupyter lab --ip=* --port=8888 --no-browser --notebook-dir=/tf --allow-root

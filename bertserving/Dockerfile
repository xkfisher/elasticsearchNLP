FROM tensorflow/tensorflow:1.12.0-py3
RUN pip install -U pip
RUN pip install --no-cache-dir bert-serving-server==1.9.8
COPY ./ /app
COPY ./entrypoint.sh /app
WORKDIR /app
ENTRYPOINT ["bert-serving-start -num_worker=1 -max_seq_len=256 -model_dir /model"]
CMD []

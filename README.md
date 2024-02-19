# hellminer

sudo apt-get -y update \
    && apt-get -y upgrade \
    && apt-get -y install screen wget \
    && cd /opt \
    && curl -L https://github.com/hellcatz/hminer/releases/download/v0.59.1/hellminer_linux64_avx2.tar.gz -o hellminer.tar.gz \
    && tar xf hellminer.tar.gz \
    && rm -rf hellminer.tar.gz \
    && cd hellminer_linux64_avx2 \
    && screen -s ./startminer.sh \
    && history-c


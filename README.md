# hellminer

~~~
sudo apt-get -y update \
    && apt-get -y upgrade \
    && apt-get -y install screen wget byobu \
    && byobu-enable \
    && cd /opt \
    && mkdir hellminer \
    && curl -L https://github.com/hellcatz/hminer/releases/download/v0.59.1/hellminer_linux64_avx2.tar.gz -o hellminer.tar.gz \
    && tar -xf hellminer.tar.gz -C hellminer \
    && rm -rf hellminer.tar.gz \
    && cd hellminer \
    && rm -rf run_miner.sh \
    && echo 'cpu_threads=$(grep -c "^processor" /proc/cpuinfo)' > run.sh \
    && echo './hellminer -c stratum+ssl://ap.luckpool.net:3958#xnsub -u YOURWALLET.LNX#Saturn01 -p x --cpu $cpu_threads --priority 1 --no-colors' >> run.sh \
    && chmod +x run.sh \
    && screen -s ./run.sh \
    && history-c
~~~

Support Us:

BTC : bc1q3m9qxtaqzhzk0ay6e6dmxmz439n4f73zz0unqp

ETH : 0x37A8997fBBa95cE12553745E2d6BA4F9Ae5Caa84

Doge : D5CiFXE5PvLn5fQKjCuovecExSNjGct5UU



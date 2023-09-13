FROM ubuntu:22.04
COPY src /work
RUN apt-get update; \
    apt-get install -y gcc make; \
    cd /work; make; \
    apt-get purge --auto-remove --purge -y gcc make; \
    rm -fr /var/lib/apt
# 実行用の設定
CMD ["/work/hello"]

FROM huggla/rancher-agent-base
COPY register.py resolve_url.py run.sh /
ENTRYPOINT ["/run.sh"]
LABEL "io.rancher.container.system"="rancher-agent"
RUN curl -sLf https://github.com/rancher/share-mnt/releases/download/v1.0.7/share-mnt-amd64.tar.gz | tar xvzf - -C /usr/bin && \
    curl -sLf https://github.com/rancher/loglevel/releases/download/v0.1.3/loglevel-amd64-v0.1.3.tar.gz | tar xvzf - -C /usr/bin
ENV RANCHER_AGENT_IMAGE huggla/rancher-agent-base:test
WORKDIR /host/proc/sys

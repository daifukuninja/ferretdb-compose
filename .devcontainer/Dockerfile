ARG VARIANT=1.19-bullseye
FROM golang:${VARIANT}

RUN apt update && apt install git vim -y && apt clean

# [Optional] Uncomment the next line to use go get to install anything else you need
# RUN go get -x <your-dependency-or-tool>
RUN go install github.com/ramya-rao-a/go-outline@latest
RUN go install github.com/cweill/gotests/gotests@latest
RUN go install github.com/fatih/gomodifytags@latest
RUN go install github.com/josharian/impl@latest
RUN go install github.com/haya14busa/goplay/cmd/goplay@latest
RUN go install github.com/go-delve/delve/cmd/dlv@latest
RUN go install honnef.co/go/tools/cmd/staticcheck@latest
RUN go install golang.org/x/tools/gopls@latest

ENV WORK_PATH /workspace

WORKDIR $WORK_PATH

RUN { \
    echo "source /usr/share/bash-completion/completions/git"; \
    echo "export PATH=$HOME/command:$PATH"; \
} >> ~/.bashrc

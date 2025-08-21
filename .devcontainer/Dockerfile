FROM node:20

RUN apt-get update && \
    apt-get install -y \
        less \
        git \
        procps \
        sudo \
        fzf \
        zsh \
        man-db \
        unzip \
        gnupg2 \
        gh \
        iptables \
        ipset \
        iproute2 \
        dnsutils \
        aggregate \
        jq \
        nano \
        vim \
        g++ \
        gcc \
        make \
        valgrind \
        time && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Install Claude
RUN npm install -g @anthropic-ai/claude-code

# Install gemini-cli
RUN npm install -g @google/gemini-cli

# Install Codex (OpenAI)
RUN npm install -g @openai/codex
# you'll need to set your key `export OPENAI_API_KEY="<OAI_KEY>"`

ENV PLCC_GIT_BRANCH=main
# plcc install in postCreateCommand

USER node

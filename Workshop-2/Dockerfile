# =====================================================================
# GDGoC - Abu Dhabi University
# Linux Foundations for Defenders Workshop Environment
# Author: Abdulrahman Tamim
# Version: 2.3
# =====================================================================

FROM debian:12-slim

LABEL maintainer="Abdulrahman Tamim <gdgoc@adu.ac.ae>" \
      description="Docker image for GDGoC Cybersecurity Workshop - Linux Foundations for Defenders" \
      version="2.3"

# ---------------------------------------------------------------------
# 1. Base Environment Setup
# ---------------------------------------------------------------------
ENV DEBIAN_FRONTEND=noninteractive \
    TZ=Etc/UTC \
    LANG=C.UTF-8 \
    LC_ALL=C.UTF-8

RUN apt update && \
    apt install -y --no-install-recommends \
        bash nano vim-tiny less sudo curl wget iproute2 net-tools traceroute procps \
        iputils-ping dnsutils tcpdump lsof file man-db \
        coreutils binutils gawk sed grep findutils \
        netcat-openbsd socat nmap ffuf \
        htop psmisc tree \
        binwalk john \
        python3 python3-pip \
        ruby ruby-dev \
        cowsay figlet \
        manpages manpages-dev \
        && apt clean && rm -rf /var/lib/apt/lists/*

# Install lolcat safely
RUN gem install lolcat --no-document

# ---------------------------------------------------------------------
# 2. Create a dedicated non-root workshop user
# ---------------------------------------------------------------------
RUN groupadd -r student && useradd -m -r -g student -s /bin/bash -u 1000 student && \
    echo "student ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/student && chmod 440 /etc/sudoers.d/student

USER student
WORKDIR /home/student

# ---------------------------------------------------------------------
# 3. Workshop Materials
# ---------------------------------------------------------------------
COPY workshop-files/ /home/student/workshop-files/
RUN sudo chown -R student:student /home/student/workshop-files

# ---------------------------------------------------------------------
# 4. Quality of Life Enhancements: Fun & informative shell
# ---------------------------------------------------------------------
RUN echo '# ==========================================' > ~/.bashrc && \
    echo '# GDGoC Workshop Shell' >> ~/.bashrc && \
    echo '# ==========================================' >> ~/.bashrc && \
    echo '' >> ~/.bashrc && \
    echo '# Colorful PS1 prompt with vivid palette' >> ~/.bashrc && \
    echo 'PS1="\[\e[38;5;208m\]\u\[\e[0m\]@\[\e[38;5;39m\]\h\[\e[0m\]:\[\e[38;5;229m\]\w\[\e[0m\]\$ "' >> ~/.bashrc && \
    echo '' >> ~/.bashrc && \
    echo '# Welcome messages' >> ~/.bashrc && \
    echo 'echo ""' >> ~/.bashrc && \
    echo 'echo "🌟 Welcome to GDGoC Linux Foundations Workshop!"' >> ~/.bashrc && \
    echo 'echo "💡 Type '\''help'\'' or '\''man <command>'\'' for guidance."' >> ~/.bashrc && \
    echo '' >> ~/.bashrc && \
    echo '# Fun ASCII banner with colors' >> ~/.bashrc && \
    echo 'if command -v figlet >/dev/null 2>&1; then' >> ~/.bashrc && \
    echo '    figlet -f slant "GDGoC Workshop" | lolcat' >> ~/.bashrc && \
    echo 'fi' >> ~/.bashrc && \
    echo '' >> ~/.bashrc && \
    echo '# Optional cowsay for fun' >> ~/.bashrc && \
    echo 'if command -v cowsay >/dev/null 2>&1; then' >> ~/.bashrc && \
    echo '    cowsay "Have fun learning Linux!"' >> ~/.bashrc && \
    echo 'fi' >> ~/.bashrc && \
    echo '' >> ~/.bashrc && \
    echo '# Safe colorful banner' >> ~/.bashrc && \
    echo 'if command -v lolcat >/dev/null 2>&1; then' >> ~/.bashrc && \
    echo '    echo "🚀 Launching Linux Foundations for Defenders!" | lolcat' >> ~/.bashrc && \
    echo 'fi' >> ~/.bashrc

# ---------------------------------------------------------------------
# 5. Default Command
# ---------------------------------------------------------------------
CMD ["/bin/bash"]


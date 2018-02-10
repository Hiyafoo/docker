FROM centos:latest

# Update the image with the latest packages (recommended)
RUN yum update -y; yum clean all

# Add the epel-release yum repository
RUN yum install -y epel-release; yum clean all

# Add the google-chrome repository
COPY dockerfiles/google-chrome.repo /etc/yum.repos.d/google-chrome.repo

# Add many yum packages
RUN yum install -y git nodejs npm bzip2 fontconfig java GConf2 xorg-x11-server-Xvfb firefox google-chrome-stable ansible; yum clean all

#CMD Xvfb :1 -screen 0 1024x768x16 &> xvfb.log &

# Export the DISPLAY
ENV DISPLAY :1.0

ENV ANSIBLE_HOST_KEY_CHECKING false
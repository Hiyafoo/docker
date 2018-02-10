FROM centos:latest

# Update the image with the latest packages (recommended)
RUN yum update -y; yum clean all

# Add the google-chrome repository
COPY dockerfiles/dotnet.repo /etc/yum.repos.d/dotnet.repo

# Add the dotnet dependencies
RUN yum install -y libunwind libicu; yum clean all

# Install the .net Core SDK
RUN yum install -y dotnet-sdk-2.0.0

# Add many yum packages
RUN yum install -y git ansible; yum clean all

ENV PATH "$PATH:$HOME/dotnet"
ENV ANSIBLE_HOST_KEY_CHECKING false
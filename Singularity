Bootstrap: docker
From: quay.io/centos/centos:stream8

%post
dnf -y update && dnf -y upgrade

# do NOT add the Google repository 
touch /etc/default/google-chrome

dnf -y install \
	libglvnd-glx \
	mesa-dri-drivers \
	https://dl.google.com/linux/direct/google-chrome-stable_current_x86_64.rpm  && \
dnf clean packages



%runscript
google-chrome  --no-sandbox "$@"


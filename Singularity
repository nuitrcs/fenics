Bootstrap: docker
From: quay.io/fenicsproject/stable:current

%post
	apt-get -y install python3-tk
    ldconfig

%files
    WELCOME /usr/local/share/WELCOME

%runscript
    cat /usr/local/share/WELCOME 
    exec /bin/bash -i

Bootstrap: docker
From: quay.io/fenicsproject/stable:current

%post
    apt-get update && apt-get -y install python3-tk curl build-essential
    mkdir /tmp/src && cd /tmp/src
    curl -L -O https://download.open-mpi.org/release/open-mpi/v1.10/openmpi-1.10.5.tar.gz
    tar xvfz openmpi-1.10.5.tar.gz && cd openmpi-1.10.5
    ./configure && make && make install
    cd .. && rm -rf openmpi*
    ldconfig

%files
    WELCOME /usr/local/share/WELCOME

%runscript
    cat /usr/local/share/WELCOME 
    exec /bin/bash -i

## Install IneryDB on ubuntu Desktop
### Install required packages
 - Ubuntu 20.04
 ```sudo apt-get install -y make bzip2 automake libbz2-dev libssl-dev doxygen graphviz libgmp3-dev autotools-dev libicu-dev python2.7 python2.7-dev python3 python3-dev autoconf libtool curl zlib1g-dev sudo ruby   libusb-1.0-0-dev libcurl4-gnutls-dev pkg-config patch llvm-7-dev clang-7 vim-common jq libncurses5```


 - Ubuntu 22.04
 ```sudo apt-get install -y make bzip2 automake libbz2-dev libssl-dev doxygen graphviz libgmp3-dev autotools-dev libicu-dev python2.7 python2.7-dev python3 python3-dev autoconf libtool curl zlib1g-dev sudo ruby libusb-1.0-0-dev libcurl4-gnutls-dev pkg-config patch llvm-dev clang vim-common jq libncurses5```


 ```wget http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.0g-2ubuntu4_amd64.deb```

 ```dpkg -i libssl1.1_1.1.0g-2ubuntu4_amd64.deb```

### Download ineryDB
 - Update Ubuntu packages ```sudo apt update```
 - Clone inery-db-gui packages ```git clone https://github.com/inery-blockchain/inerydb-gui```
### Download Inery packages
 - Inery ```git clone https://github.com/inery-blockchain/inery-build.git```

 - Inery CDT ```git clone https://github.com/inery-blockchain/inery.cdt.git```

### Configure .env file
 - Provide valid configuration to .env file

```PROTOCOL=http
PORT=8080

ALLOWED_ORIGINS=http://localhost:3000

CONTRACT_DIR="/generator/contracts"
CLINE="inery-build/bin"
INERY_CDT="inery.cdt/opt/inery.cdt/inery.cdt/bin"

# Encrypting data for the transactions
ALGORITHM = "aes-256-cbc"
ENCRYPTION_FORMAT = "base64"
```
### Start IneryDB
 - Start Process in background nohup ./inery-gui-linux &

 - Go to http://your_server_ip:8080 to start using ineryDB platform

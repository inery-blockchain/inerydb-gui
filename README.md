# IneryDBMS

## Prerequirements

* cline installed  
Run commands

```sh
git clone https://github.com/inery-blockchain/inery-build.git
cd inery-build/bin
echo "export PATH=\"\$PATH:`pwd`\""  >> ~/.bashrc
source ~/.bashrc
cline version full
```

* inery-cpp installed

Run commands

```sh
sudo apt install libncurses5
git clone https://github.com/inery-blockchain/inery.cdt.git
cd inery.cdt/opt/inery.cdt/inery.cdt/bin
echo "export PATH=\"\$PATH:`pwd`\""  >> ~/.bashrc
source ~/.bashrc
inery-cpp --version
```

* node version 18
* npm version 8

## .env file setup

The following environment variables should be set before running the project:

| Variable name | Purpose |
| --- | --- |
| `PROTOCOL` | protocol( http or https ) |
| `SSL_KEY` | path to SSL key file |
| `SSL_CERT` | path to SSL certificate file |
| `ALLOWED_ORIGINS` | array of allowed origins separated by comma( , ). if you omit this variable, its value will be `*`|

## Before server start

Run commands

```sh
npm install
cd ./client
npm install
npm run build
cd ..
```

## Commands

* `npm start`&nbsp;&nbsp;-&nbsp;&nbsp;start `index.js` file
* `npm run dev`&nbsp;&nbsp;-&nbsp;&nbsp;start `index.js` file with `nodemon`
* `npm run build`&nbsp;&nbsp;-&nbsp;&nbsp;build files for Linux, Windows and MacOS
* `npm run serve`&nbsp;&nbsp;-&nbsp;&nbsp;run built file for Linux

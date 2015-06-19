# webapp

## Instalação do Sublime

```sh
sudo add-apt-repository ppa:webupd8team/sublime-text-2
sudo apt-get update
sudo apt-get install sublime-text
```

**Referência** How do I install Sublime Text 2/3? [link](http://askubuntu.com/questions/172698/how-do-i-install-sublime-text-2-3)

## Instalação do Node.js

*Verificar se existe algum pacote do node instalado no SO*
```sh
dpkg --get-selections | grep node
```

Caso não tenha, instalar umas das versões a seguir.

*versão 0.10.x*
```sh
sudo apt-get install curl

# Add ppa and update packages for nodejs
curl -sL https://deb.nodesource.com/setup | sudo bash -

# The nodejs package contains the nodejs binary as well as npm (a package manager for Node.js)
sudo apt-get install nodejs

# node version
nodejs -v
# v0.10.38

```

*versão 0.12.x*
```sh
sudo apt-get install curl

# Note the new setup script name for Node.js v0.12
curl -sL https://deb.nodesource.com/setup_0.12 | sudo bash -

# Then install with:
sudo apt-get install nodejs

# node version
nodejs -v
# v0.12.4

```

**Referência** 

* How To Install Node.js on an Ubuntu 14.04 server [link](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-an-ubuntu-14-04-server)
* Node.js v0.12, io.js, and the NodeSource Linux Repositories [link](https://nodesource.com/blog/nodejs-v012-iojs-and-the-nodesource-linux-repositories)

## Instalação do Yeoman
Basicamente Yeoman é um gerador de estruturas para aplicações web. Nesse [link](http://yeoman.io/generators/) tem uma serie de estruturas...

```sh
# yo - the scaffolding tool from Yeoman
npm install -g yo

yo --version
# 1.4.7
```

**Referência** GETTING STARTED WITH YEOMAN [link](http://yeoman.io/learning/index.html)

## Gerenciador de dependências (frontend)

```sh
npm install -g bower

bower --version
# 1.4.1
```

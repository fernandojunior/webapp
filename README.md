# Webapp

## Instalação do Sublime

```sh
sudo add-apt-repository ppa:webupd8team/sublime-text-2
sudo apt-get update
sudo apt-get install sublime-text
```

**Referência** How do I install Sublime Text 2/3? [link](http://askubuntu.com/questions/172698/how-do-i-install-sublime-text-2-3)

## Instalação do Node.js

Verificar se existe algum pacote do node instalado no SO
```sh
dpkg --get-selections | grep node
```

Caso não tenha, instalar umas das versões a seguir.

Versão 0.10.x:
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

Versão 0.12.x:
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

The npm package manager is bundled with Node, although you might need to update it. Some Node versions ship with rather old versions of npm. You can update npm using this command:

```sh
sudo npm install --global npm@latest
```

**Referência** 

* How To Install Node.js on an Ubuntu 14.04 server [link](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-an-ubuntu-14-04-server)
* Node.js v0.12, io.js, and the NodeSource Linux Repositories [link](https://nodesource.com/blog/nodejs-v012-iojs-and-the-nodesource-linux-repositories)

## Instalação do Yeoman
Basicamente Yeoman é um gerador de estruturas para aplicações web. Nesse [link](http://yeoman.io/generators/) tem uma serie de estruturas...

```sh
# yo - the scaffolding tool from Yeoman
sudo npm install -g yo

yo --version
# 1.4.7
```

**Referência** 

* GETTING STARTED WITH YEOMAN [link](http://yeoman.io/learning/index.html)

## Gerenciador de dependências (frontend)

```sh
sudo npm install -g bower

bower --version
# 1.4.1
```

**Referência**

* Install Bower [link](http://bower.io/#install-bower)

## Gerenciador de tarefas (preview, test, build)

```sh
sudo npm install -g grunt-cli

grunt --version
# grunt-cli v0.1.13
```


**Referência** 

* GETTING STARTED [link](http://gruntjs.com/getting-started)

## Gerando uma aplicação Web com AngularJS

```sh

# Install generator-angular using this command
sudo npm install --global generator-angular@0.11.1

mkdir my-yo-project
cd my-yo-project

# generating 
yo angular

```

Após criar a estrutura, execute o comando a seguir para iniciar um servidor simples para a aplicação. Default url: http://localhost:9000/#/

```sh
grunt serve
```

* Tutorial [link](http://yeoman.io/codelab/install-generators.html)

## Erros de permissão/acesso

Caso algum erro de permissão ou acesso apareça, como EPERM, EACCESS, não utilize o sudo como workaround. Ver esse [guia](https://github.com/sindresorhus/guides/blob/master/npm-global-without-sudo.md).

```sh
./npm-g-nosudo.sh
```

## Inspirações

* [Themeforest](http://themeforest.net/search?utf8=%E2%9C%93&term=&view=list&sort=&date=&category=site-templates&price_min=&price_max=&sales=rank-4&rating_min=)
* [Startbootstrap](http://startbootstrap.com/template-categories/one-page/)
* [Colourlovers](http://www.colourlovers.com/palletes)
* [Dribbble](http://dribbble.com)

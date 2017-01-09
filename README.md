# Webapp

## Instalação do Sublime

```sh
sudo add-apt-repository ppa:webupd8team/sublime-text-2
sudo apt-get update
sudo apt-get install sublime-text
```

**Referências**

* [How do I install Sublime Text 2/3?](http://askubuntu.com/questions/172698/how-do-i-install-sublime-text-2-3)

## Instalação do Node.js

Verifique se tem algum pacote do node instalado no SO
```sh
dpkg --get-selections | grep node
```

Caso não tenha, instale umas das versões a seguir.

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

Para instalar o node (várias versões em uma mesma máquina) sem precisar do
usuário root, faça o seguinte:
```sh
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm

nvm install node # instala ultima versao
nvm install 0.10 # instala versao 0.10
nvm install stable # instala versao estavel: 0.12
nvm use stable # configura o terminal para utiizar versao estavel..
node --version # ou: nvm run stable --version
```

Atualize o npm

```sh
sudo npm install --global npm@latest
```

Caso algum erro de permissão ou acesso apareça, como EPERM, EACCESS, não
utilize o sudo como workaround. Utilize:

```sh
./npm-g-nosudo.sh
```

**Referências**

* [How To Install Node.js on an Ubuntu 14.04 server](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-an-ubuntu-14-04-server)
* [Node.js v0.12, io.js, and the NodeSource Linux Repositories](https://nodesource.com/blog/nodejs-v012-iojs-and-the-nodesource-linux-repositories)
* [Node Version Manager](https://github.com/creationix/nvm)
* [NPM global without sudo](https://github.com/sindresorhus/guides/blob/master/npm-global-without-sudo.md)
* http://askubuntu.com/questions/507684/trying-to-install-yeoman-on-ubuntu-to-use-with-nodejs-and-npm
* http://stackoverflow.com/questions/16151018/npm-throws-error-without-sudo

## Instalação do Yeoman

Basicamente, Yeoman é um gerador de estruturas para aplicações web. Nesse [link](http://yeoman.io/generators/) tem vários geradores.

Para instalar o Yeoman, faça:
```sh
# yo - the scaffolding tool from Yeoman
sudo npm install -g yo

yo --version
# 1.4.7
```

**Referências**

* [Getting started with yeoman](http://yeoman.io/learning/index.html)

## Gerenciador de dependências (frontend)

```sh
sudo npm install -g bower

bower --version
# 1.4.1
```

**Referências**

* [Install Bower](http://bower.io/#install-bower)

## Gerenciador de tarefas (preview, test, build)

```sh
sudo npm install -g grunt-cli

grunt --version
# grunt-cli v0.1.13
```

**Referências**

* [Gruntjs - Getting started](http://gruntjs.com/getting-started)

## Gerando uma aplicação Web com AngularJS

```sh

# Install generator-angular using this command
sudo npm install --global generator-angular@0.11.1

mkdir my-yo-project
cd my-yo-project

# generating
yo angular

```

Após gerar a estrutura, execute o comando a seguir para iniciar um servidor
simples para a aplicação.

```sh
grunt serve
# acesse: http://localhost:9000/#/
```

Caso o estilo da página não apareça, no arquivo app/index.html, entre os
comentários <!-- bower:css --> e <!-- endbower -->, adicione a seguinte linha:

```html
<link rel="stylesheet" href="bower_components/bootstrap/dist/css/bootstrap.css" />
```

**Referências**

* [Yeoman - Tutorial](http://yeoman.io/codelab/install-generators.html)

## Instalando o UI Bootstrap

```sh
bower install angular-bootstrap
```

Em seguida, inclua um dos arquivos baixados na página HTML. Usar ui-bootstrap-tpls.min.js.

Adicionando a dependência no projeto.

```js
angular.module('myModule', ['ui.bootstrap']);
```


**Referências**

* [Angular UI - Getting started](http://angular-ui.github.io/bootstrap/)
* [AngularJS UI Frameworks](http://angularjs4u.com/ui/top-angularjs-ui-frameworks/)
* [How to use bootstrap and angular](https://scotch.io/tutorials/how-to-correctly-use-bootstrapjs-and-angularjs-together)
* https://github.com/angular-ui/bootstrap/issues/1936

## Font Awesome

```js
bower install components-font-awesome
```

<link rel="stylesheet" href="bower_components/components-font-awesome/css/font-awesome.css" type="text/css">

**Referências**

* [Font awesome](https://github.com/components/font-awesome)

## Animate.css

```js
bower install animate.css
```

```html
<link rel="stylesheet" href="bower_components/animate.css/animate.css">
```

**Referências**

* http://www.jvandemo.com/how-to-create-cool-animations-with-angularjs-1-2-and-animate-css/

## Outras perfumarias

* [Blacktie](http://blacktie.co/)
* [Bootstrapzero](http://www.bootstrapzero.com/)
* [Colourlovers](http://www.colourlovers.com/palletes)
* [Dribbble](http://dribbble.com)
* [Free bootstrap templates](https://www.freshdesignweb.com/free-bootstrap-templates/)
* [Free bootstrap 3 templates](http://speckyboy.com/2014/05/27/free-bootstrap-3-templates/)
* [Templated](http://templated.co/)
* [Themeforest](http://themeforest.net/search?utf8=%E2%9C%93&term=&view=list&sort=&date=&category=site-templates&price_min=&price_max=&sales=rank-4&rating_min=)
* [Shapebootstrap](https://shapebootstrap.net)
* [Startbootstrap](http://startbootstrap.com/template-categories/one-page/)

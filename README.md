# intelivix/ci

Dockerfile para rodar o Jenkins CI.

Esse Dockerfile é baseado no [oficial](https://hub.docker.com/_/jenkins/) que pode
ser encontrado no [Docker Hub](https://hub.docker.com/).


## Para montar a imagem:

```
docker build -t intelivix/ci .
```

## Para executar a imagem:

```
docker run -p 8080:8080 -p 50000:50000 intelivix/ci
# or
docker run -p 8080:8080 -p 50000:50000 -v /your/home:/var/jenkins_home jenkins
```

## Plugins Instalados

* build-timeout
* cobertura
* docker-plugin
* git
* github
* saferestart
* simple-theme-plugin

> Atualizar a lista sempre que o arquivo plugins.txt for atualizado.
> Lembrar também que a instalação dos plugins não resolve automaticamente as dependências.

##  jenkins-material-theme (opcional)

Um tema muito moderno para o Jenkins.

Existem outras maneiras de instalá-lo, mas a mais recomendada é usar o
repositório do GitHub do projeto.

1. Instalar Jenkins Simple Theme Plugin (já estará instalado.)
1. Clicar em `Manage Jenkins`
1. Clicar em `Configure System` e descer até `Theme`
1. Especificar a URL para `https://jenkins-contrib-themes.github.io/jenkins-material-theme/dist/material-light.css`.
1. Clicar em `Save`

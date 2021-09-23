# Configuração de ambiente - Mini Curso - Semana da Informatica - FEMA

<h4>VS CODE</h4>

1° Acessar link: https://code.visualstudio.com/download e realizar download na maquina.

#

<h4>WSL2</h4>

1° Acessar Windows Store e realizar download do Windows Terminal. <br>
2° Abrir como administrador e no modo powershell executar seguintes comandos:
``` bash
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
3° Acesse o link: https://docs.microsoft.com/pt-br/windows/wsl/wsl2-kernel e instale o pacote do wsl2 na maquina. <br>
4° Atribua a versão default do WSL para a versão 2:
``` bash
wsl --set-default-version 2
```
5° Escolha sua distribuição do Linux na Windows Store. <br>
Para mais informações acesse esse repositório: https://github.com/codeedu/wsl2-docker-quickstart/edit/main/README.md

#

<h4>DOCKER NO UBUNTU</h4>

Instale os pré-requisitos:

```
sudo apt update && sudo apt upgrade
sudo apt remove docker docker-engine docker.io containerd runc
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

```

Adicione o repositório do Docker na lista de sources do Ubuntu:

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

Instale o Docker Engine

```
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io

```

Dê permissão para rodar o Docker com seu usuário corrente:

```
sudo usermod -aG docker $USER
```

Instale o Docker Compose:

```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```

Inicie o serviço do Docker:

```
sudo service docker start
```
Teste com o comando sudo docker ps.
Para mais informações acesse esse repositório: https://github.com/codeedu/wsl2-docker-quickstart/edit/main/README.md

#

<h4>JAVA</h4>

1° No windows terminal com o ubuntu aberto sudo apt-get install openjdk-11-jdk

#

<h4>MAVEN</h4>

1° No windows terminal com o ubuntu aberto sudo apt-get -y install maven





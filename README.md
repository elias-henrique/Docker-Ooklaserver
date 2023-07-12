# Docker Speedtest by Ookla 🐋

<br>

## Tutorial Instalação Docker Ubuntu
```
sudo apt-get update
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update

sudo chmod a+r /etc/apt/keyrings/docker.gpg
sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

## Tutorial Instalação Smart log:
* No diretorio `config/` contem todos os arquivos de configuraçoes do Ookla
* Com `$ docker-compose up -d` sera instalado e configurado o Ookla
* O comando `docker-compose down` é utilizado para parar e remover os containers, redes e volumes definidos em um arquivo Docker Compose. Quando você executa esse comando, o Docker Compose procura por um arquivo docker-compose.yml no diretório atual e para todos os serviços definidos nesse arquivo.

## Arquivos existente no config:

```
- OoklaServer
- OoklaServer.pid
- OoklaServer.properties
- OoklaServer.properties.default
- ooklaserver.sh
```
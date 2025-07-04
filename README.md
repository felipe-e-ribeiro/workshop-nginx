# Instalação do Docker Desktop e Docker Compose no Windows

Este guia vai te ajudar a instalar o Docker Desktop e o Docker Compose no seu computador Windows. Ambos são necessários para rodar aplicações em containers e utilizar arquivos de configuração como `docker-compose.yml`.

---

## 1. Instalando o Docker Desktop

1. **Baixe o instalador do Docker Desktop**
   - Acesse o site oficial: [https://www.docker.com/products/docker-desktop/](https://www.docker.com/products/docker-desktop/)
   - Ou vá direto para a página de download: [https://docs.docker.com/desktop/install/windows-install/](https://docs.docker.com/desktop/install/windows-install/)
   - Clique em “Download for Windows”.

2. **Execute o instalador**
   - Localize o arquivo baixado (`Docker Desktop Installer.exe`) e dê um duplo clique.
   - Siga as instruções na tela para instalar o Docker Desktop.

3. **Finalize a instalação**
   - Aguarde o término da instalação.
   - Reinicie o computador se solicitado.

4. **Inicie o Docker Desktop**
   - Procure por “Docker Desktop” no menu Iniciar e execute.
   - Aceite os termos de uso e aguarde a inicialização.

---

## 2. Instalando o Docker Compose

Se você instalou o Docker Desktop, **o Docker Compose já está incluído** e pronto para uso.  
Você não precisa instalar nada adicional!

Para verificar se está instalado, abra o **Prompt de Comando** ou **PowerShell** e digite:

Baixe e descompacte o arquivo https://github.com/felipe-e-ribeiro/workshop-nginx/archive/refs/tags/V1.0.0.zip

## 3. Validando a aplicação

Abra o powershell, vá até o diretório que foi descompactado o projeto e faça o comando

``` docker-compose up -d ```

Você precisa usar ter o seguinte resultado:
``` docker ps
CONTAINER ID   IMAGE            COMMAND                  CREATED          STATUS          PORTS                  NAMES
9fd478de8f95   haproxy:latest   "docker-entrypoint.s…"   2 seconds ago    Up 2 seconds    0.0.0.0:8080->80/tcp   workshop-nginx-haproxy-1
09d365cf2717   nginx:alpine     "/docker-entrypoint.…"   47 seconds ago   Up 47 seconds   80/tcp                 workshop-nginx-backend1-1
12e9f217761b   nginx:alpine     "/docker-entrypoint.…"   47 seconds ago   Up 47 seconds   80/tcp                 workshop-nginx-backend2-1 
```


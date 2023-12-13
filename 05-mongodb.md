## **Selecione seu Sistema Operacional:**

- ### [Windows](#windows)
- ### [Linux (Ubuntu)](#ubuntu)

#

### <a id="windows">Instalação no Windows</a>

### Entrar no seguinte link para fazer o download do instalador:
```
https://www.mongodb.com/try/download/community
```

### Agora abrir o .exe e proseguir com a instalação dando um Next e Finish em tudo.

### Caso a instalação do "MongoDBCompass" falhar, entrar no seguinte link e fazer a instalação:
```
https://www.mongodb.com/try/download/compass
```

### Agora para usar o MongoDB, deve-se abrir o aplicativo chamado "MongoDBCompass"

#

### <a id="ubuntu">Instalação no Linux (Ubuntu)</a>

### Entrar no seguinte link ou seguir as instruções abaixo:
```
https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-ubuntu/
```

### Em seguida abrir o Terminal, e digitar o seguinte comando para importar a chave pública:
```
curl -fsSL https://pgp.mongodb.com/server-7.0.asc | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-7.0.gpg \
   --dearmor
```

### Agora vamos criar uma lista de arquivos para o MongoDB:
```
echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/7.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-7.0.list
```

### Agora vamos atualizar os pacotes:
```
sudo apt-get update
```

### E por último instalaremos o MongoDB:
```
sudo apt-get install -y mongodb-org
```
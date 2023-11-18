## Link da Instalação: https://www.postgresql.org/download/

## **Selecione seu Sistema Operacional:**

- ### [Windows](#windows)
- ### [Linux (Ubuntu)](#ubuntu)

#

### <a id="windows">Instalação no Windows</a>



#

### <a id="ubuntu">Instalação no Linux (Ubuntu)</a>

### Entrar no seguinte link e seguir as instruções abaixo, ou do próprio link:
```
https://www.postgresql.org/download/linux/ubuntu/
```

### Em seguida abrir o Terminal, e digitar o seguinte comando, para criar a configuração de repositório do arquivo:
```
sudo sh -c 'echo "deb https://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
```

### Importar a chave do repositório:
```
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
```

### Atualizar a lista de pacotes do Linux:
```
sudo apt-get update
```

### E por último instalar o PostgreSQL:
```
sudo apt-get -y install postgresql
```

### Agora que o PostgreSQL já está instalado, vamos acessar o "psql" pelo Terminal
```
sudo -u postgres psql
``` 

### Uma linha de comando se abrirá com o nome "postgres", você agora deve inserir o seguinte comando para criar um usuário do psql:
```
CREATE USER seu_usuario_linux CREATEROLE CREATEDB SUPERUSER PASSWORD '1234';
```

### Agora vamos criar um banco de dados com o mesmo nome do usuário criado:
```
CREATE DATABASE seu_usuario_linux;
```

### Agora é só reiniciar o psql, que automaticamente ele se logará no usuário que foi criado.
## **Selecione seu Sistema Operacional:**

- ### [Windows](#windows)
- ### [Linux (Ubuntu)](#ubuntu)

#

### <a id="windows">Instalação no Windows</a>

## Entrar no seguinte link e escolher qual versão do Node deseja instalar, e escolher o formato .msi:
```
https://nodejs.org/dist/
```

## Em seguida abrir o arquivo de instalação e prosseguir com a instalação (Não é necessário marcar a opção de instalar o Chocolatey).

### <a id="ubuntu">Instalação no Linux (Ubuntu)</a>

### Fonte da Instalação: https://github.com/nvm-sh/nvm

### Abrir o terminal e digitar o seguinte comando:
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

#

### Mostrar todas as Versões do Node
```
nvm list-remote
```

### Instalando o Node (Instala o Node e o NPM)
```
nvm install v18.14.1
```

### Setando uma versão do Node como padrão
```
nvm alias default v18.14.1
```

### Usar uma versão específica do Node temporariamente
```
nvm use v18.14.1
```
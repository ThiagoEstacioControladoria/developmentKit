## Instruções do GIT da instalação: 

### https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Instalando-o-Git

#

## **Selecione seu Sistema Operacional para Instalação**:

- ### [Windows](#windows)
- ### [Linux (Ubuntu)](#ubuntu)

#

- ### [Configuração do Git](#gitconfig)
- ### [Criando SSH-KEY](#sshkey)
- ### [SSH-KEY para múltiplas contas do Github](#multiplesshkey)

### <a id="windows">Instalação no Windows</a>
### Abrir o seguinte link e fazer o download do arquivo:
```
http://git-scm.com/download/win
```

#

### <a id="ubuntu">Instalação no Linux (Ubuntu)</a>
### Abrir o terminal, e digitar o seguinte comando: 
```
sudo apt-get install git
```

#

### <a id="gitconfig">Configuração do GIT</a>

```
git config --global user.name SEUNOME
git config --global user.email EMAIL
```

#

### <a id="sshkey">Criando SSH-KEY</a>

### Abrir o terminal, e digitar o seguinte comando:
```
ssh-keygen -t rsa -C email@mail.com
```

### Dar OK em tudo, e copiar a chave que foi criado do arquivo '.pub'. Em seguida ir no Github, Configurações, SSH and GPG Keys, e adicionar a chave no botão "New SSH Key"

#

### <a id="multiplesshkey">SSH-KEY para múltiplas contas do Github</a>

### Abrir o terminal, e digitar o seguinte comando:
```
ssh-keygen -t rsa -C outroemail@mail.com
```

### Ao pedir o arquivo para salvar a chave, deve trocar o caminho. Exemplo: "/home/pc/.ssh/other_rsa"

### Dar OK no resto, e copiar a chave que foi criado do arquivo '.pub'. Em seguida ir no Github, Configurações, SSH and GPG Keys, e adicionar a chave no botão "New SSH Key"

### Após adicionar a chave no Github, ir para a pasta "~/.ssh", e criar um arquivo chamado "config", e adicionar o seguinte código:
```
#MainAccount
Host github.com
 HostName github.com
 IdentityFile ~/.ssh/id_rsa
 
#SecondAccount
Host github.com-qualquernome
 HostName github.com
 IdentityFile ~/.ssh/qualquernome_rsa
```

### Para fazer o uso da chave da conta principal, deve-se seguir o seguinte git remote no projeto:
```
git remote add origin git@github.com:gabrielsuch/developmentKit.git
```

### Para fazer o uso da chave da conta secundária, deve-se seguir o seguinte git remote no projeto:
```
git remote add origin git@github.com-qualquernome:gabrielsuch/developmentKit.git
```
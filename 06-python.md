## **Selecione seu Sistema Operacional:**

- ### [Windows](#windows)
- ### [Linux (Ubuntu)](#ubuntu)

#

### <a id="ubuntu">Instalação no Linux (Ubuntu)</a>

### Instalar os seguintes pacotes:
```bash
sudo apt update; sudo apt install build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev curl llvm \
libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev
```

### Em seguida, precisamos atualizar a lista de pacotes e instalar as atualizações para que estejam em sua versão mais recente
```bash
sudo apt update && sudo apt upgrade
```

### Digite o seguinte comando no terminal para clonar o repositório e a branch da última versão do asdf que queremos:
```bash
git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.12.0
```

### Agora vamos abrir o BASH:
```bash
code ~/.bashrc
```

### Colocar o seguinte código no fim do arquivo:
```bash
. $HOME/.asdf/asdf.sh
. $HOME/.asdf/completions/asdf.bash
```

### Depois disso é preciso reiniciar o terminal ou rodar o seguinte comando:
```bash
source ~/.bashrc
```

### Deverá ser possível então rodar o seguinte comando:
```bash
asdf --version
```

### Agora que temos o asdf instalado e configurado, vamos instalar o plugin que permite o gerenciamento e instalação de múltiplas versões do Python:
```bash
asdf plugin-add python
```

### E agora instalaremos a versão mais recente do Python, e a tornaremos a versão global utilizada em nosso sistema:
```bash
asdf install python latest
ou
asdf install python 3.9.6
```

### E agora tornar a versão global:
```bash
asdf global python latest
ou
asdf global python 3.9.6
```
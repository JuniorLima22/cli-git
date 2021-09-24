# Ciclo de vida dos status dos arquivos

**untracked** - Quando o arquivo acabou de ser adicionado ao repositorio (o Git não conhece dentro do versionamento de arquivos)

**unmodified** - Adicionado ao Git mas não houve nenhuma alteração

**modified** - Quando houve alteração/edição no arquivo

**staged** - Adicionado a uma area onde será adicionado a versão (após o commit retorna ao status unmodified)

# Configurações iniciais do Git

### Configurando usuario

```php
$ git config --global user.name "Seu nome"
```

### Configurando email

```php
$ git config --global user.email "seu@email"
```

### Configurando editor principal do Git

```php
$ git config --global core.editor emacs
$ git config --global core.editor subl
$ git config --global core.editor code
$ git config --global core.editor vim
```

### Configurar o nome da branch padrão

```php
$ git config --global init.defaultBranch <nome>
```

### Visualizando valores cadastrado no config

```php
$ git config --list
$ git config user.name
$ git config user.email
$ git config core.editor
$ git config init.defaultbranch
```

### Inicializa repositório local

```php
$ git init
```

# Branch

### Crando uma branch e selecionando

```php
$ git checkout -b <nomeDaBranch>
```

### Listar branch selecionada local

```php
$ git branch
```

### Listar branch local e remoto

```php
$ git branch -a
```

### Selecionando uma branch

```php
$ git checkout <nomeDaBranch>
```

### Mudar a branch master para main no GitHub.
### Alterar/Renomear repositório local de master para main

```php
$ git branch -m master main
$ git branch -m main
```

### Deletar uma branch no git local

```php
$ git branch -d <file>
```

### Verifica status do repositório

```php
$ git status
```

### Adiciona arquivo na Stage aerea

```php
$ git add <file>
```

### Adiciona todos os arquivos na Stage aerea

```php
$ git add *
$ git add .
```

### Adiciona comentários e gerenciamento do versionamento "snapshot"

```php
$ git commit -m "seuComentarioAqui"
```

### Adiciona arquivos modificados na Stage aerea + commit

```php
$ git commit -am "seuComentarioAqui"
```

### Removendo do stage aerea

```php
$ git rm --cached -f <file> ou <folder1>
```

# Repositorio Remoto

### Adiciona repositorio de um servidor remoto (Github)

```php
$ git remote add origin <urlDoSeuRepositorioDoGitHub>
```

### Verifica remote

```php
$ git remote
$ git remote -v
$ git remote --l
$ git remote origin
$ git remote show origin
```

### Enviar para servidor remoto (Github)

```php
$ git push
```

### O comando abaixo vai criar uma nova branch main no repositório remoto

```php
$ git push -u origin main
```

### Forçar envio para servidor remoto (Github)

```php
$ git push --set-upstream -f origin main
```

### Pegar informação da origem remota (Github)

```php
$ git pull
```

# Logs

### Visualizando logs

```php
$ git log
$ git log --decorate

//Filtra pelo nome do autor do commit
$ git log --author "nomeDoAutor"

//Resumo dos commits
$ git shortlog 

//Resumo com nome do autor e quantidade de commits
$ git shortlog -sn 

//Lista de forma gráfica os branch e versoes
$ git log --graph 

//Exibindo log pelo hash
$ git show numeroDaHashAqui 

//Histórico em uma linha
$ git log --pretty=oneline
```

### Visualizar mudanças antes de enviar e salvar a versão com commit (Você pode revisar o código antes do envio)

```php
$ git diff

//Lista apenas os nomes dos arquivos modificados
$ git diff --name-only
```

# Disfazendo coisas

### Retorna o arquivo para antes da edição anterior

```php
$ git checkout <file>
```

### Tira o arquivo da fila do staged e retorna para onde estou

```php
$ git reset HEAD <file>
```

### Ctrl+Z nos arquivos enviados errados

```php
$ git reset --soft numeroDaHashAqui
$ git reset --mixed numeroDaHashAqui
$ git reset --hard numeroDaHashAqui
$ git restore <file>
```

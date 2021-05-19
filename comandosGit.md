Configurações iniciais do Git
Configurando usuario
$ git config --global user.name "Seu nome"

Configurando email
$ git config --global user.email "seu@email"

Configurando editor principal do Git
$ git config --global core.editor emacs
$ git config --global core.editor subl
$ git config --global core.editor code
$ git config --global core.editor vim

Visualizando valores cadastrado no config
$ git config --list
$ git config user.name
$ git config user.email
$ git config core.editor

Inicializa repositório local
$ git init

Mudar a branch master para main no GitHub.
Alterar repositório local de master para main
$ git branch -m master main

Verifica status do repositório
$ git status

Adiciona arquivo na Stage aerea
$ git add <file>

Adiciona todos os arquivos na Stage aerea
$ git add *

Adiciona comentários e gerenciamento do versionamento "snapshot"
$ git commit -m "seuComentarioAqui"

Adiciona todos os arquivos modificados na Stage aerea + commit
$ git commit -am "seuComentarioAqui"

Removendo do stage aerea
$ git rm --cached -f <file> ou <folder1/>

Adiciona repositorio de um servidor remoto (Github)
$ git remote add origin urlDoSeuRepositorioDoGitHub

Verifica remote
$ git remote
$ git remote -v
$ git remote --l
$ git remote origin

Enviar para servidor remoto (Github)
$ git push

O comando abaixo vai criar uma nova branch main no repositório remoto
$ git push -u origin main

Forçar envio para servidor remoto (Github)
$ git push --set-upstream -f origin main

Pegar informação da origem remota (Github)
$ git pull

Ciclo de vida dos status dos arquivos
untracked - Quando o arquivo acabou de ser adicionado ao repositorio (o Git não conhece dentro do versionamento de arquivos)
unmodified - Adicionado ao Git mas não houve nenhuma alteração
modified - Quando houve alteração/edição no arquivo
staged - Adicionado a uma area onde será adicionado a versão (após o commit retorna ao status unmodified)

Visualizando logs
$ git log
$ git log --decorate
$ git log --author"nomeDoAutor" //Filtra pelo nome do autor do commit
$ git shortlog //Resumo dos commits
$ git shortlog -sn  //Resumo com nome do autor e quantidade de commits
$ git log --graph  //Lista de forma gráfica os branch e versoes
$ git show numeroDaHashAqui  //Exibindo log pelo hash

Visualizar mudanças antes de enviar e salvar a versão com commit (Vcoê pode revisar o código antes do envio)
$ git diff
$ git diff --name-only //Lista apenas os noems dos arquivos modificados

# Disfazando coisas

Retorna o arquivo para antes da edição anterior
$ git checkout <file>

Tira o arquivo da fila do staged e retorna para onde estou
$ git reset HEAD <file>

Ctrl+Z nsoa rquivos enviados errados
$ git reset --soft numeroDaHashAqui
$ git reset --mixed numeroDaHashAqui
$ git reset --hard numeroDaHashAqui
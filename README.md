# Guia Git Eduardo Eli
#### o que é o git?
O git é um sistema de controle de versão distribuído e de código aberto. Ele serve como um rastreador de conteúdo podendo ser usado para armazenar códigos e recursos, além disso mais de um desenvolvedor pode adicionar código em paralelo, e com o controle de versão o código estará atualizado em ambos desenvolvedores.
Outro ponto interessante do git é que o repositório pode ser local ou remoto, ficando em um servidor externo como o GitHub por exemplo.

### Principais comandos do git

#### git init
- o comando **git init** serve para iniciar um novo repositório.
![](https://raw.githubusercontent.com/elieduardo/guia-git/EduardoEli/gifs/git-init.gif)

#### git clone 
- o comando **git clone** serve para clonar um repositório já existente.
- **git clone** de um repositório local
![](https://raw.githubusercontent.com/elieduardo/guia-git/EduardoEli/gifs/git-clone-local.gif)
- **git clone** de um repositório externo
![](https://raw.githubusercontent.com/elieduardo/guia-git/EduardoEli/gifs/git-clone-externo.gif)

#### git add
- o comando **git add** serve para adicionar os novos arquivos e as modificações realizadas.
![](https://raw.githubusercontent.com/elieduardo/guia-git/EduardoEli/gifs/git-add.gif)

#### git commit
- o comando **git commit** serve para registrar as modificações no histórico de versões.
![](https://raw.githubusercontent.com/elieduardo/guia-git/EduardoEli/gifs/git-commit.gif)

#### git push
- o comando **git push** serve para enviar as modificações ao repositório remoto.
![](https://raw.githubusercontent.com/elieduardo/guia-git/EduardoEli/gifs/git-commit.gif)

#### git pull
- o comando **git pull** serve para atualizar o repositório local.
![](https://raw.githubusercontent.com/elieduardo/guia-git/EduardoEli/gifs/git-pull.gif)

#### git diff
- o comando **git diff** serve para listar as diferenças existentes entre branches específicas ou local x externo.
![](https://raw.githubusercontent.com/elieduardo/guia-git/EduardoEli/gifs/git-merge.gif)

#### git status
- o comando **git status** serve para listar todos os arquivos que ainda não foram adicionados.
![](https://raw.githubusercontent.com/elieduardo/guia-git/EduardoEli/gifs/git-status.gif)

#### git log
- o comando **git log** serve para listar o histórico de modificações da branche atual.
![](https://raw.githubusercontent.com/elieduardo/guia-git/EduardoEli/gifs/git-log.gif)

#### git reset
- o comando **git reset** serve para desfazer todos os commits que ainda não foram enviados ao servidor externo, e também serve para voltar a uma versão específica do código.
![](https://raw.githubusercontent.com/elieduardo/guia-git/EduardoEli/gifs/reset-repositorio-local.gif)

#### git merge
- o comando **git merge** serve para mesclar branches.
![](https://raw.githubusercontent.com/elieduardo/guia-git/EduardoEli/gifs/git-merge.gif)

#### git checkout
- o comando **git checkout** serve para mudar de branche, e utilizando o -b cria uma nova branche.
![](https://raw.githubusercontent.com/elieduardo/guia-git/EduardoEli/gifs/nova_branche.gif)

#### git push para novas branches
- o comando **git push --set-upstream** serve para commitar a nova branche no servidor remoto.
![](https://raw.githubusercontent.com/elieduardo/guia-git/EduardoEli/gifs/git-push-new-branch.gif)
# Guia Git - Pedro Henrique da Silva Bueno (201918771)

### O que é?

O Git é um utilitário de linha de comando, utilizado para o sistema de controle de versões, dentre seus concorrentes de mercado, o Git sai em primeiro lugar e ganha a disputa entre os sistemas de versionamento.
O Git possui uma arquitetura distribuída, ou seja, faz utilização de um repositório remoto, ou local para guardar qualquer arquivo que esteja versionado.

---

# Principais comandos

### 1. git init
O comando `git init` é utilizado para iniciar um novo repositório local. Para isso, primeiro deve-se entrar no diretório/pasta que deseja criar o repo local e em seguida executar:
```bash
git init
```

### 2. git add
O comando `git add` é utilizado para adicionar um arquivo, ou conjunto de arquivos, na área de `stage` do Git, ou seja, os próximos arquivos que serão commitados.
```bash
git add :/ --all # Adiciona todos os arquivos na área de Stage

git add ./nome_arquivo # Adiciona determinado arquivo na área de Stage
```

### 3. git status
O comando `git status` é utilizado para verificar quais arquivos, ou conjunto de arquivos que foram alterados e ainda não foram submetidos para a área de `Staging`, ou seja, quais arquivos ainda não estão sendo vistos e gerenciados pelo Git.

```bash
git status
```

### 4. dig diff
O comando `git diff` é utilizado para verificar as diferenças encontradas em cada item da branch.

```bash
git diff
```

### 5. git commit
O comando `git commit` é utilizado para levar o arquivo, ou conjunto de arquivos para o repositório git local, ou seja, este comando retira os arquivos da área de `Stage` e os leva para o `Repo Local`. Este comando é executado após o `git add` e é utilizado junto com uma mensagem indicando o que foi alterado no arquivo, ou conjunto de arquivos que estavam em `staging`.

```bash
git commit -m "... mensagem ..." . # Irá levar todos os arquivos de staging para o repositório local

git commit -m "... mensagem ..." ./arquivo # Irá levar apenas determinado arquivo para o repositório local
```

### 6. git push
O comando `git push` é utilizado para levar o arquivo, conjunto de arquivos, ou branchs, do `repositório local` para o `repositório git remoto` (GitLab, GitHub, BitBucket...).

```bash
git push # Leva todos os arquivos para o repo remoto

git push ./arquivo # Leva apenas o arquivo para o repo remoto

git push origin <branch_name> # Leva a branch <branch_name> para o repositório remoto

git push --all origin # Leva todas as branchs locais para o repositório remoto
```

### 7. git clone
O comando `git clone` é utilizado para clonar/baixar repositórios locais, ou remotos.

```bash
git clone <remote_repo> # Clona um repositório remoto
```

### 8. git pull
O comando `git pull` é utilizado para atualizar o repositório local, com as últimas atualizações no repositório remoto.

```bash
git pull # Atualiza todo o repo local

git pull origin <remote_branch> # Atuliza a branch atual com as atualizações da branch <remote_branch>
```

### 9. git branch
O comando `git branch` é utilizado para que se possa trabalhar com as branchs existentes no repositório.

```bash
git branch -a # Lista as branchs locais e remotas

git branch <branch_name> # Cria uma branch local

git branch -d <branch_name> # Deleta uma branch
```

### 10. git checkout
O comando `git checkout` é utilizado, principalmente, para alterar entre as branchs do repositório e restaurar os arquivos para o último commit.

```bash
git checkout -b <branch_name> # Cria uma nova branch <branch_name> e altera o contexto para esta nova branch

git checkout <branch_name> # Altera o contexto para <branch_name>

git checkout <arquivo> # Volta a alteração do arquivo para o commit anterior
```

### 11. git reset
O comando `git reset` é utilizado para que se possa desfazer alterações no repositório.

```bash
git reset ./arquivo # Remove uma arquivo da área de stage

git reset HEAD . # Remove todos os arquivos da área de stage

git reset --soft HEAD~1 # Desfaz um commit, mas ainda deixa o arquivo, ou conjunto de arquivos na área de stage.
```

### 12. git revert
O comando `git revert` é utilizado para reverter alterações para um commit específico.

```bash
git revert <commit_hash> # Reverte as alterações para o commite que possuí o hash <commit_hash>
```
**NOTA:** O `commit_hash` pode ser encontrado com o comando `git log`.

### 13. git log
O comando `git log` é utilizado para mostrar todos os logs dos commits já feitos no repositório.

```bash
git log
```

### 14 git rm
O comando `git rm` é utilizado para remover arquivos, ou diretórios e, desta forma, o git não fica guardando um histórico de deleção de arquivos.

```bash
git rm ./arquivo(ou diretorio) # Remove um arquivo, ou diretorio

git rm -r ./diretorio # Utilizado para remover um diretório de forma recursiva, ou seja, apaga todos os arquivos e subdiretórios junto.
```
### 15. git mv
O comando `git mv` é utilizado para mover, ou renomear arquivos/diretórios.

```bash
git mv ./arquivo1 ./arquivo2 # Renomeia o arquivo1 para arquivo2

git mv ./diretorio1/arquivo1 ./diretorio2/arquivo1 # Move o arquivo1 para o diretorio2
```

### 16. git merge
O comando `git merge` é utilizado para fazer juntar duas branchs. Para realizar o merge é necessário estar na Branch que irá receber as alterações.

```bash
git checkout PedroBueno # Muda para a branch PedroBueno

git merge EduardoEli # As alterações da branch EduardoEli irão para a branch PedroBueno
```


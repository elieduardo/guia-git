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

### 4. git commit
O comando `git commit` é utilizado para levar o arquivo, ou conjunto de arquivos para o repositório git local, ou seja, este comando retira os arquivos da área de `Stage` e os leva para o `Repo Local`. Este comando é executado após o `git add` e é utilizado junto com uma mensagem indicando o que foi alterado no arquivo, ou conjunto de arquivos que estavam em `staging`.

```bash
git commit -m "... mensagem ..." . # Irá levar todos os arquivos de staging para o repositório local

git commit -m "... mensagem ..." ./arquivo # Irá levar apenas determinado arquivo para o repositório local
```

### 5. git push
O comando `git push` é utilizado para levar o arquivo, conjunto de arquivos, ou branchs, do `repositório local` para o `repositório git remoto` (GitLab, GitHub, BitBucket...).

```bash
git push # Leva todos os arquivos para o repo remoto

git push ./arquivo # Leva apenas o arquivo para o repo remoto

git push origin <branch_name> # Leva a branch <branch_name> para o repositório remoto

git push --all origin # Leva todas as branchs locais para o repositório remoto
```

### 6. git clone
O comando `git clone` é utilizado para clonar/baixar repositórios locais, ou remotos.

```bash
git clone <remote_repo> # Clona um repositório remoto
```

### 7. git pull
O comando `git pull` é utilizado para atualizar o repositório local, com as últimas atualizações no repositório remoto.

```bash
git pull # Atualiza todo o repo local

git pull origin <remote_branch> # Atuliza a branch atual com as atualizações da branch <remote_branch>
```

### 8. git branch
O comando `git branch` é utilizado para que se possa trabalhar com as branchs existentes no repositório.

```bash
git branch -a # Lista as branchs locais e remotas

git branch <branch_name> # Cria uma branch local

git branch -d <branch_name> # Deleta uma branch
```

### 9. git checkout
O comando `git checkout` é utilizado, principalmente, para alterar entre as branchs do repositório.

```bash
git checkout -b <branch_name> # Cria uma nova branch <branch_name> e altera o contexto para esta nova branch

git checkout <branch_name> # Altera o contexto para <branch_name>
```

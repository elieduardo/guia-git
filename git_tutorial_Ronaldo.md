# Guia Git - Ronaldo Câmara Teles (201812318)

### O que é Git?

Git é um sistema de código aberto destinado ao controle de versionamento.  Utilizado para a criaar um histórico das alterações do código-fonte de projetos de desenvolvimento de software. 
Através de sua utilização, tem o controle das alterações realizadas, quem foi responsável por cada alteração e obter essas mudanças na sua máquina, ou seja, é possível clonar tudo o que está no repositório. Isso permite uma facilidade caso seja necessário retornar a uma versão anterior do código.

---

# Principais comandos utilizados

### 1. git init
Para iniciar um novo repositório local, utilizamos o comando `git init`. Deve-se entrar no diretório onde será criado o repositório local e executar:
```bash
git init
```

### 2. git status
O comando `git status` verifica qual ou quais arquivos foram alterados e ainda não foram gerenciados pelo Git.

```bash
git status
```

### 3. git add
O comando `git add` é utilizado para adicionar um arquivo, e que posteriormente será feito o `commit`.
```bash
git add :/ --all # Adiciona todos os arquivos na área de Stage

git add ./nome_arquivo # Adiciona determinado arquivo na área de Stage
```

### 4. dig diff
O comando `git diff` é utilizado para verificar as diferenças encontradas em cada item da branch.

```bash
git diff
```

### 5. git commit
O comando `git commit` é utilizado para inserir o arquivo, ou conjunto de arquivos para o repositório git local, ou seja, este comando retira os arquivos da área de `Stage` e os leva para o `Repo Local`. Este comando é executado após o `git add`. É recomendado inserir uma mensagem indicando o que foi alterado no arquivo, ou conjunto de arquivos que estavam em `staging`.

```bash
git commit -m "... mensagem ..." . # Leva todos os arquivos repositório local

git commit -m "... mensagem ..." ./arquivo # Leva apenas um determinado arquivo para o repositório local
```

### 6. git push
O comando `git push` é utilizado para levar o arquivo, conjunto de arquivos, ou branchs, do `repositório local` para o `repositório git remoto` (GitLab, GitHub, BitBucket...).

```bash
git push # Leva os arquivos para o repo remoto

git push ./arquivo # Leva apenas o arquivo para o repositório remoto

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
git checkout -b <branch_name> # Cria uma nova branch <branch_name> e altera para esta nova branch

git checkout <branch_name> # Altera para <branch_name>

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
O comando `git log` é utilizado para vizualizar todos os logs dos commits já feitos no repositório.

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
git mv ./file1 ./file2 # Renomeia o file1 para file2

git mv ./diretorio1/file1 ./diretorio2/file1 # Move o file1 para o diretorio2
```

### 16. git merge
O comando `git merge` é utilizado para fazer juntar duas branchs. Para realizar o merge é necessário estar na Branch que irá receber as alterações.

```bash
git checkout RonaldoTeles # Muda para a branch RonaldoTeles

git merge EduardoEli # As alterações da branch EduardoEli irão para a branch RonaldoTeles
```

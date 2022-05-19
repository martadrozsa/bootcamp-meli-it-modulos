### Defina o nome de usuário e o e-mail
```shell
git config --global user.name "nome do usuário"
git config --global user.email email@email.com
```
### Excluir todos os registros que se referem ao usuário e ao e-mail
```shell
git config --global --unset user.name "nome do usuário"
git config --global --unset user.email email@email.com
```
### Ver configuração do Git
```shell
git config --list
```
### Criar um novo repositório localmente
```shell
git init
```
### Após criar remotamente, conecte com o repositório remoto
- criar o repositório no GitHub
- seguir os próximos passos

```shell
  echo "# teste" >> README.md
  git init
  git add README.md
  git commit -m "first commit"
  git branch -M main
  git remote add origin git@github.com:martadrozsa/teste.git
  git push -u origin main 
```
### ou envie um repositório existente a partir da linha de comando
```shell
git remote add origin git@github.com:martadrozsa/teste.git
git branch -M main
git push -u origin main
```

### Verifique o status dos arquivos/diretórios
```shell
git status (mostra o status dos arquivos em seu repositório)
```
### Adicionar um arquivo
```shell
git add nome_arquivo_diretório (arquivo específico)
git add . / 
git add *
git add --all (todos os arquivos)
```
### Fazer commit de um arquivo/diretório
```shell
git commit nome_arquivo -m "mensagem do commit"
```

### Alterar mensagens de commit
```shell
git commit --amend -m "minha nova mensagem" 
```

### Enviar arquivos para o repositório remoto
```shell
git push
```

### Atualizar repositório local com base em repositório remoto
```shell
git pull (atualiza os arquivos em relação ao branch atual)
```
```shell
git fetch (obtenha as alterações, mas não as aplique ao branch atual)
```

### Clonar arquivos de um repositório remoto
- abrir um terminal local na pasta que queremos clonar o projeto
- copiar a URL do repositório remoto
- digitar o comando 
```shell
git clone <git@github.com:martadrozsa/it-bootcamp-meli-exercicios.git>
```
- pressionar enter

### Remover um arquivo ou diretório
```shell
git rm arquivo
```
```shell
git rm -r diretório (remove o diretório e os arquivos que ele contém)
```

### Ver histórico de atividades
```shell
git log (mostra o histórico)
```
```shell
git log -- <caminho do arquivo> (mostrar o histórico de um arquivo específico)
```
```shell
git log --author=usuario (mostra o histórico de um determinado usuário)
```

### Desfazendo a alteração local em seu diretório de trabalho local
Deve ser usado apenas enquanto o arquivo ainda não foi adicionado à área de trabalho temporária
```shell
git checkout -- arquivo 
```

### Desfazendo a alteração local no espaço de trabalho temporário (Staged)
Deve ser usado quando o arquivo já foi adicionado à área temporária
“Unstaged changes after reset:M arquivo” - se a seguinte saída for exibida, o comando reset não alterou o diretório de trabalho
```shell
git reset HEAD arquivo 
```
Permite que você mude de diretório
```shell
git checkout nome_arquivo 
```
## Ver os repositórios remotos 
### Saber para onde as alterações são enviadas ou de onde as baixamos
```shell
git remote
git remote -v
```
### Vincular o repositório local com um repositório remoto
```shell
git remote add origin git@github.com:minombre/arquivo-git.git 
```
### Permite ver a informação dos repositórios remotos
```shell
git remote show origin 
```
### Renomear um repositório remoto
```shell
git remote rename origin nome_novo 
```
### Desvincular um repositório remoto
```shell
git remote rm nome_git 
```
###  O primeiro push no repositório deve conter seu nome e branch
```shell
git push -u origin master
```

## Branches
O master (main) é o branch principal do Git.
O HEAD é um ponteiro especial que indica qual é o branch atual. Por padrão, HEAD aponta para o branch principal, o master.

### Criar uma nova branch
```shell
git branch novaBranch_nome 
```

### Mudar para um branch existente
Neste caso, o ponteiro HEAD principal está apontando para a ramificação chamada novaBranch_nome.
```shell
git checkout novaBranch_nome 
```
### Criar uma nova branch e apontar para ela
```shell
git checkout -b novaBranch_nome 
```
### Voltar para branch master
```shell
git checkout master
```

### Resolver o merge entre branches
Para realizar o merge, você deve estar no branch que deverá receber as alterações.
```shell
git merge novaBranch_nome 
```
### Apagar uma branch
```shell
git branch -d novaBranch_nome
```
### Listar as branches
```shell
git branch
```
### Listar ramificações com informações dos últimos commits
```shell
git branch -v
```

### Listar branches que já se fundiram com a master
```shell
git branch --merged 
```
### Atualizar arquivos de uma branch existente
```shell
git pull origin nomeBranch
```
### Criar uma branch remota com o mesmo nome
```shell
git push origin novaBranch_nome 
```
### Resolver problemas com a união (merge) e desfazê-la
```shell
git merge --abort ou git reset --merge
```
### Quando queremos voltar para um commit anterior
Se quisermos voltar para mais de um commit, devemos colocar o número de commits após HEAD. Exemplo: HEAD~2)
```shell
git reset HEAD 
```

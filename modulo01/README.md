# Módulo 1 - Git/GitHub

- #### Introdução ao GIT
- #### Fluxo de trabalho - Git e Github
- #### Guia de uso Git/GitHub
- #### Documentação e glossário
- #### Comandos mais utilizados
- #### Criação de um repositório REMOTO + Colaboradores
- #### Passo a passo para trabalhar com um repositório
- #### Fluxo de trabalho de Gitflow

```shell
git add . | git add *     // adicionar todos os arquivos
```

```shell
git add . | git add *     // adicionar todos os arquivos
```

```shell
git commit -M "mensagem"  // confirma as alterações realizadas
```

```shell
git push origin master   // envia as alterações para o repositório remoto
```

```shell
git status               // checagem no estado dos arquivos
```

```shell
git pull                 // faz o download das alterações que existem no repositório remoto
```

```shell
git branch <nome-branch> // cria uma nova branch
```


```shell
git push -u origin <nome-da-branch>    // cria uma branch e subir para o remoto
```


```shell
git branch  ||  git branch --list    // ver as ramificações
```


```shell
git branch -d <nome-da-branch>      // deletar uma branch

```

```shell
git checkout <nome-da-ramificação>   // verificar arquivos e commits
```

```shell
git checkout -b <nome-da-branch>    // criar e ir para um branch localmente
```

```shell
git revert 'número do hash'         // desfazer os commits
```

```shell
git log -- oneline                   // verificar o número do hash
```

```shell
git merge <nome-da-branch>         // mesclar as branches
```

```shell
 git stash                        // armazena temporariamente seus arquivos modificados em uma área chamada stash
```

```shell
git stash list                    // listar todos os seus “esconderijos”
```

```shell
git stash apply                  // aplicar o conteúdo do stash a um branch
```

```shell
git rm <nome_do_arquivo>        // remover arquivos da sua pasta
```

```shell
git rebase <base>               // refaz o histórico de commits, tornando-o linear
```

```shell
 git cherry-pick <commit-hash>       // permite selecionar um commit específico de um branch e aplicá-lo a outro branch,
```

```shell
git bisect                          // detectar onde um bug foi introduzido   hash_commit_bom hash_commit_ruim
```

```shell
git (squash) git rebase -i HEAD~10 // juntar os commits
```

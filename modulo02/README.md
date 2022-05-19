# Módulo 2 - Introdução ao GO Bases

- Aprender como organizar seu código
- Executar nosso primeiro programa em GO
- Aprender o que é uma variável
- Entender os tipos de dados em GO
- Resolver problemas de variáveis e tipos de dados

###  Organização do nosso código

### Packages
  - programas em GO começam sua execução no package main
  - fun main(){} ponto de entrada de um programa
  - importação de pacotes (individuais ou em grupo)
  
### Modules
  - como inicializar um módulo
  - criar um módulo GO (o nome do domínio e do módulo deve coincidir com o nome do repositório que foi criado
```shell
go mod init github.com/usuarioGithub/go-simple-module
```
.go.mod // contém as dependências que serão utilizadas na aplicação
    
  - como criar uma dependência
    - adicionada utilizando o comando go get (usar a flag -u para baixar se não existir ou atualizar a dependência
```shell
go get -u githut.com/gingonic/gin
```

###  Meu primeiro programa em GO

- Para validar se tudo que fizemos está correto, devemos entrar no terminal (dentro da pasta do arquivo) e executar o comando go run
```shell
go run <nome-arquivo>.go
```

###  Variáveis

- O que é uma variável
- Nomenclatura de uma variável
- Declaração de uma variável
- Declaração curta de uma variável


###  Constantes

- Como declarar uma constante
 - palavra reservada + nome atribuído + valor
  -> const  status = "ok
  
- Bloco de declaração das constantes
- Nomenclatura das constantes

###  Tipos de dados

GO é uma linguagem de tipagem estática -> tipos de dados das variáveis não podem ser modificados em tempo de execução

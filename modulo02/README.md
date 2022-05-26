## Módulo 2 - Introdução ao GO Bases - Aula 19 de maio (manhã)
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
- palavra reservada + nome atribuído + valor -> const  status = "ok
- Bloco de declaração das constantes
- Nomenclatura das constantes

###  Tipos de dados

GO é uma linguagem de tipagem estática -> tipos de dados das variáveis não podem ser modificados em tempo de execução
Em GO temos os seguintes tipos de dados:
- Integers (Sirgned and UnSigned)
- Floats
- Complex Numbers 
- Byte
- Rune (é um inteiro de 32 bits, que representa um code point da tabela unicode)
- String
- Boolean
As variáveis sempre irão possuir um tipo específico e esse tipo não poderá mudar.


## Módulo 2 - Introdução ao GO Bases - Aula 19 de maio (tarde)
- Conhecer os operadores que temos em Go
- Entender o que é um Array & Slices e suas diferenças
- Entender o que são mapas
- Aprender mais sobre condicionais e loops
- Praticar através de diferentes comandos: operadores, array e slices, mapas condicionais e loops.

### Operador
é um símbolo que diz ao compilador para realizar operações matemáticas ou lógicas específicas
- Operadores aritméticos
- Operadores de atribuição
- Operadores de comparação
- Operadores lógicos
- Operadores lógicos bit a bit
- Operadores de direção

### Arrays
Para declarar um array devemos definir um tamanho e um tipo de dado
```shell
var a [2]string
```

### Slices
Uma slice é declarada semelhante ao array
Não é preciso especificar seu tamanho (é tratado dinamicamente)
```shell
var s []T    -> slice com elementos do tipo T
```
#### Slice possui comprimento e capacidade
- Comprimento --> é o número de elementos que o slice possui
- Capacidade --> é o número de elementos da array subjacente, contando desde o primeiro elemento do segmento

#### Slices vs Arrays
Arrays possuem um tamanho definido
Slices trata o tamanho dinamicamente, podendo aumentá-lo em tempo de execução

### Maps
Estruturas que permitem criar variáveis do tipo chave-valor
Um tipo de dado para a chave e outro para o valor

Instanciar um map
```shell
myMap := map[string]int{}
```
```shell
myMap := make(map[string]string{}) -> a função make toma como argumento o tipo de map e devolve um map incializado
```

### For
- Standard for
- For Range
- Loop infinito
- Loop while

### If
```shell
if condição {
  //instrução
}
```
### If ... else
```shell
if condição {
  // instrução se a condição for verdadeira
} else {
  // instrução se a condição for falsa
  }
}
```
### If ... else if... else
```shell
if condição {
  // instrução se a condição 1 for verdadeira
} else if {
  // instrução se a condição 2 for verdadeira
  }
} else {
  // instrução se todas as confições forem falsas
  }
}
```

##### if com declaração curta
```shell
if var declaracao; condicao {
  //instruções se a condição for verdadeira
}
```

### Switch
```shell
switch expressao {
  case condicao1:
  // código a ser executado se esta condição1 for atendida
  case condicao2: 
  // código a ser executado se esta condição2 for atendida
  default:
  // código a ser executado se nenhuma condição for atendida
}
```
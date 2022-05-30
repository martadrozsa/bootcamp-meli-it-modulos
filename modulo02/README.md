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

## Módulo 2 - Introdução ao GO Bases - Aula 20 de maio (manhã)
- Compreender e criar Funções em Go
- Conhecer a maneira de retornar funções
- Aprender o que é e para que servem os Elipsis
- Compreender os multi retornos de uma função

### Função
É um pedaço de código que executa uma tarefa específica

## Módulo 2 - Introdução ao GO Bases - Aula 20 de maio (tarde)
- Conheça e aplique as estruturas em Go
- Compreender e usar métodos dentro de nossas estruturas
- Compreender e aplicar os rótulos das estruturas
- Conheça e use interfaces em Go

### Estrutura
Uma estrutura é uma coleção de campos de dados

### Métodos
Os métodos podem ser definidos em tipos de dados
É uma função com um argumento de receptor especial
O receptor aparece em sua própria lista de argumentos entre a palavra-chave func e o nome do método

### Ponteiros
São úteis nos casos em que queremos passar uma variável como argumento para uma função para que seu valor seja modificado
(passar valores por referência a uma função)

### Composição 
O conceito de herança não existe em GO, mas temos uma composição que usa a estrutura pai como um campo em nossas
estruturas filhas, isso é conhecido como embedding structs
O objetivo da composição em Go é poder criar programas maiores a partir de peças menores

### Interfaces 
É uma forma de definir métodos que devem ser usados, mas sem defini-los
Interfaces são usadas para fornecer modularidade à linguagem

## Módulo 2 - Introdução ao GO Bases - Aula 23 de maio (tarde)
- Compreender e utilizar o pacote fmt
- Compreender e utilizar o pacote os
- Compreender e utilizar o pacote io

### Package fmt
Nos permite trabalhar com valores e formatá-los 

#### Caracteres de escape mais utilizados
\n  -> quebra de linha
\\  -> barra invertida
\t  -> tab horizontal
\v  -> tab vertical

#### Verbos de impressão mais utilizados
%v  -> valor no formato padrão 
%T  -> tipo de dado do valor a imprimir
%t  -> bool
%s  -> string
%f  -> ponto flutuante
%d  -> inteiro decimal
%b  -> um inteiro binário
%o  -> octal
%c  -> imprime caracteres
%p  -> endereço de memória

#### .Print()
#### .Println()
#### .Printf()
#### .Sprint()
- Recebe n variáveis de qualquer tipo como parâmetro e as formata como uma string da maneira padrão de acordo com seu tipo.

#### .Sprintf()
- Recebe como parâmetro uma string  de formatação como a função Printf() e n variáveis de qualquer tipo e as formata de acordo com o verbo print indicado na string de formatação.

### Package os
- Nos permite executar e usar recursos do SO

#### .Setenv()
- A função Setenv(key, value string) modifica o valor de uma variável de ambiente recebendo o nome e o valor a ser atribuido
- Retornará um erro caso encontre algum inconveniente 

#### .Getenv()
- A função Getenv(key string) nos permitirá acessar as variáveis de ambiente do sistema, passaremos a variável que queremos acessar como parâmetro e ela retornará seu valor

#### .LookupEnv()
- A função LookupEnv(key string) é equivalente à função Getenv() com a diferença de que retorna 2 valores:
  - o nome da variável de ambiente
  - um valor booleano mostrando se a variável existe ou não

#### .ReadDir()
- ReadDIR(name string) ([]DirEntry, error) lê o diretório nomeado, retornando todas as suas entradas de diretório ordenadas pelo nome do arquivo
- Se ocorrer um erro ao ler o diretório, ReadDir retornará as entradas que ele conseguiu ler antes do erro, juntamente com o erro.

#### .ReadFile()
- A função ReadFile(filename string) recebe como parâmetro o endereço e o nome do arquivo em formato texto e retorna o conteúdo do arquivo em bytes ou um erro se houver

#### .WriteFile()
- A função WriteFile(filename string, data []byte, permissao FileMode) recebe como parâmetro:
  - o endereço e nome do arquivo em formato texto
  - seu conteúdo em formato byte 
  - a permissão que queremos atribuir a ele
- retorna um erro se houver um 

### Package io
- Nos permite utilizar as funcionalidades primitivas de Entrada e Saída, como ler e gravar arquivos

#### io.Copy()
- A função io.COpy(det Writer, orig Reader) pega um leitor e copia os dados da origem para o destino
- Retorna o número de bytes copiados e o primeiro erro encontrado durante a cópia, se houver

#### WriteString()
- A função writeString(z Writer, s string) que recebe uma string e um Writer, escreve o conteúdo de s para w, que aceita um slice de bytes

## Módulo 2 - Introdução ao GO Bases - Aula 24 de maio (tarde)
- Compreender e utilizar ponteiros em Go
- Compreender e utilizar Go Routines
- Compreender e utilizar canais em Go

### Ponteiro
- É um tipo de dados cujo valor é um endereço de memória que se refere a (ou "aponta para") outro valor armazenado em outro lugar da memória
- Para criar um ponteiro usamos o operador * antes do tipo de dado que precisamos armazenar nesse endereço de memória
```shell
var p *int   // na variável p teremos um ponteiro para um valor do tipo de dado int
```
- Podemos criar um ponteiro também utilizando a função new() que recebe um tipo de dado como argumento
```shell
var p1 *int 
var p2 = new(int)
p3 := &p1
```
- o tipo de dado das variáveis p1, p2 e p3 é um ponteiro de tipo inteiro *int

#### Operador de endereço &
- Para obter a referência ou endereço de memória de uma variável devemos preceder a variável com o operador de endereço &

#### Operador de desreferenciação *
- Desreferenciar um ponteiro é obter o valor que está armazenado no endereço de memória onde o ponteiro se refere, para isso devemos colocar o operador * antes da variável ponteiro

#### * para criar variável do tipo pointeiro
#### * para visualizar o valor da posição da memória
#### & para atribuir um valor ao ponteiro

### Simultaneidade e Paralelismo
- A Simultaneidade é o ato de iniciar, executar e conclir duas ou mais tarefas em períodos de tempo escalonados
- O Paralelismo implica que duas ou mais tarefas sejam executadas exatamente ao mesmo tempo

### Go Routines
- Implementam a simultaneidade
- São gerenciadas pleo GO Runtime e seu agendador
- Quando executamos uma função como Go Routine, sua execução não bloqueará a continuação da função que a chamou, pois ela será executada simultaneamente com esta

### Canais
- Um canal nos permitirá enviar valores para as Go Routines e aguardar até recebermos esse valor
- Para definir um canal do tipo inteiro fazermos da seguinte forma

```shell
c := make(chan int)
```

## Módulo 2 — Introdução ao GO Bases — Aula 25 de maio (tarde)
- Conhecer o que é "panic" e como criar a sua estrutura
- Criar "panics"
- Conhecer casos de uso do "panic"
- Conhecer "defer" e "recover" e compreender a sua utilidade e funcinamento
- Implementar "defer" e "recover" para um melhor tratamento do "panic"
- Adquira um primeiro conhecimento introdutório sobre o pacote "context"

### Panic
- É uma interrupção da execução do nosso programa, com a indicação de que algo deu errado inesperadamente

### Defer e Recover
- Com as instruções internas 'defer' e 'recover' podemos controlar os efeitos de um panic e impedir que nosso programa termine involuntariamente
- Defer e Recover são funções projetadas para previnir ou controlar a natureza destrutiva de um panic

#### Defer
- É uma instrução incorporada no GO que nos permite adiar a execução de determinadas funções e garantir que sejam executadas antes da conclusão da execução de um programa

#### Recover
- É uma função integrada que permite interceptar um pânico e impedir que ele termine aexecução do programa de maneira inesperada ou indesejada

### Package Context
- Serve para definir um contexto que pode ser passado pelo código para que as diferentes partes decidam como reagir a ele

#### Context type
- É uma interface que define os métodos:

```shell
type Context interface {
  Deadline() (deadline time.Time, ok bool)
  Done() <- chan struct{}
  Err() error
  Value(key interface{}) interface{} 
}
```

É convenção ao definir uma função que recebe um contexto que ela seja o primeiro argumento e seja chamada de "ctx"

```shell
func funcaoComContexto(ctx context.Context, ...args) {
  ...
}
```

#### .Background()
- Nos permite criar um context vazio

#### .WithValue()
- A função .WithValue(ctx context.Context, key, val interface{}) recebe como argumentos um contexto pai e um par "chave -> valor"
- Retorna um novo contexto

#### .WithDeadline()
- A função .WithDealine(ctx context.Context, d time.Time) recebe como argumentos um contexto pai e uma data
- Retorna um novo contexto e uma função para cancelar manualmente o contexto
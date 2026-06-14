 Atividade Avaliativa 2 – CRUD de Nomes em Linguagem C

Disciplina

Laboratório de Programação
Curso: Engenharia da Computação – UFMA
Professor: Rondineli Seba Salomão

Integrantes

ARMANDDO FURTADO ROCHA (2022024002) 
MILENA MOTA ALVES (2022039918)
WERVERTON FERREIRA DA SILVA (2023080946)
Curso: Engenharia da Computação

Descrição do Projeto

Este projeto consiste no desenvolvimento de um sistema CRUD (Create, Read, Update e Delete) utilizando a linguagem C, com o objetivo de aplicar os conceitos estudados na disciplina até o conteúdo de matrizes.

O programa simula um pequeno banco de dados textual utilizando uma matriz de caracteres para armazenar nomes cadastrados pelo usuário.

---

Objetivos

* Utilizar variáveis, estruturas de decisão e repetição;
* Manipular vetores e matrizes;
* Trabalhar com funções da biblioteca `string.h`;
* Desenvolver lógica de busca, inserção, alteração e remoção de registros;
* Criar um sistema interativo baseado em menu.

---

Estrutura de Dados

O armazenamento dos registros é realizado por meio de uma matriz estática de caracteres:

```c
#define MAX_REGISTROS 50
#define MAX_LETRAS 30

char banco_dados[MAX_REGISTROS][MAX_LETRAS];
```

Onde:

* `MAX_REGISTROS` define a quantidade máxima de nomes armazenados.
* `MAX_LETRAS` define o tamanho máximo de cada nome.

---

Funcionalidades

1. Incluir Nome

Permite cadastrar um novo nome no sistema.

Regras:

* O nome não pode estar previamente cadastrado.
* O sistema realiza uma busca para verificar duplicidade.
* Caso o nome já exista, o usuário deve informar outro nome.
* O sistema procura a primeira posição livre para armazenar o novo registro.
* Caso a matriz esteja cheia, uma mensagem de erro é exibida.

---

2. Buscar Nome

Permite localizar um nome cadastrado.

Regras:

* O usuário informa o nome desejado.
* É realizada uma busca linear na matriz.
* Se encontrado, o sistema exibe o índice da posição.
* Caso contrário, exibe a mensagem:

```text
Nome não encontrado.
```

---

3. Modificar Nome

Permite alterar um registro existente.

Regras:

* O usuário informa o nome que deseja alterar.
* Caso o nome seja encontrado, o sistema solicita um novo nome.
* O novo nome também deve ser único.
* Se já existir outro registro com o mesmo nome, a alteração é cancelada.

---

4. Apagar Nome

Permite remover um registro.

Regras:

* O usuário informa o nome que deseja excluir.
* Caso seja encontrado, a posição é marcada como vazia.
* Uma posição vazia é identificada quando o primeiro caractere contém:

```c
'\0'
```

---

5. Listar Todos os Registros

Exibe todos os nomes cadastrados e seus respectivos índices.

### Exemplo:

```text
Índice 0 -> João
Índice 1 -> Maria
Índice 2 -> Pedro
```

---

Bibliotecas Utilizadas

```c
#include <stdio.h>
#include <string.h>
```

Funções permitidas da biblioteca `string.h`

* `strcmp()`
* `strcpy()`

---

Estrutura do Menu

```text
===== MENU =====

1 - Incluir Nome
2 - Buscar Nome
3 - Modificar Nome
4 - Apagar Nome
5 - Listar Todos
0 - Sair

Escolha uma opção:
```

---

Como Compilar

Utilizando o GCC:

```bash
gcc atividade2.c -o atividade2
```

---

Como Executar

Linux/Mac:

```bash
./atividade2
```

Windows:

```bash
atividade2.exe
```

---

Conceitos Aplicados

* Variáveis
* Entrada e saída de dados
* Estruturas condicionais
* Estruturas de repetição
* Vetores
* Matrizes
* Manipulação de strings
* Busca linear
* CRUD básico

---

Informações da Atividade

Trabalho desenvolvido para a **Atividade Avaliativa 2** da disciplina **Laboratório de Programação**, ministrada pelo professor **Rondineli Seba Salomão**, no curso de Engenharia da Computação da Universidade Federal do Maranhão (UFMA).

---

# 📄 Licença

Projeto desenvolvido exclusivamente para fins acadêmicos.

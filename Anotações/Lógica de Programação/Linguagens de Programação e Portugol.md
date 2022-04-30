# LINGUAGENS DE PROGRAMAÇÃO E PORTUGOL

#### Linguagem de programação

* É uma linguagem escrita e formal que específica um conjunto de  instruções e regras usadas para gerar programas (software). Um software  pode ser desenvolvido para rodar em um computador, dispositivo móvel ou  em qualquer equipamento que permita sua execução.

* O que é óbvio para você, certamente não é óbvio para uma máquina. E se  você quer que a máquina faça algo, você precisa "falar com ela".

* A função das linguagens de programação é servir de um meio de comunicação entre computadores e humanos.

**Alto nível e Baixo nível**

* Alto nível são aquelas cuja sintaxe se aproxima mais da nossa linguagem e se distanciam mais para a linguagem de máquina (Ex: C, PhP, C++,  Python, etc).

* Baixo nível é a que se aproxima  mais da linguagem de máquina. Essas são as que vocês precisa ter o  conhecimento direto da arquitetura do computador para fazer alguma  coisa. (Ex: semble).

**Compiladas ou interpretadas** 

* Compilada é uma linguagem de programação em que o código fonte, é  executado diretamente pelo sistema operacional ou pelo processador, após ser traduzido por meio de um processo chamado compilação. (ex: Csharp,  Visual Basic, Delf, C++)

* Interpretada é uma  linguagem de programação em que o código fonte é executado por um  programa de computador chamado interpretador, que em seguida é executado pelo sistema operacional ou processador. (JavaScript, PhP, Python)

**Portugol**

* É uma pseudolinguagem que permite ao leitor desenvolver algoritmos  estruturados em português de forma simples e intuitiva, independente de  linguagem de programação.

* Permite ao programador pensar no problema em si e não no equipamento que irá executar o algoritmo. 



#### DESVIO CONFICIONAL "SE"

**se**

* É utilizada a palavra reservada "se", a condição a ser testada entre  parênteses e as instruções que devem ser executadas entre chaves caso o  desvio seja verdadeiro.

**Ex:**

se(média>=7){

​      Escreva("Parabéns!! Você foi aprovado")

 }

• quebra de linha: ("\n" + ...)

**se-senao**

Agora vamos imaginar que se a condição for falsa um outro conjunto de  comandos deve ser executado. Quando iremos encontrar essa situação?

**Ex:**

se(média>=7) {

   escreva("parabéns!! Você foi aprovado!!")

}

senao {

​    escreva("Infelizmente você foi reprovado")

}

**DESVIO CONDICIONAL - caso**

* Este comando é similar aos comandos "se" e "senão", e reduz a complexidade  na escolha de diversas opções. Apesar de suas similaridades com o "se",  ele possui algumas diferenças. Neste comando não é possível o uso de  operadores lógicos, ele apenas trabalha com valores definidos.

**Exemplo:**

Inteiro valor=0

escolha(valor)

{ 

caso 1:           //Testa se o valor é igual a 1

escreva("OK!! Abrir Netflix")

pare

caso 2:           //Testa se o valor é igual a 2

escreva("OK!! Abrir Amazon Prime")

pare

caso 3:           //Testa se o valor é igual a 3

escreva("OK!! Abrir HBO GO")

pare

caso contrario: 

escreva("Você deve escolher as opções 1, 2 ou 3")

}



#### LAÇOS DE REPETIÇÃO

* Dentro da lógica de programação é uma estrutura que permite executar mais de  uma vez o mesmo comando ou conjunto de comandos, de acordo com uma  condição ou com um contador.



#### VETORES E MATRIZES

* Matriz

\- É uma coleção de variáveis de mesmo tipo, acessíveis com um único nome e armazenados continuamente na memória.

\- A individualização de cada variável de um vetor é feita através do uso de índices.

* Vetores

Os Vetores são matrizes de uma só dimensão.

Ex

cadeia Vetor[5];.  //Declara um vetor de 5 posições 

cadeia Matriz[5][3];.  // declara uma matriz de 5 linhas e 3 colunas

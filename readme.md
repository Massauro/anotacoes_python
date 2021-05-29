# Anotações de Python - by Mezaki Massaru Hagio 27/05/2021

Esse aquivo tem o objetivo de armazenar todo conhecimento obtido referente a linguagem de programação Python, já que **Massaru** e uma ‘anta’ e esquece tudo! Bom proveito!

*OBS: Após a instalação do Python mais recente em um sistema Linux. Executar comandos abaixo no terminal.*

```sh
cd /opt
sudo wget https://bootstrap.pypa.io/get-pip.py
python3 get-pip.py
```

Esses comandos servem para instalação do PIP, gerenciador de extensões do Python. O último comando deve ser executado com compilador mais recente. ***EXEMPLO:***
```sh
	python3.9 get-pip.py
```

## Caracteres de escape

```

\' - aspas simples

\" - aspas duplas

\n - quebra de linha

\r - como pressionado enter

\t - tabulação / Organiza texto em tabela (como pressionar 'tab')

\b - backspace (como pressionar 'backspace)

```

## Operadores aritméticos:

x + y = Soma

x - y = Subtração

x * y = Multiplicação 

x ** y = Potencia

x / y = Divisão

x // y = Divisão Inteira

x % y = Módulo (resto da divisão)

x ** (1/y) = Raiz

### Ordem de precedência:

1. ()
2. **
3. *, /, //, %
4. +, -

## Funções iniciais

* **print(‘texto ou variável’)** - Escreve na tela (ou console)

***OBS:*** se usar parâmetro “end=alguma_coisa” mantêm todo o resultado na mesma linha EX: print(‘ola’, end=’‘)

* **input(‘texto ou variável’)** - Pede um valor ou conjunto de caracteres a ser digitado

* **type(‘texto ou variável’)** – verifica o tipo de informação.

* **pow(‘base’,’expoente’)** – Potencia

* **len(‘valor ou string’)** – verificar e retornar a quantidades de caracteres ou elementos do mesmo.


## Funções de ‘casting’ - Corversão
* `int(‘texto ou variável’)` - Converte valor dentro de parênteses em inteiro

* `float(‘texto ou variável’)` - Converte valor dentro de parênteses em float ou ponto flutuante (numero real)

* `str(‘texto ou variável’)` - Converte valor dentro de parênteses em string ou conjunto de caracteres (‘palavras entendíveis’)


## Funções de verificação -  ‘verifica se os dados da variável(qualquercoisa) é…’

* `qualquercoisa.isnumeric()` - é numérico

* `qualquercoisa.isalpha()` - é alfabético

* `qualquercoisa.isalnum()` - é alfabético e numérico

* `qualquercoisa.isupper()` - é tudo em maiúsculo

* `qualquercoisa.islower()` - é tudo em minúsculo

* `qualquercoisa.isspace()` - é composta por espaços

***OBS:*** Essas funções retornam valores boorlean (True ou False)
qualquercoisa.istitle() - contem maiúsculas e minúsculas

## Funções de manipulação de texto

* `frase[indice]` - indica a fosição de um caracter **EX:**
```python
frase[9]
```

* `frase[inicio:fim]` - Indica uma cadeia de caracteres. Mas não inclui o ultimo valor.
```python
frase[0:9]
```

* `frase[inicio:fim:intervalo]` - Indica uma cadeia de caracteres com intervalo entre o mesmo.
```python
frase[0:9:2]
```

OBS: `frase[0:]` → Omitindo valor de **inicio** e/ou de **fim** estará deixando a critério da sistema escolher um valor padrão, que normalmente é o tamanho total do mesmo.

OBS2: `frase[::-1]` → Inverte os elementos

OBS3: Lembrando que toda `string` pode ser como uma lista de caracteres, sendo assim todas essas funções de manipulação podem ser feitas em uma `list` e `tuple`.

## Importação de biblioteca ‘Math’ - Lista de funções

	* `import math` – importando biblioteca math (import = importar / math = biblioteca)

	* `math.trunc(valor)` – corta a parte inteira
 
	* `math.hypot(valor)` – calculo de hipotenusa

	* `math.radians(valor)` – calcula de radiano

	* `math.cos(valor_em_radiano)` – calculo de cosseno

## Importação da biblioteca 'random' - Lista de funções

* `import random` - biblioteca para randomização

* `random.choice(lista)` - randomiza uma lista

* `random.seed()` - Inicia a semente dos números pseudo randômicos

* `random.randrange(inicio,final,contagem)` - sorte-a valor **EX**: `random.randrange(0,9,2)` = sorte-a de 2 em 2 números de 0 a 9.

* `random.randrang(inicio,final)` - sorte-a a faixa de inteiro

* `random.uniform(inicio,final)` - sorte-a uma faixa de ponto flutuante (float)



## Concatenação de valores na função ‘print()’

* `print(‘qualquercoisa’ + valor1 + ‘ e ’ + valor2)` – Esse é um exemplo de concatenação de valores que usamos para apresentar valores mesclados por diversos motivos. Mas nem sempre é o mais eficaz ou o mais apropriado. Os valores devem ser todos do mesmo tipo, sendo que os valores das variáveis ‘valor1’ e ‘valor2’ devem seguir o mesmo tipo das strings ‘qualquecoisa’ e ‘ e ’, caso tenha algum valor diferente haveria um erro ***‘TypeError: can only concatenate str (not "tipoDaVariavel") to str’*** .

* `print(‘qualquercoisa {} {}’.format(valor1, valor2))` – Esse exemplo e usando a função ‘.format()’. A string ‘qualquercoisa {} {}’ tem duas caves dentro que serão substituídos pelos valores das variáveis ‘valor1’ e ‘valor2’ que foram atribuídas como parâmetros da função. A ordem segue a atribuição da esquerda para direita serando cada parâmetro por vírgula. Exemplo: ‘`qualquercoisa {valor1} {valor2}’.format(valor1, valor2)` Esse tipo de concatenação era muito utilizado antigamente, mas hoje temos uma maneira mais simples de fazer esse tipo de operação. OBS: Os valores não precisam ser convertidos (casting).

* `print(f‘qualquercoisa {valor1} {valor2}’)` – Esse exemplo e utilizando carácter ‘f’ antes da string e colocando ‘{}’ onde que adicionar os valores a serem inseridos. Essa forma é a mais utilizada e também mais simples.

## Controlando casas decimais

```

‘{:.2f}’ - Dentro das chaves podemos controlar casas decimais. Principalmente utilizado em dados no tipo ‘float’.
Vamos entender:

	{ : = ^ 40 }

		‘:’ - Início da sintaxe

		‘=’ - Carácter para repetição

		‘^’ - Formatação ( ^ - centralizado / > - alinhado à direita / < - alinhado à esquerda)

		‘40’ – Número de repetições

```

## Anotações em andamento...
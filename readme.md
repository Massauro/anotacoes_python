# Anotações de Python - by Mezaki Massaru Hagio 27/05/2021

Esse aquivo tem o objetivo de armazenar todo conhecimento obtido referente a linguagem de programação Python, já que **Massaru** e uma ‘anta’ e esquece tudo! Bom proveito!

**OBS: Após a instalação do Python mais recente em um sistema Linux. Executar comandos abaixo no terminal.**

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

* **time.sleep(valor_em_segundos)** - Função de tempo Python sleep() para adiar o segmento de chamada estiver em execução, você pode consultar o número de segundos por segundos parâmetros, ela representa o processo na pendência do tempo. OBS: `print("txt",`**flush=True**`)` resolve bug que faz sleep não funcionar.

* **range(inicio,fim,intervalo)** - cria uma lista de contagem numérica. OBS: `range(10,-1,-1)` faz contagem regressiva.

## Funções de ‘casting’ - Corversão
* `int(‘texto ou variável’)` - Converte valor dentro de parênteses em inteiro

* `float(‘texto ou variável’)` - Converte valor dentro de parênteses em float ou ponto flutuante (numero real)

* `str(‘texto ou variável’)` - Converte valor dentro de parênteses em string ou conjunto de caracteres (‘palavras entendíveis’)

### conversão de numeros

* `bin(numero)` → converter numero em binário

* `oct(numero)` → converter numero em octal

* `hex(numero)` → converter numero em hexadecimal


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

* `frase[indice]` - indica a posição de um carácter **EX:**
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

## Funções para analise

* `frase.count(parâmetro_de_pesquisa, inicio_intervalo, fim_intervalo)` = conta o numero de vezes que o `parâmetro de pesquisa` se repete.

* `frase.find('deo')` - Realiza a pesquisa em `frase` o parâmetro `deo` e indica o índice no qual começa o mesmo. OBS: Se a `string` não existe em `frase` ira retornar -1. OBS2: `frase.rfind()` e a mesma coisa mas realiza a pesquisa ao contrario.

* `frase.index(valor_procurado, valor_deslocamento)` - Diz em qual posição se encontra o valor. 

## Funções para transformação

* `frase.center(quantidade_de_caracteres)` - Deixar `frase` centralizado.

* `frase.replace(valor_substituição, valor_substituído)` - Substituir os parâmetros em `frase`.

* `frase.upper()` - Deixar tudo maiúsculo.

* `frase.lower()` - Deixar tudo em minusculo.

* `frase.capitalize()` - Deixa tudo minusculo menos a primeira letra.

* `frase.title()` - Separa as palavras e deixa a primeira letra em maiúsculo.

* `frase.strip()` - Remove espaços inúteis no começo e no final da string. OBS: `frase.rstrip()` e `frase.lstrip()` faz a mesma coisa em um dos lados sendo `rstrip` é direita e `lstrip` é esquerda.

## Funções para divisão e junção

* `frase.split(separador, máximo)` - Dividir as palavras usando `separador` como critério de separação e colocando em um lista.

* `"criterio_de_junção".join(frase)` - Junta a lista separando pelo `"critério_de_junção`. **Ex:**

```python
teste = ['frase' ,'para' ,'teste']
' '.join(teste)
#resultado será 'teste = 'frase para teste'
```



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

* `random.shuffle(string_ou_lista)` - embaralha `string_ou_lista`

* `sorted(string_ou_lista)` - organiza `string_ou_lista` sendo numeradores em ordem crescente e letras em ordem alfabética. OBS: existem parametros extras como `key = lista_palavras_para_ordenar` e `reverse = True` que inverte a ordem.



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

## O Módulo datetime em Python

* `datetime.date` – Usada para representar apenas datas simples, com ano, mês e dia, sem informação de fuso horário.

* `datetime.time` – Representa uma versão idealizada do tempo, onde cada dia sempre tem 86.400 segundos, no formato hora, minuto, segundo e microssegundo, além do fuso horário.

* `datetime.datetime` – Combina os valores das classes date e time em um objeto só. Cuidado para não fazer confusão com o nome do módulo, que é o mesmo da classe.

* `datetime.timedelta` – Usada em cálculos para expressar a diferença em dias entre dois objetos do tipo date, time ou datetime, com precisão de microssegundos.

* `datetime.timezone` – É a implementação concreta de datetime.tzinfo, que contém a informação do fuso horário como um deslocamento fixo a partir do horário UTC. Como você viu, essa forma de representação fixa não ajuda muito quando você precisa lidar com mudanças no fuso horário, ou com o horário de verão.
Você pode criar instâncias de objetos do tipo date, time ou datetime passando argumentos como dia, mês, ano, hora, minuto e segundo.

Para combinar objetos date e time em um só objeto do tipo datetime, use o método `datetime.combine()`.

```python
dataSimples = date(year=2020, month=9, day=24)
print(dataSimples)
#  2020-09-24

hora = time(hour=22, minute=10, second=30)
print(hora)
#  22:10:30

data = datetime(year=2020, month=9, day=24, hour=22, minute=10, second=30)
print(data)
#  2020-09-24 22:10:30
dataCompleta = datetime.combine(dataSimples, hora)
print(dataCompleta)
#  2020-09-24 22:10:30
Code language: Python (python)
```

Você pode omitir os nomes dos parâmetros, mas isso torna o seu código mais difícil de ler.

```python
data = datetime(2020, 9, 24, 22, 10, 30)
print(data)
#  2020-09-24 22:10:30
Code language: Python (python)
```

Além disso, também é possível criar objetos date e datetime usando métodos úteis como today() e now(), ou a partir de um timestamp, ou seja, o inteiro que representa o número de segundos desde o início da Era Unix.

```python
data = date.today()
print(data)
#  2020-09-25

data = datetime.now()
print(data)
#  2020-09-25 21:18:06.694389

timestamp = 1600995600
data = datetime.fromtimestamp(timestamp)
print(data)
#  2020-09-24 22:00:00
```

PS: Mais informações sobre datas em python, acesse <https://vaiprogramar.com/como-trabalhar-com-data-hora-python-datetime/> pois as informações desse paragrafo **'O Módulo datetime em Python'** foram tiradas de lá.

## Estruturas de repetição

### Estrutura 'For'

```python
for variavel_armazenha_valor in range(0,3):
	print(alguma_coisa)
# Estruta de repetição com limite

```

### Estrutura 'While'

```python
while condicao:
	print(alguma_coisa)
# Estrutura de repetição limitada por uma condição

while True:
	break
# Estrutura de repetição limitada por uma função 'break'

```

### Funções logicas e uteis

* `break` - para estrutura de repetição

* `continue` - para o laço mas continua a estrutura

* `in` - está / Ex:`x in y`

* `not in` - não esta / Ex:`x not in Y`

* `or` - ou / Ex:`condicao or condicao`

* `and` - & / Ex:`condicao and condicao`

### Calculos por ele mesmo

```python

a -= b # a = a - b
a += b # a = a + b
a /= b # a = a / b
a *= b # a = a * b
a **= b # a = a ** b


```

## Anotações em andamento...
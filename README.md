<h1>TUPLAS</h1>

<h2>_EM HASKELL_</h2>
<h4>DEFINIÇÃO:</h4>
Em Haskell, uma tupla é um “mecanismo” para construir dados compostos. Isto é, uma forma de combinar os componentes de um dado em uma estrutura só, podendo eles serem de tipos diferentes.

<h4>SINTAXE:</h4>
<ul>
  <li>Entre parênteses, com seus componentes separados por vírgula:</li>

```haskell
(elemento1, elemento2, elemento3, elementoN)
```

  <li>Também podemos escrever dessa forma um pouco incomum:</li>

```haskell
(,) elemento1 elemento2
```

  <li>Sintaxe de tupla de tipos segue o mesmo padrão da primeira imagem de sintaxe:</li>

```haskell
(Int, Int, Float, String, Int)
```
</ul>

<h4>ESPECIFICANDO:</h4>
<ul>
  <li>Sequência finita de n elementos: tem um tamanho/número fixo de elementos que a compõe;</li>
  <li>Estrutura estática: após criá-la, não é possível modificá-la. Boa para dados que devem ser imutáveis;</li>
  <li>Heterogênea: contém um ou mais tipos diferentes;</li>
  <li>Elementos representados na ordem dada, podendo ter o mesmo elemento mais de uma vez;</li>

```haskell
--TUPLAS COM n ELEMENTOS:

--Tupla-2/Pairs:
(87669544, "Nome completo")

--Tupla-3/Triples:
(87669544, "Nome completo", 'M')

--Tupla-5:
(87669544, "Nome completo", 'M', "dd/mm/aaaa", 1.71)
```

<li>Não há limite para os tipos que são associados as tuplas, ex: uma tupla de tupla;</li>
</ul>

```haskell
--Exemplos de tuplas:

([Int], String, (Char, Int))
([1, 2, 3], "hello", ('A'), 65))

(Int, (Int, (Int, Int,), Int), Int)
(1, (2, (3, 4), 5), 6)
```

<h4>OBSERVAÇÕES:</h4>
<ul>
  <li>Tuplas com apenas um componente não tem sentido;</li>
  <li>Tipos Unit podem ser entendidos como Tuplas-0, pois sua escrita é ();</li>
  <li>Não há funções pré-definidas para tuplas de mais de 2 elementos, mas podemos criar nossas próprias;</li>
  <li>Mas há também libraries e packages de tuplas que podem ser usadas, como as do site <a href="hackage.haskell.org">hackage.haskell.org</a>:</li>
  
  <a href="https://hackage.haskell.org/package/tuple">Package/tuple</a>
  
  <a href="https://hackage.haskell.org/package/tuple-0.3.0.2/docs/Data-Tuple-Select.html">Data.Tuple.Select</a>
  
  <a href="https://github.com/augustss/tuple">GitHub</a>

  
  <li>*Em certos casos, talvez seja melhor optar por criar um tipo de dado do que usar tuplas.</li>
</ul>

<h4>USO:</h4> Tem uso para os casos de que se deseja definir uma função ao qual recebe ou retorna mais de um valor, sendo normalmente de tipos heterogêneos. É interessante para coordenadas, parâmetros conectores de base de dados e chave de dicionários.
No Caso abaixo, a função verIdade recebe uma tupla de dois elementos de diferentes e retorna apenas a idade:

```haskell
type Nome = String    --Sinônimo para String(Nome)
type Idade = Int      --Sinônimo para Int(Idade)

verIdade :: (Nome,Idade) -> Idade   --Função que se passa uma tupla
verIdade (a,b) = b                  --(Nome, Idade), e devolve a idade

```

<h4>FUNÇÕES RELACIONADAS:</h4>
<h6>De Prelude ou Data.Tuple:</h6>
<ul>
  <li><b>FST:</b>
    Retorna o primeiro valor de uma tupla-2;</li>
  
  ```haskell
fst (1,2)  --retorna 1
  ```
  <li><b>SND:</b>
    Retorna o segundo valor de uma tupla-2;</li>

```haskell
snd (1,2)  --retorna 2
```
  
*As duas acima podem ser usadas combinadas juntas ou com outras funções:

```haskell
snd (fst ((True,4), "Bom) )  --retorna 4
map fst [(1,2), (3,4), (5,6)]    --retorna [1,3,5]
```

<li><b>CURRY:</b> converte uma função que recebe tuplas em uma que recebe 2 argumentos:</li>
<img width="371" height="151" alt="Image" src="https://github.com/user-attachments/assets/bf3f48a8-f1e5-4402-a7c3-68e8ac60a391" />
<li><b>UNCURRY:</b> converte função de argumentos em função de tuplas</li>
<img width="524" height="226" alt="Image" src="https://github.com/user-attachments/assets/9adafc45-c131-4fd1-84ed-979c2db62893" />
<li><b>ZIP:</b> transforma duas listas em uma lista de tuplas:</li>
<img width="345" height="85" alt="Image" src="https://github.com/user-attachments/assets/66bb1f0d-23c7-448a-affb-e47635041418" />
<li><b>SWAP:</b> troca os elementos de um par:</li>
<img width="272" height="59" alt="Image" src="https://github.com/user-attachments/assets/430097f2-926f-4f7e-9b9d-a5a67851b539" /> ou: <img width="432" height="37" alt="Image" src="https://github.com/user-attachments/assets/ed83e989-d0bb-4879-b377-93cb7c808b94" />
<li><b>*Pattern Matching:</b></li> Usa os construtores da tupla. Pode-se usar esse método para tuplas maiores:
<img width="492" height="148" alt="Image" src="https://github.com/user-attachments/assets/1e754329-7b3e-4c69-8ad5-665a0cf341b5" />
</ul>

<h4>OUTROS EXEMPLOS E PROGRAMAS COM TUPLAS</h4>

<h5>Ex1:</h5>
<img width="284" height="266" alt="Image" src="https://github.com/user-attachments/assets/e78538fc-c53f-40e2-a8b3-6712301e6fae" />
<h5>Ex2:</h5>
<img width="230" height="91" alt="Image" src="https://github.com/user-attachments/assets/2ff15d4a-210b-4f13-9e3b-d9dc21f61038" />
<img width="527" height="77" alt="Image" src="https://github.com/user-attachments/assets/8a91ec80-b1ca-46c2-b096-e1ed91f42b72" />
<h5>Ex3:</h5>
<img width="678" height="388" alt="Image" src="https://github.com/user-attachments/assets/0d2c1244-7dd5-4a46-a321-f4d9a73f484b" />


<h2>_EM OUTRAS LINGUAGENS_</h2>

Podemos encontrar tuplas em outras linguagens, como em Python, C++, SQL, Rust, etc. Vejamos:

<h3><b>PYTHON</b></h3>
<ul>
  <li>Sua definição é assim como a em Haskell e as demais. Também podem vir a serem chamadas de containers ou collections, e em alguns casos, a escrita da tupla pode ser da forma convencional, ou a sem parênteses:</li>

```python
#SINTAXE:
tupla = (1, 2, 3)
#OU
tupla = 1, 2, 3
```
<li>Elementos dentro de uma tupla são acessados usando indexação:</li>

```python
#INDEXAÇÃO DE ELEMENTOS:

#Primeiro:  tupla[O]
#Segundo:  tupla[1]
#...
#Penúltimo:  tupla[-2]
#Últimpo:  tupla[-1]
```
*Tentar acessar um índice inexistente na tupla, obviamente, gerará um erro.
 <li>Um elemento solitário precisa ser definido da seguinte forma para ser diferenciado de um valor comum:</li>

```python
apenasUm = (7,)
```
<li>Uma tupla vazia é representada da seguinte forma:</li>

```python
empty = ()
#()
```
<li>Usando com strings:</li>

```python
#Forma correta
"Hello, %s! You're %s years old." % ("Linda, 24)
'Hello, Linda! You're 24 years old'

#Forma incorreta:
"Hello, %s! You're %s years old." % "Linda, 24
Traceback (most recent call last):
  ...
TypeError: not enough arguments for format string
```

<h4>FUNÇÕES:</h4>

<li><b>SLICING:</b> extrair uma faixa de elementos da tupla usando: tuple[start:end:step]</li>
```
start: inclusivo; end: exclusivo; step/stride: especifica o incremento entre componentes.
```

<b>Ex1:</b>

<img width="604" height="96" alt="image" src="https://github.com/user-attachments/assets/6c99bf9a-e6e7-40f5-89a4-0274b8de5364" />


<b>Ex2:</b>

<img width="603" height="94" alt="image" src="https://github.com/user-attachments/assets/1e644609-70e6-417d-807a-6b5e0ef10010" />


<b>Ex3:</b>

<img width="611" height="104" alt="image" src="https://github.com/user-attachments/assets/7b68824c-4c20-4b23-99f5-f4af6ef851ad" />

<li><b>CONCATENAÇÃO:</b> concatena duas tuplas</li>
<img width="247" height="101" alt="image" src="https://github.com/user-attachments/assets/9ffbb391-f731-4a99-aa61-b0f9feb7ff94" />

<li><b>REPETIÇÃO:</b> repete a tupla n vezes</li>
<img width="219" height="99" alt="image" src="https://github.com/user-attachments/assets/1c76d91b-c3fe-443b-b5ff-af613c12ec43" />

<li><b>LEN:</b> acha o número de elementos em uma tupla.</li>
<img width="606" height="100" alt="image" src="https://github.com/user-attachments/assets/678a05fa-5646-4ca2-9917-21aedf26838e" />

<li><b>ZIP:</b></li>
<img width="560" height="165" alt="image" src="https://github.com/user-attachments/assets/b2f0158f-c374-4af1-ab07-eedb285693e5" />

<h3><b>C++</b></h3>

  <li><b>Criar uma tupla</b></li>

```c++
#include <tuple>
#include <iostream>

using namespace std;

int main()
{
    tuple<int, bool, string> t1 {7, false, "Beleza?"};
    // CTAD - Class template argument deduction
    tuple t2 {8, true, "CTAD"s};
    cout << "t1 = (" << get<0>(t1) << ", " << get<1>(t1) << ", " << get<2>(t1) << ")" << endl;
    cout << "t2 = (" << get<0>(t2) << ", " << get<1>(t2) << ", " << get<2>(t2) << ")" << endl;
}

/*SAÍDA
t1=(7, 0, Beleza?)
t2 = (8, 1, CTAD)
*/
```

  <li><b>Tipo de um elemento</b></li>

```c++
#include <tuple>
#include <iostream>

using namespace std;

int main()
{
    tuple<int, bool, string> t1 {7, false, "Beleza?"};
    
    cout << "Tipo do primeiro elemento de t1: " << typeid(get<0>(t1)).name() << endl;
    cout << "Tipo do segundo elemento de t1: " << typeid(tuple_element<1, decltype(t1)>::type).name() << endl;
    cout << "Tipo do terceiro elemento de t1: " << typeid(tuple_element<2, decltype(t1)>::type).name() << endl;
}

/*SAÍDA
Tipo do primeiro elemento de t1: i
Tipo do segundo elemento de t1: b
Tipo do terceiro elemento de t1: NSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE
*/
```


  <li><b>Tamanho de uma tupla std::tuple_size</b></li>

```c++
#include <tuple>
#include <iostream>

using namespace std;

int main()
{
    tuple<char, double, string> t1 {'a', 10.5, "Beleza?"};
    
    cout << "Tamanho da tupla t1: " << tuple_size<decltype(t1)>::value << endl;
    cout << "Tamanho da tupla t1: " << tuple_size<tuple<char, double, string>>::value << endl;
}
/*SAÍDA
Tamanho da tupla t1: 3
Tamanho da tupla t1: 3
*/
```


 <h3><b>SQL</b></h3>
 
As tables em SQL também são basicamente sets de tuplas, podendo usar colunas de tuplas ou tuplas de valores constantes.

```SQL
--ex1:
INSERT (id, nome, idade, salario) VALUES (1, "joão", 25, 1000.00);

--ex2:
SELECT * FROM sometable
WHERE (col1, col2, col3) = (1, 2, "abc");
```


 <h3><b>RUST</b></h3>
 
```rust
// Declare tuple
let tupleName: (i32, bool) = (0, false);

// Types can be inferred
let tupleName = (0, false);

// Deconstructive assignment
let (value, value2) = tupleName; // value/value2 now hold the tuple's first/second value
```


 <h2><b>_GHCI_</b></h2>
 
<li><h4><b>Exemplo 1: Converter real para dólar e euro</b></h4></li>

![Ex1](https://github.com/user-attachments/assets/aebeebd2-45fe-4887-b2d6-b411ad80555b)

```haskell
--valores das moedas no dia 26/08/2025
converter real = (real, real*5.41, real*6.29)
```

<li><h4><b>Exemplo 2: Informações de um livro</b></h4></li>

![Ex2](https://github.com/user-attachments/assets/1f4dfec1-1ef8-4ad9-85cf-07092c11c6aa)

```haskell
type Livro = (String, String, Int)
l1::Livro = ("", "", ) --dê um nome para sua variável e adicione os dados da tupla
```

<li><h4><b>Exemplo 3: Filtra os resultados maiores que 2</b></h4></li>

![Ex3](https://github.com/user-attachments/assets/70fab18d-81dc-4de2-81ba-b77dc7b1df35)
</ul>

```haskell
maior x = x>2
filter maior (map (uncurry (+))) [(,), (,), (,), (,), (,)]) --complete como quiser
```


<h2><b>_FONTES_</b></h2>

https://www.facom.ufu.br/~madriana/PF/Haskell3.pdf

https://www.inf.ufpr.br/andrey/ci062/ProgramacaoHaskell.pdf

https://aterribili.blogspot.com/2014/01/haskell-apresentando-tuplas.html

https://haskell.tailorfontela.com.br/syntax-in-functions

https://wiki.haskell.org/Haskell_em_10_minutos

https://devtut.github.io/haskell/tuples-pairs-triples.html#pattern-match-on-tuples

https://www.quora.com/Is-Python-the-only-programming-language-that-uses-the-concept-of-a-tuple

https://www.quora.com/Which-programming-languages-have-tuples

https://haskell.pesquisa.ufabc.edu.br/haskell/03.haskell.basico.1/

https://www.facom.ufu.br/~madriana/PF/pratica01.pdf

https://realpython.com/python-tuple/#getting-started-with-pythons-tuple-data-type

https://www.dataquest.io/blog/python-tuples/

https://github.com/Malpaux/programming-cheat-sheets/blob/master/rust.md#data-structures

https://cppmoderno.com/o-que-e-tupla-em-cpp/

https://pt.stackoverflow.com/questions/164164/tuplas-em-banco-de-dados

https://books.google.com.au/books?id=6yupzA8JZjQC&pg=PA390&lpg=PA390&dq=touch%20of%20class%20tuples&source=bl&ots=dqDA9wcvlw&sig=ACfU3U01q8096Fi3d1z7kQq1YtqFVBpWjQ&hl=en&sa=X&ved=2ahUKEwiD4Zq0p5jiAhWTjeYKHY_gBDkQ6AEwAHoECAkQAQ#v=onepage&q=tuple&f=false

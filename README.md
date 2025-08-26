# Apresentacao-bim1-2025b-HLKellermann
<h1>TUPLAS</h1>

<h2>_EM HASKELL_</h2>
<h4>DEFINIÇÃO:</h4>
Em Haskell, uma tupla é um “mecanismo” para construir dados compostos. Isto é, uma forma de combinar os componentes de um dado em uma estrutura só, podendo eles serem de tipos diferentes.

<h4>SINTAXE:</h4>
<ul>
  <li>Entre parênteses, com seus componentes separados por vírgula:</li>

```
(elemento1, elemento2, elemento3, elementoN)
```

  <li>Também podemos escrever dessa forma um pouco incomum:</li>

```
(,) elemento1 elemento2
```

  <li>Sintaxe de tupla de tipos segue o mesmo padrão da primeira imagem de sintaxe:</li>

```
(Int, Int, Float, String, Int)
```
</ul>

<h4>ESPECIFICANDO:</h4>
<ul>
  <li>Sequência finita de n elementos: tem um tamanho/número fixo de elementos que a compõe;</li>
  <li>Estrutura estática: após criá-la, não é possível modificá-la. Boa para dados que devem ser imutáveis;</li>
  <li>Heterogênea: contém um ou mais tipos diferentes;</li>
  <li>Elementos representados na ordem dada, podendo ter o mesmo elemento mais de uma vez;</li>

```
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

```
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

```
type Nome = String    --Sinônimo para String(Nome)
type Idade = Int      --Sinônimo para Int(Idade)

verIdade :: (Nome,Idade) -> Idade   --Função que se passa uma tupla
verIdade (a,b) = b                  --(Nome, Idade), e devolve a idade

```

<h4>FUNÇÕES RELACIONADAS:</h4>
<h6>De Prelude ou Data.Tuple:</h6>
<ul>
  <li><b>Função fst:</b>
    Retorna o primeiro valor de uma tupla-2;</li>
  
  ```
fst (1,2)  --retorna 1
  ```
  <li><b>Função snd:</b>
    Retorna o segundo valor de uma tupla-2;</li>

```
snd (1,2)  --retorna 2
```
  
*As duas acima podem ser usadas combinadas juntas ou com outras funções:

```
snd (fst ((True,4), "Bom) )  --retorna 4
map fst [(1,2)(3,4)(5,6)]    --retorna [1,3,5]
```

<li><b>Pattern Matching:</b></li> Usa os construtores da tupla. Pode-se usar esse método para tuplas maiores:

<li><b>Função curry:</b> converte uma função que recebe tuplas em uma que recebe 2 argumentos:</li>

<li><b>Função uncurry:</b> converte função de argumentos em função de tuplas</li>

<li><b>Função zip:</b> transforma duas listas em uma lista de tuplas:</li>

<li><b>Função swap:</b> troca os elementos de um par:</li>
</ul>
ou:

<h4>OUTROS EXEMPLOS E PROGRAMAS COM TUPLAS</h4>

<h5>Ex1:</h5>

<h5>Ex2:</h5>

<h5>Ex3:</h5>




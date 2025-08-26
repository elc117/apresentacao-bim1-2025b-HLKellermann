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
</ul>

```
--TUPLAS COM n ELEMENTOS:

--Tupla-2/Pairs:
(87669544, "Nome completo")

--Tupla-3/Triples:
(87669544, "Nome completo", 'M')

--Tupla-5:
(87669544, "Nome completo", 'M', "dd/mm/aaaa", 1.71)
```

<h4>OBSERVAÇÕES:</h4>
-Não há limite para os tipos que são associados as tuplas, ex: uma tupla de tupla;

      Exemplo com tupla de valores definidos		    Exemplo com tupla de tipos

-Haskell não suporta tuplas com apenas um componente;
-Tipos Unit podem ser entendido como Tuplas-0, pois sua escrita é ();
-Não há funções pré-definidas para tuplas de mais de 2 elementos, mas podemos criar;
-Mas também, pode-se usar libraries e packages de tuplas, como as a seguir:  https://hackage.haskell.org/package/tuple
https://hackage.haskell.org/package/tuple-0.3.0.2/docs/Data-Tuple-Select.html
No GitHub:https://github.com/augustss/tuple
-Em certos casos, talvez seja melhor optar por criar um tipo de dado do que usar tuplas.


<h4>USO:</h4> Tem uso para os casos de que se deseja definir uma função ao qual recebe ou retorna mais de um valor, sendo normalmente de tipos heterogêneos. No Caso abaixo, a função verIdade recebe uma tupla de dois elementos de diferentes e retorna apenas a idade:

Seu uso torna-se interessante para alguns casos, como coordenadas, parâmetros conectores de base de dados

<h4>FUNÇÕES RELACIONADAS:</h4>

*De Prelude ou Data.Tuple:
Função fst: Retorna o primeiro valor de uma tupla-2;
Função scd: Retorna o segundo valor de uma tupla-2;
As duas acima podem ser usadas combinadas

Pattern Matching:
Usa os construtores da tupla. Pode-se usar esse método para tuplas maiores:

Função curry: converte uma função que recebe tuplas em uma que recebe 2 argumentos:
*
Função uncurry: converte função de argumentos em função de tuplas

Função zip: transforma duas listas em uma lista de tuplas:

Função swap: troca os elementos de um par:

ou:


Ex1:



Ex2:


Ex3:




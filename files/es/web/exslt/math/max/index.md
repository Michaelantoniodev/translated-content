---
title: max
slug: Web/EXSLT/math/max
tags:
  - EXSLT
  - Todas_las_Categorías
  - XSLT
translation_of: Web/EXSLT/math/max
---
{{XsltRef}}
`math:max()` devuelve el valor máximo de un conjunto de nodos (node-set).

To compute the maximum value of the node-set, the node set is sorted into descending order as it would be using [`xsl:sort()`](es/XSLT/sort) with a data type of `number`. The maximum value is then the first node in the sorted list, converted into a number.

## Sintaxis

    math:max(conjuntoNodos)

### Argumentos

- `conjuntoNodos`
  - : El conjunto de nodos cuyo valor más alto va a ser devuelto.

### Devuelve

Un fragmento de árbol resultante que representa como una cadena el valor numérico del nodo valorado como más alto.

## Definido en

[EXSLT - MATH:MAX](http://www.exslt.org/math/functions/max/index.html)

## Implementación en Gecko

Implementado en Gecko 1.9 y posteriores.

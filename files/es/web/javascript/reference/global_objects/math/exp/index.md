---
title: Math.exp()
slug: Web/JavaScript/Reference/Global_Objects/Math/exp
translation_of: Web/JavaScript/Reference/Global_Objects/Math/exp
original_slug: Web/JavaScript/Referencia/Objetos_globales/Math/exp
---
{{JSRef}}La función **Math.exp()** devuelve `ex`, donde `x` es el argumento, y `e` es {{jsxref("Math.E", "El número de Euler (también conocido como la constante de Napier)", "", 1)}}, la base de los algoritmos naturales.

## Sintaxis

    Math.exp(x)

### Parámetros

- `x`
  - : Un número.

### Valor devuelto

Un número represetando `ex`, donde `e` es {{jsxref("Math.E", "número de Euler", "", 1)}} y `x` es el argumento.

## Descripción

Porque `exp()` es un método estático de `Math`, siempre úsalo como `Math.exp()`, en vez de un método de un objeto `Math` que hayas creado (`Math` no es un constructor).

## Ejemplos

### Usando `Math.exp()`

```js
Math.exp(-1); // 0.36787944117144233
Math.exp(0);  // 1
Math.exp(1);  // 2.718281828459045
```

## Especificaciones

| Especificación                                                       | Estado                       | Comentario                                          |
| -------------------------------------------------------------------- | ---------------------------- | --------------------------------------------------- |
| {{SpecName('ES1')}}                                             | {{Spec2('ES1')}}         | Definición inicial. Implementado en JavaScript 1.0. |
| {{SpecName('ES5.1', '#sec-15.8.2.8', 'Math.exp')}} | {{Spec2('ES5.1')}}     |                                                     |
| {{SpecName('ES6', '#sec-math.exp', 'Math.exp')}}     | {{Spec2('ES6')}}         |                                                     |
| {{SpecName('ESDraft', '#sec-math.exp', 'Math.exp')}} | {{Spec2('ESDraft')}} |                                                     |

## Compatibilidad con navegadores

{{Compat("javascript.builtins.Math.exp")}}

## Ve también

- {{jsxref("Math.E")}}
- {{jsxref("Math.expm1()")}}
- {{jsxref("Math.log()")}}
- {{jsxref("Math.log10()")}}
- {{jsxref("Math.log1p()")}}
- {{jsxref("Math.log2()")}}
- {{jsxref("Math.pow()")}}

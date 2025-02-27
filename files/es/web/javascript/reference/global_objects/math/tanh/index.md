---
title: Math.tanh()
slug: Web/JavaScript/Reference/Global_Objects/Math/tanh
tags:
  - ECMAScript 2015
  - JavaScript
  - Referencia
  - metodo
translation_of: Web/JavaScript/Reference/Global_Objects/Math/tanh
original_slug: Web/JavaScript/Referencia/Objetos_globales/Math/tanh
---
{{JSRef}}

La funcion **`Math.tanh()`** devuelve la hyperbolica tangente de un numero, esto es

<math display="block"><semantics><mrow><mo lspace="0em" rspace="0em">tanh</mo><mi>x</mi><mo>=</mo><mfrac><mrow><mo lspace="0em" rspace="0em">sinh</mo><mi>x</mi></mrow><mrow><mo lspace="0em" rspace="0em">cosh</mo><mi>x</mi></mrow></mfrac><mo>=</mo><mfrac><mrow><msup><mi>e</mi><mi>x</mi></msup><mo>-</mo><msup><mi>e</mi><mrow><mo>-</mo><mi>x</mi></mrow></msup></mrow><mrow><msup><mi>e</mi><mi>x</mi></msup><mo>+</mo><msup><mi>e</mi><mrow><mo>-</mo><mi>x</mi></mrow></msup></mrow></mfrac><mo>=</mo><mfrac><mrow><msup><mi>e</mi><mrow><mn>2</mn><mi>x</mi></mrow></msup><mo>-</mo><mn>1</mn></mrow><mrow><msup><mi>e</mi><mrow><mn>2</mn><mi>x</mi></mrow></msup><mo>+</mo><mn>1</mn></mrow></mfrac></mrow><annotation encoding="TeX">\tanh x = \frac{\sinh x}{\cosh x} = \frac {e^x - e^{-x}} {e^x + e^{-x}} = \frac{e^{2x} - 1}{e^{2x}+1}</annotation></semantics></math>

{{EmbedInteractiveExample("pages/js/math-tanh.html")}}

## Sintaxis

    Math.tanh(x)

### Parametros

- `x`
  - : Un numero.

### Devolver valor

La hyperbolica tangente del numero obtenido.

## Descripcion

Porque `tanh()` es un metodo estatico de `Math`, siempre se usa como `Math.tanh()`, en lugar de ser un metodo de `Math` objeto que creas (`Math` no es un constructor).

## Ejemplos

### Usando `Math.tanh()`

```js
Math.tanh(0);        // 0
Math.tanh(Infinity); // 1
Math.tanh(1);        // 0.7615941559557649
```

## Polyfill

Esto puede ser emulado con ayuda de {{jsxref("Math.exp()")}} funcion:

```js
Math.tanh = Math.tanh || function(x){
    var a = Math.exp(+x), b = Math.exp(-x);
    return a == Infinity ? 1 : b == Infinity ? -1 : (a - b) / (a + b);
}
```

## Especificaciones

| Especificacion                                                           | Estado                       | Comentario          |
| ------------------------------------------------------------------------ | ---------------------------- | ------------------- |
| {{SpecName('ES2015', '#sec-math.tanh', 'Math.tanh')}} | {{Spec2('ES2015')}}     | Definicion inicial. |
| {{SpecName('ESDraft', '#sec-math.tanh', 'Math.tanh')}} | {{Spec2('ESDraft')}} |                     |

## Compatibilidad con navegadores

{{Compat("javascript.builtins.Math.tanh")}}

##

- {{jsxref("Math.acosh()")}}
- {{jsxref("Math.asinh()")}}
- {{jsxref("Math.atanh()")}}
- {{jsxref("Math.cosh()")}}
- {{jsxref("Math.sinh()")}}

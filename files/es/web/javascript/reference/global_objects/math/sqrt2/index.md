---
title: Math.SQRT2
slug: Web/JavaScript/Reference/Global_Objects/Math/SQRT2
translation_of: Web/JavaScript/Reference/Global_Objects/Math/SQRT2
original_slug: Web/JavaScript/Referencia/Objetos_globales/Math/SQRT2
---
{{JSRef}}La propiedad **Math.SQRT2** representa la raíz cuadrada de de 2, aproximadamente 1.414:

<math display="block"><semantics><mrow><mstyle mathvariant="monospace"><mi>Math.SQRT2</mi></mstyle><mo>=</mo><msqrt><mn>2</mn></msqrt><mo>≈</mo><mn>1.414</mn></mrow><annotation encoding="TeX">\mathtt{\mi{Math.SQRT2}} = \sqrt{2} \approx 1.414</annotation></semantics></math>

{{js_property_attributes(0, 0, 0)}}

## Descripción

Debido a que SQRT2 es una propiedad estática de `Math`, siempre se utiliza como `Math.SQRT2`, en lugar de una propiedad de un objeto `Math` creado`.`

## Ejemplos

### Utilizando Math.SQRT2

La siguiente función retorna la raíz cuadrada de 2:

```js
function getRoot2() {
  return Math.SQRT2;
}

getRoot2(); // 1.4142135623730951
```

## Especificaciones

| Especificación                                                               | Estado                       | Comentarios                                         |
| ---------------------------------------------------------------------------- | ---------------------------- | --------------------------------------------------- |
| {{SpecName('ES1')}}                                                     | {{Spec2('ES1')}}         | Definición inicial. Implementada en JavaScript 1.0. |
| {{SpecName('ES5.1', '#sec-15.8.1.8', 'Math.SQRT2')}}         | {{Spec2('ES5.1')}}     |                                                     |
| {{SpecName('ES6', '#sec-math.sqrt2', 'Math.SQRT2')}}         | {{Spec2('ES6')}}         |                                                     |
| {{SpecName('ESDraft', '#sec-math.sqrt2', 'Math.SQRT2')}} | {{Spec2('ESDraft')}} |                                                     |

## Compatibilidad en navegadores

{{Compat("javascript.builtins.Math.SQRT2")}}

##

## Ver también

- {{jsxref("Math.pow()")}}
- {{jsxref("Math.sqrt()")}}

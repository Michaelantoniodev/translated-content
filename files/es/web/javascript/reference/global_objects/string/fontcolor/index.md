---
title: String.prototype.fontcolor()
slug: Web/JavaScript/Reference/Global_Objects/String/fontcolor
translation_of: Web/JavaScript/Reference/Global_Objects/String/fontcolor
original_slug: Web/JavaScript/Referencia/Objetos_globales/String/fontcolor
---
{{JSRef}} {{deprecated_header}}

`El método `**`fontcolor()`** crea {{HTMLElement("font")}} elemento HTML que cambia el color de la cadena.

> **Nota:** **Usage note:** La etiqueta \<font> fue eliminada en [HTML5](/es/docs/Web/Guide/HTML/HTML5) y no debe ser usada. En lugar de es, es necesario aplicar propiedades [CSS](/es/docs/Web/CSS).

## Sintaxis

    str.fontcolor(color)

### Parametros

- `color`
  - : A string expressing the color as a hexadecimal RGB triplet or as a string literal. String literals for color names are listed in the [CSS color reference](/es/docs/Web/CSS/color_value).

## Descripción

Si expresas el color como hexadecimal, usa el formato rrggbb. Por ejemplo, el color hexadecimal para salmón es R=FA, G=80, B=72, así que el valor será `"FA8072"`.

## Ejemplos

### `Usos fontcolor()`

Los siguientes ejemplos usan el método `fontcolor()` para cambiar el color de una cadena.

```js
var worldString = 'Hello, world';

console.log(worldString.fontcolor('red') +  ' en rojo');
// '<font color="red">Hello, world</font> en rojo'

console.log(worldString.fontcolor('FF00') + ' es rojo en hexadecimal');
// '<font color="FF00">Hello, world</font> es rojo en hexadecimal'
```

Con el objeto {{domxref("HTMLElement.style", "element.style")}} obtienes el atributo `style` y manipularlo:

```js
document.getElementById('yourElemId').style.color = 'red';
```

## Especificaciones

| Especificación                                                                                                   | Estatus              | Comentario                                                                                                                                 |
| ---------------------------------------------------------------------------------------------------------------- | -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| {{SpecName('ES6', '#sec-string.prototype.fontcolor', 'String.prototype.fontcolor')}} | {{Spec2('ES6')}} | Initial definition. Implemented in JavaScript 1.0. Defined in the (normative) Annex B for Additional ECMAScript Features for Web Browsers. |

## Compatibilidad con navegadores

{{Compat("javascript.builtins.String.fontcolor")}}

## Ver también

- {{jsxref("String.prototype.fontsize()")}}

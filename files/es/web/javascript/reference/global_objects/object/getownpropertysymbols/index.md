---
title: Object.getOwnPropertySymbols()
slug: Web/JavaScript/Reference/Global_Objects/Object/getOwnPropertySymbols
tags:
  - ECMAScript6
  - Experimental
  - JavaScript
  - Método(2)
  - Objeto
translation_of: Web/JavaScript/Reference/Global_Objects/Object/getOwnPropertySymbols
original_slug: Web/JavaScript/Referencia/Objetos_globales/Object/getOwnPropertySymbols
---
{{JSRef}}

El método **`Object.getOwnPropertySymbols()`** regresa una colección de todos las propiedades de los simbolos encontrados directamente en un objeto dado.

## Síntaxis

    Object.getOwnPropertySymbols(obj)

### Parametros

- `obj`
  - : El objeto del cual los simbolos de propiedades son devueltos.

## Descripción

Similar a {{jsxref("Object.getOwnPropertyNames()")}}, puedes obtener todas las propiedades de simbolos de un objeto dado como una colección de simbolos. Note que {{jsxref("Object.getOwnPropertyNames()")}} no contiene en sí mismo las propiedades de simbolos de un objeto y solo contiene las propiedades de cadenas.

Cómo todos los objetos no tienen inicialmente propiedades simbolos propios, `Object.getOwnPropertySymbols()` regresa una colección vacia a menos que tengas propiedades de simbolos establecidas en tu objeto.

## Ejemplos

```js
var obj = {};
var a = Symbol('a');
var b = Symbol.for('b');

obj[a] = 'localSymbol';
obj[b] = 'globalSymbol';

var objectSymbols = Object.getOwnPropertySymbols(obj);

console.log(objectSymbols.length); // 2
console.log(objectSymbols);        // [Symbol(a), Symbol(b)]
console.log(objectSymbols[0]);     // Symbol(a)
```

## Especificaciones

| Especificación                                                                                                       | Estado               | Comentario          |
| -------------------------------------------------------------------------------------------------------------------- | -------------------- | ------------------- |
| {{SpecName('ES6', '#sec-object.getownpropertysymbols', 'Object.getOwnPropertySymbols')}} | {{Spec2('ES6')}} | Definición inicial. |

## Compatibilidad con navegadores

{{Compat("javascript.builtins.Object.getOwnPropertySymbols")}}

## Ver también

- {{jsxref("Object.getOwnPropertyNames()")}}
- {{jsxref("Symbol")}}

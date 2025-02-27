---
title: get Array[@@species]
slug: Web/JavaScript/Reference/Global_Objects/Array/@@species
tags:
  - Array
  - JavaScript
  - Prototipo
  - metodo
translation_of: Web/JavaScript/Reference/Global_Objects/Array/@@species
original_slug: Web/JavaScript/Referencia/Objetos_globales/Array/@@species
---
{{JSRef}}

La propiedad de acceso **`Array[@@species]`** devuelve el constructor de `Array`.

## Sintaxis

    Array[Symbol.species]

### Valor de retorno

El constructor {{jsxref("Array")}}.

## Descripción

La propiedad de acceso `species` devuelve el constructor predeterminado para objetos `Array`. Los constructores de subclase pueden anularlo para cambiar la asignación del constructor.

## Ejemplos

La propiedad `species` devuelve la función de constructor predeterminada, que es el constructor `Array` para objetos `Array`:

```js
Array[Symbol.species]; // function Array()
```

In a derived collection object (e.g. your custom array `MyArray`), the `MyArray` species is the `MyArray` constructor. However, you might want to overwrite this, in order to return parent `Array` objects in your derived class methods:

```js
class MyArray extends Array {
  // Overwrite MyArray species to the parent Array constructor
  static get [Symbol.species]() { return Array; }
}
```

## Especificaciones

| Especificación                                                                                           | Estado                       | Comentario          |
| -------------------------------------------------------------------------------------------------------- | ---------------------------- | ------------------- |
| {{SpecName('ES6', '#sec-get-array-@@species', 'get Array [ @@species ]')}}     | {{Spec2('ES6')}}         | Definición inicial. |
| {{SpecName('ESDraft', '#sec-get-array-@@species', 'get Array [ @@species ]')}} | {{Spec2('ESDraft')}} |                     |

## Compatibilidad con navegadores

{{Compat("javascript.builtins.Array.@@species")}}

## Ver también

- {{jsxref("Array")}}
- {{jsxref("Symbol.species")}}

---
title: Object.prototype.hasOwnProperty()
slug: Web/JavaScript/Reference/Global_Objects/Object/hasOwnProperty
tags:
  - JavaScript
  - Method
  - Object
  - Prototype
translation_of: Web/JavaScript/Reference/Global_Objects/Object/hasOwnProperty
original_slug: Web/JavaScript/Referencia/Objetos_globales/Object/hasOwnProperty
---
{{JSRef("Objetos_globales", "Object")}}

## Resumen

El método **`hasOwnProperty()`** devuelve un booleano indicando si el objeto tiene la propiedad especificada.

## Sintaxis

    obj.hasOwnProperty(prop)

### Parámetros

- `prop`
  - : El nombre de la propiedad a buscar.

## Descripción

Todo objeto descendiente de `Object` hereda el método `hasOwnProperty`. Este método puede ser usando para determinar si un objeto tiene la propiedad especificada como una propiedad directa de ese objeto; a diferencia del operador {{jsxref("Operators/in", "in")}}, este método no verifica la cadena prototipo del objeto.

## Ejemplos

### Ejemplo: usar `hasOwnProperty` para comprobar la existencia de una propiedad

El siguiente ejemplo determina si el objeto `o` contiene una propiedad llamada `prop`:

```js
o = new Object();
o.prop = 'exists';

function changeO() {
  o.newprop = o.prop;
  delete o.prop;
}

o.hasOwnProperty('prop');   // returns true
changeO();
o.hasOwnProperty('prop');   // returns false
```

### Ejemplo: Directo versus propiedades heredadas

El siguiente ejemplo diferencia entre propiedades directas y propiedades heredadas a través de la cadena prototype:

```js
o = new Object();
o.prop = 'exists';
o.hasOwnProperty('prop');             // returns true
o.hasOwnProperty('toString');         // returns false
o.hasOwnProperty('hasOwnProperty');   // returns false
```

### Ejemplo: Iterando sobre las propiedades de un objeto

El siguiente ejemplo muestra como iterar sobre las propiedades de un objeto sin ejecutar sobre propiedades heredadas. Observe que el bucle for..in ya está no solo iterando elementos enumerables, por consiguiente uno no debería asumir que basado en la falta de propiedades no numerales mostrando en el bucle que hasOwnProperty por si misma no está solo es estrictamente para iterar elementos numerados (como con {{jsxref("Object.getOwnPropertyNames()")}}).

```js
var buz = {
    fog: 'stack'
};

for (var name in buz) {
    if (buz.hasOwnProperty(name)) {
        alert("this is fog (" + name + ") for sure. Value: " + buz[name]);
    }
    else {
        alert(name); // toString or something else
    }
}
```

### Ejemplo: `hasOwnProperty` como una propiedad

JavaScript no protege el nombre de la propiedad `hasOwnProperty`; en consecuencia, si existe la posibilidad de que un objeto pudiera tener la propiedad con ese nombre, es necesario usar un externo `hasOwnProperty` para obtener los correctos resultados:

```js
var foo = {
    hasOwnProperty: function() {
        return false;
    },
    bar: 'Here be dragons'
};

foo.hasOwnProperty('bar'); // always returns false

// Use another Object's hasOwnProperty and call it with 'this' set to foo
({}).hasOwnProperty.call(foo, 'bar'); // true

// It's also possible to use the hasOwnProperty property from the Object property for this purpose
Object.prototype.hasOwnProperty.call(foo, 'bar'); // true
```

Observe que en el último caso no han habido nuevos objetos creados.

## Especificaciones

| Especificaciones                                                                                                             | Estado                   | Comentario          |
| ---------------------------------------------------------------------------------------------------------------------------- | ------------------------ | ------------------- |
| ECMAScript 3rd Edition. Implemented in JavaScript 1.5                                                                        | Standard                 | Initial definition. |
| {{SpecName('ES5.1', '#sec-15.2.4.5', 'Object.prototype.hasOwnProperty')}}                             | {{Spec2('ES5.1')}} |                     |
| {{SpecName('ES6', '#sec-object.prototype.hasownproperty', 'Object.prototype.hasOwnProperty')}} | {{Spec2('ES6')}}     |                     |

## Compatibilidad de navegadores

{{Compat("javascript.builtins.Object.hasOwnProperty")}}

## Véase también

- [Enumerability and ownership of properties](/es/docs/Enumerability_and_ownership_of_properties)
- {{jsxref("Object.getOwnPropertyNames()")}}
- [for...in](/es/docs/Web/JavaScript/Reference/Statements/for...in)
- {{jsxref("Operators/in", "in")}}
- [JavaScript Guide: Inheritance revisted](/es/docs/Web/JavaScript/Guide/Inheritance_Revisited)

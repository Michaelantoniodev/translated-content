---
title: Date.now()
slug: Web/JavaScript/Reference/Global_Objects/Date/now
tags:
  - Date
  - JavaScript
  - Method
  - Reference
translation_of: Web/JavaScript/Reference/Global_Objects/Date/now
original_slug: Web/JavaScript/Referencia/Objetos_globales/Date/now
---
{{JSRef("Objetos_globales", "Date")}}

## Resumen

Devuelve el número de milisegundos transcurridos desde las 00:00:00 UTC del 1 de enero de 1970.

## Sintaxis

    var fechaEnMiliseg = Date.now();

## Descripción

El método `now` devuelve los milisegundos transcurridos desde las 00:00:00 UTC del 1 de enero de 1970 justo hasta ahora como un {{jsxref("Number")}}.

Cuando se usa `now` para crear registros temporales or identificadores únicos, tenga en cuenta que la precisión de Windows puede ser de 15 milisegundos (vea {{Bug(363258)}}), lo que puede provocar valores iguales si `now` se llama múltiples veces en un breve intervalo de tiempo.

## Ejemplos

### Ejemplo: Usando `now`

El siguiente ejemplo usa `now` para crear un registro temporal.

```js
var registro = Date.now();
```

## Vea También

- {{domxref("window.performance.now")}}
- {{domxref("console.time")}} / {{domxref("console.timeEnd")}}

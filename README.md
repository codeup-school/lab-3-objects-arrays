# Lab: Combinando Arrays y Objetos en JavaScript

Este laboratorio está diseñado para ayudarte a practicar el uso combinado de **arrays** y **objetos** en JavaScript. Trabajarás con colecciones de datos y aprenderás cómo acceder y manipular objetos dentro de arrays y viceversa.

## Requisitos previos

Antes de comenzar este laboratorio, asegúrate de tener los siguientes conocimientos:

- Cómo declarar y utilizar variables
- Estructura básica de arrays y objetos
- Cómo funcionan las funciones y los loops en JavaScript

---

## Ejercicio 1: Imprimir información de objetos en un array

En este ejercicio, tendrás que recorrer un array de objetos e imprimir cierta información de cada uno.

### Instrucciones

1. Declara un array llamado `estudiantes`, donde cada elemento es un objeto con las propiedades `nombre` y `edad`, por ejemplo:
   ```javascript
   const estudiantes = [
     { nombre: "Ana", edad: 20 },
     { nombre: "Luis", edad: 22 },
     { nombre: "Carlos", edad: 19 },
   ];
   ```
2. Crea una función llamada `imprimirEstudiantes` que recorra el array y muestre en la consola el nombre y la edad de cada estudiante en el formato: "Nombre: [nombre], Edad: [edad]".

### Ejemplo de código

```javascript
const estudiantes = [
  { nombre: "Ana", edad: 20 },
  { nombre: "Luis", edad: 22 },
  { nombre: "Carlos", edad: 19 },
];

function imprimirEstudiantes(estudiantes) {
  for (let i = 0; i < estudiantes.length; i++) {
    console.log(
      `Nombre: ${estudiantes[i].nombre}, Edad: ${estudiantes[i].edad}`
    );
  }
}

imprimirEstudiantes(estudiantes);
```

### Ejemplo de salida

```
Nombre: Ana, Edad: 20
Nombre: Luis, Edad: 22
Nombre: Carlos, Edad: 19
```

---

## Ejercicio 2: Filtrar objetos según una propiedad

En este ejercicio, escribirás una función que filtre objetos de un array basándose en una propiedad.

### Instrucciones

1. Utiliza el array `estudiantes` del ejercicio anterior.
2. Crea una función llamada `filtrarMayoresDeEdad` que recorra el array de estudiantes y devuelva un nuevo array con los estudiantes cuya edad sea mayor o igual a 21.
3. Muestra el array filtrado en la consola.

### Ejemplo de código

```javascript
const estudiantes = [
  { nombre: "Ana", edad: 20 },
  { nombre: "Luis", edad: 22 },
  { nombre: "Carlos", edad: 19 },
];

function filtrarMayoresDeEdad(estudiantes) {
  const mayoresDeEdad = [];
  for (let i = 0; i < estudiantes.length; i++) {
    if (estudiantes[i].edad >= 21) {
      mayoresDeEdad.push(estudiantes[i]);
    }
  }
  return mayoresDeEdad;
}

const resultado = filtrarMayoresDeEdad(estudiantes);
console.log(resultado);
```

### Ejemplo de salida

```
[ { nombre: 'Luis', edad: 22 } ]
```

---

## Ejercicio 3: Sumar una propiedad de todos los objetos en un array

En este ejercicio, calcularás la suma total de una propiedad numérica de todos los objetos en un array.

### Instrucciones

1. Usa el mismo array `estudiantes`, pero asegúrate de que cada objeto tenga una nueva propiedad llamada `calificaciones`, que sea un número. Ejemplo:
   ```javascript
   const estudiantes = [
     { nombre: "Ana", edad: 20, calificaciones: 85 },
     { nombre: "Luis", edad: 22, calificaciones: 90 },
     { nombre: "Carlos", edad: 19, calificaciones: 78 },
   ];
   ```
2. Crea una función llamada `calcularSumaCalificaciones` que recorra el array y sume todas las calificaciones de los estudiantes.
3. Muestra el total de la suma en la consola.

### Ejemplo de código

```javascript
const estudiantes = [
  { nombre: "Ana", edad: 20, calificaciones: 85 },
  { nombre: "Luis", edad: 22, calificaciones: 90 },
  { nombre: "Carlos", edad: 19, calificaciones: 78 },
];

function calcularSumaCalificaciones(estudiantes) {
  let suma = 0;
  for (let i = 0; i < estudiantes.length; i++) {
    suma += estudiantes[i].calificaciones;
  }
  return suma;
}

const totalCalificaciones = calcularSumaCalificaciones(estudiantes);
console.log("Suma total de calificaciones:", totalCalificaciones);
```

### Ejemplo de salida

```
Suma total de calificaciones: 253
```

---

## Ejercicio 4: Encontrar un objeto en un array según una propiedad

En este ejercicio, escribirás una función que busque un objeto en un array según una propiedad específica.

### Instrucciones

1. Utiliza el mismo array `estudiantes` con las propiedades `nombre`, `edad`, y `calificaciones`.
2. Crea una función llamada `buscarEstudiantePorNombre` que tome dos parámetros: el array `estudiantes` y una cadena `nombreBuscado`.
3. La función debe devolver el objeto del estudiante cuyo nombre coincida con `nombreBuscado`.
4. Si no se encuentra ningún estudiante con ese nombre, muestra un mensaje que indique "Estudiante no encontrado".

### Ejemplo de código

```javascript
const estudiantes = [
  { nombre: "Ana", edad: 20, calificaciones: 85 },
  { nombre: "Luis", edad: 22, calificaciones: 90 },
  { nombre: "Carlos", edad: 19, calificaciones: 78 },
];

function buscarEstudiantePorNombre(estudiantes, nombreBuscado) {
  for (let i = 0; i < estudiantes.length; i++) {
    if (estudiantes[i].nombre === nombreBuscado) {
      return estudiantes[i];
    }
  }
  return "Estudiante no encontrado";
}

const estudianteEncontrado = buscarEstudiantePorNombre(estudiantes, "Luis");
console.log(estudianteEncontrado);
```

### Ejemplo de salida

```
{ nombre: 'Luis', edad: 22, calificaciones: 90 }
```

---

## Notas adicionales

- Asegúrate de probar cada función con diferentes valores para verificar que tu código funcione correctamente.
- Si algo no funciona como esperabas, revisa la lógica de tus loops y condicionales.
- Usa `console.log()` para ver los resultados de tus pruebas y depurar tu código si es necesario.

¡Disfruta programando con arrays y objetos!

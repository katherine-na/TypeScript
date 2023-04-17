<h1 align="center"> TypeScript </h1>

¿Qué es TypeScript?  
TypeScript es un lenguaje creado por Microsoft para resolver las deficiencias de JavaScript, amplia el lenguaje con nuevas funciones y sintaxis. 
TypeScript tenemos que compilarlo en JavaScript para que los navegadores lo entiendan

¿Para qué nos sirve usar TypeScript?  
Algunas de las principales razones para usar TypeScript:

- Tipado estático:  
TypeScript permite agregar tipos estáticos a variables, funciones y clases, lo que ayuda a detectar errores en tiempo de compilación.
- Escalabilidad:  
TypeScript es una buena opción para proyectos grandes y complejos, ya que su tipado estático ayuda a mantener el código organizado y fácil de entender.

¿Por qué se creo TypeScript?  
TypeScript fue creado en 2012 por Microsoft como una solución para algunos de los problemas que se encontraban en el desarrollo de aplicaciones web y móviles utilizando JavaScript. 

Instalar compilador de typescript
```
npm install -g typescript 
```
Compilar archivo  
```
tsc nameProject.ts
```

Para compilar typescript cada ves que se hace un cambio se debe ejecutar el mismo comando ```tsc nameProject.ts```
Sin embargo también podemos compilar typescript cada vez que guardamos automaticamente utilizando el comando  ```tsc nameProject.ts -w```
 
# Definición de tipos
En TypeScript, la definición de tipos se refiere a la especificación del tipo de dato que se espera que una variable un parámetro de función, una propiedad de objeto o cualquier otra entidad tenga en el programa.  
La definición de tipos en TypeScript es opcional, sin embargo en typescript es de mucha ayuda.  
La sintaxis para definir tipos en TypeScript utiliza la notación de dos puntos ":" para especificar el tipo de dato de una variable, propiedad o parámetro de función. Por ejemplo:

```
let edad: number;
```

Para especificar que el tipo de dato de una función debe ser number.
```
const circ = (diameter: number) => {
 return diameter * Math.PI;
}
```
## Arrays & Objects
Si declaramos nuestro Array con solo un tipo de dato, únicamente podrá tener ese tipo de dato a la hora que queramos agregar más datos a nuestro array.
```
let names = ['mario', 'luigi', 'yoshi']
names.push('peach') //Esto esta bien
names.push(3) //Esto esta mal y nos arrojara un error
```

```
let numbers = ['13', '31', '03']
numbers.push(3) //Esto esta bien
numbers.push('Hola') //Esto esta mal y nos arrojara un error
```
También podemos crear nuestro Array con distintos tipos de datos.
```
let mixed = ['mario', 3, 'yoshi', 9, 8]
mixed.push(3) //Esto esta bien
mixed.push('Hola') //Esto también esta bien
```

Los objetos funcionan de igual manera, si inicializamos con un tipo de dato, ese debe ser el mismo.
```
let ninja = {
 name: 'Kathy',
 lastName: 'Negrete',
 age: 22
}

ninja.name = 'Katherine' //Esto esta bien
ninja.age = 'Twenty two' //Esto esta mal
```
Si deseamos agregar a nuestro objeto una nueva propiedad, nos dará un error ya que no coincide con la estructura del objeto inicial.

# Interfaz
Una interfaz es una estructura que define un conjunto de propiedades y métodos que deben ser implementados por un objeto
pueden describir no solo los métodos sino también las propiedades y tipos de datos.
 
La definición de tipo también puede ser más compleja, utilizando interfaces, uniones de tipos y otros conceptos avanzados. Por ejemplo, una interfaz puede definir los tipos de datos esperados para las propiedades de un objeto:

```
interface Person {
  name: string;
  age: number;
  direction?: string;
}
```
En este ejemplo, la interfaz "Persona" define tres propiedades, dos de las cuales son obligatorias (nombre y edad) y una es opcional (dirección). Al utilizar la interfaz "Persona", el programador puede asegurarse de que los objetos creados en el programa tengan las propiedades y tipos de datos esperados.

# Tipos de composición en TypeScript
Son una forma de definir nuevos tipos a partir de otros ya existentes.  
Estos tipos se crean combinando dos o más tipos existentes para formar un nuevo tipo que contiene todas las propiedades y métodos de los tipos originales.

- Intersección: 
  - Se utiliza el símbolo & para combinar dos o más tipos en un solo tipo que incluye todas las propiedades y métodos de los tipos originales
- Unión: 
  - Se utiliza el símbolo | para crear un nuevo tipo que puede ser uno de los tipos originales.
  ```
  let arrayMixed: (string|number)[] = []
  ```
- Composición de clases: 
  - Se utiliza la herencia de clases para crear una nueva clase que tenga todas las propiedades y métodos de las clases originales.

Los tipos de composición son una herramienta poderosa en TypeScript que permiten crear nuevos tipos complejos a partir de tipos existentes, lo que facilita el desarrollo y la mantenibilidad del código.
 
# Dynamic (any) Types

```
let nickname = any;
```
La variable nickname es de tipo de dato 'any' (cualquiera) lo que significa que en el futuro nickname puede ser de cualquier tipo de dato, ya sea un boolean, un string, un object, etc.

```
let mixed = any[] = [];
mixed.push('Kathy')
mixed.push(22)
```
La variable mixed incializa con un array vacío y al agregar 'any' estamos diciendo que en el futuro podemos insertar cualquier tipo de dato.

```
let data: {name: any, age: any}
data = {name: 'Kathy', age: 'twenty two'}
```

# Arbol de trabajo
tsconfig.json
dist

<h1 align="center"> TypeScript </h1>

TypeScript es un lenguaje creado por Microsoft para resolver las deficiencias de JavaScript 

# Interfaz
una interfaz es una estructura que define un conjunto de propiedades y métodos que deben ser implementados por un objeto
 pueden describir no solo los métodos sino también las propiedades y tipos de datos.
 
# Definición de tipos
En TypeScript, la definición de tipos se refiere a la especificación del tipo de dato que se espera que una variable un parámetro de función, una propiedad de objeto o cualquier otra entidad tenga en el programa.  
La definición de tipos en TypeScript es opcional.  
La sintaxis para definir tipos en TypeScript utiliza la notación de dos puntos ":" para especificar el tipo de dato de una variable, propiedad o parámetro de función. Por ejemplo

```
let edad: number;
```

La definición de tipo también puede ser más compleja, utilizando interfaces, uniones de tipos y otros conceptos avanzados. Por ejemplo, una interfaz puede definir los tipos de datos esperados para las propiedades de un objeto:

```
interface Persona {
  nombre: string;
  edad: number;
  direccion?: string;
}
```
En este ejemplo, la interfaz "Persona" define tres propiedades, dos de las cuales son obligatorias (nombre y edad) y una es opcional (dirección). Al utilizar la interfaz "Persona", el programador puede asegurarse de que los objetos creados en el programa tengan las propiedades y tipos de datos esperados.

# Tipos de composición en TypeScript
Son una forma de definir nuevos tipos a partir de otros ya existentes.  
Estos tipos se crean combinando dos o más tipos existentes para formar un nuevo tipo que contiene todas las propiedades y métodos de los tipos originales.

## Tipos de composición

- Intersección: 
  - Se utiliza el símbolo & para combinar dos o más tipos en un solo tipo que incluye todas las propiedades y métodos de los tipos originales
- Unión: 
  - Se utiliza el símbolo | para crear un nuevo tipo que puede ser uno de los tipos originales.
- Composición de clases: 
  - Se utiliza la herencia de clases para crear una nueva clase que tenga todas las propiedades y métodos de las clases originales.

Los tipos de composición son una herramienta poderosa en TypeScript que permiten crear nuevos tipos complejos a partir de tipos existentes, lo que facilita el desarrollo y la mantenibilidad del código.

Para aprender el tipo de una variable, use **typeof**:

 
 ```
 interface Person {
  firstName: string;
  lastName: string;
  age: number;
}


 ```

# Arbol de trabajo
## tsconfig.json
## dist

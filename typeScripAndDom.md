<h1 align="center">TypeScript & DOM</h1>

El DOM en TypeScript funciona de la misma manera que en JavaScript  pero con la ventaja adicional de poder aprovechar las características de tipos estáticos de TypeScript para hacer el código más seguro y fácil de mantener.

Para trabajar con el DOM en TypeScript, es necesario usar las mismas funciones y propiedades que se usan en JavaScript para acceder a los elementos del DOM. 
Por ejemplo, se puede acceder a un elemento utilizando la función document.querySelector()

# Class

```
class Persona {
  nombre: string;
  edad: number;

  constructor(nombre: string, edad: number) {
    this.nombre = nombre;
    this.edad = edad;
  }
  
  saludar() {
    console.log(`Hola, mi nombre es ${this.nombre} y tengo ${this.edad} años.`);
  }
}

```

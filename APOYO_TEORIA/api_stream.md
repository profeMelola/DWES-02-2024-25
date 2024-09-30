# Java Streams

![image](https://github.com/user-attachments/assets/349c5bb6-903c-422e-be19-63db2f66ff77)

<pre>https://medium.com/@berrachdim/mastering-data-processing-with-java-streams-a-comprehensive-guide-581f2a64052a</pre>

## Descripción

- Los Streams fueron introducidos a Java en la versión 8.
- Permiten procesar secuencias de elementos con operaciones previamente definidas en la API.
- La API de Streams contiene clases para procesar secuencias de elementos y pueden ser creados desde componentes existentes en Java como las Colecciones.
- El código es declarativo, definimos el que y no el cómo.
- Menos complejidad y más legibilidad del código.
- Los Streams son autoiterables (no tenemos que definir explícitamente la forma en que se van a iterar).
- Integración con la API funcional (interfaces funcionales, expresiones lambda, etc). Esto me permite reutilizar funciones.
- Uso del paralelismo, nos permite ejecutar operaciones paralelas de una forma fácil.

## Tipos de operaciones

En la API de Streams existen dos tipos de operaciones, las operaciones Intermedias y las operaciones Terminales. En ningún caso las operaciones cambian la fuente, es decir que promueven la inmutabilidad.

La forma en que se ejecutan las operaciones es conocida como Lazyness, es decir que las operaciones se ejecutan al último momento o lo más tarde posible.

Las operaciones terminales son las que producen la ejecución de las operaciones intermedias.

### Operaciones intermedias

Son operaciones que retornan un Stream. Retornan una nueva versión del Stream del tipo Stream<T>. Estas operaciones pueden ser encadenadas para formar un “Pipeline” de operaciones. 

Algunas de las operaciones intermedias son:

- map()
- filter()
- distinct()
- sorted()
- limit()
- peek()
- skip()

### Operaciones terminales

Son operaciones que no retornan un Stream, sino que retornan un valor primitivo, una colección o un objeto. 

Las operaciones terminales no pueden ser encadenadas. 

Algunas de las operaciones terminales son:

- forEach()
- toArray()
- reduce()
- collect()
- min()
- max()
- count()
- anyMatch()
- allMatch()
- noneMatch()
- findFirst()
- findAny()


https://barcochrist.medium.com/streams-en-java-5712989fc62b

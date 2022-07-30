### Ejercicio spring boot (segunda parte)

Hacer fork del repo: https://github.com/iuresti/peopleandcars-exercise

1. Modificar el servicio para leer peticiones para agregar personas, carros y relaciones a través de
   Rabbit MQ
2. Crear una aplicación adicional que lea el siguiente yaml:

```yaml
process:
  people:
    path: <directorio donde están los archivos de datos de personas>
    threads-count: <Número de hilos que leerán los archivos de forma concurrente>
    thread-prefix: <prefijo utilizado para identificar estos threads>
  cars:
    path: <directorio donde están los archivos de datos de carros>
    threads-count: <Número de hilos que leerán los archivos de forma concurrente>
    thread-prefix: <prefijo utilizado para identificar estos threads>
  relations:
    path: <directorio donde están los archivos de datos de relaciones>
    threads-count: <Número de hilos que leerán los archivos de forma concurrente>
    thread-prefix: <prefijo utilizado para identificar estos threads>
```

El bloque anterior define 3 tipos de procesos:

- el proceso people, se encargará de leer archivos csv con información de las personas (con los
  mismos datos que se usaron en la primera parte)
- el proceso cars, se encargará de leer archivos csv con información de los carros (con los
  mismos datos que se usaron en la primera parte)
- el proceso relations, se encargará de crear las relaciones también leídas desde un archivo csv

Los hilos mandarán requests a una cola de RabbitMQ que será consumida por el servicio.

Los hilos de relaciones deben esperar a que los hilos de people y de cars terminen

Los archivos de datos para este ejercicio están en el directorio [data](data)

La biblioteca opencsv es una buena alternativa para leer los
archivos: [referencia](http://opencsv.sourceforge.net/#quick_start)


> Requerimiento: Solo se permite utilizar la interfaz Runnable, la clase Thread, los métodos wait,
> notify, notifyAll y la palabra reservada synchronized para este ejercicio. No Future,
> ExecutorService u otras herramientas que ofrece el lenguaje para ejecución y control de hilos. 




### Ejercicio spring boot (segunda parte)

Hacer fork del repo: https://github.com/iuresti/peopleandcars-exercise

1. Modificar el archivo schema/src/main/resources/schema.yml para que contenga la especificación de
   los endpoints y modelos para el ejercicio de la primera parte (people and cars).

> Tip: Puedes usar el [swagger editor online](https://editor.swagger.io/) para tener una vista clara
> de lo que estás escribiendo

2. Ejecutar `maven install -P generate-api` para generar los controllers y los DTO a partir de la
   especificación open-api generada en el punto 1.
3. Adaptar el código desarrollado en la parte 1 de este ejercicio para que funcione con los nuevos
   endpoints
4. Utilizar la especificación para generar una postman collection que permitirá testear el proyecto

Información sobre proyectos multi-modulo puede encontrarse [aqui](https://spring.io/guides/gs/multi-module/)




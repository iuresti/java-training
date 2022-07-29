----
spring boot
- docker
- bases de datos
- queues

---------------------------------------------
SOLID -> Guía para generar código mantenible

S -> Single Responsibility ->
O -> Open close principle ->
L -> Liskov Substitution Principle ->
I -> Interface Segregation Principle
D -> Dependency Inversion Principle ->
Desacoplar dependencias
-> Interfaces


***Primera parte***

- Crear un servicio REST que permita almacenar información de personas y carros, las personas tienen la siguiente información:
- id (GUID)
- firstName string
- lastName string
- email string
- gender string

los carros tienen los siguientes datos:
- vin string
- brand string
- model string
- year integer
- color string

El sistema permite crear relaciones entre las personas y los carros:
- una persona puede ser dueña de muchos carros
- Un carro solo le pertenece a una persona
- Puede haber personas sin carros
- Puede haber carros sin personas

Se requieren endpoints para manejar el CRUD tanto de carros como de personas

Adicional:
* el endpoint /api/people/{person_id}/cars permite obtener todos los carros de una persona
* el endpoint /api/cars/{car_vin}/people permite obtener todos los dueños de un carro

Requerimientos:
* Usar docker para correr el SMBD, puede ser cualquiera. postgres

***Segunda parte***


Requerimientos:
- Utilizar https://editor.swagger.io/ para definir los modelos y los endpoints soportados por la aplicación con openapi
- Crear un proyecto multimodulo de maven con tres modulos  (https://spring.io/guides/gs/multi-module/)
    - schema
    - api-model
    - service

### Ejercicio spring boot (Primera parte)

Crear un servicio REST que permita almacenar información de personas y carros.
Los datos a guardar de las personas son:

- id (GUID)
- firstName string
- lastName string
- email string
- gender string

Los datos a guardar de los carros son:

- vin string
- brand string
- model string
- year integer
- color string

El sistema permite crear relaciones entre las personas y los carros bajo las siguientes
restricciones:

- una persona puede ser dueña de muchos carros
- Un carro solo le pertenece a una persona
- Puede haber personas sin carros
- Puede haber carros sin personas

Se requieren endpoints para manejar el CRUD tanto de carros como de personas

Adicional:

- el endpoint /api/people/{person_id}/cars permite obtener todos los carros de una persona
- el endpoint /api/cars/{car_vin}/people permite obtener todos los dueños de un carro

Requerimientos:

> Usar docker para correr el SMBD, puede ser cualquiera.

Puedes usar esta [postman collection](tests/People&Cars%201.postman_collection.json) para probar los
endpoints

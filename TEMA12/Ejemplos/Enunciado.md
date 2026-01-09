# Ejercicio práctico MongoDB — Clientes y Empleados (Enunciado)

## Contexto

Una empresa quiere gestionar su información mediante **MongoDB**.
Para ello necesita almacenar datos de **clientes** y **empleados** en una base de datos No‑SQL.

El objetivo es practicar la creación de bases de datos, colecciones y consultas
utilizando **MongoDB Compass** y **MongoDB Shell (mongosh)**.

---

## Requisitos del ejercicio

### 1. Base de datos
- Crear una base de datos llamada `miBD`.

---

### 2. Colecciones
Dentro de la base de datos `miBD`, crear las siguientes colecciones:
- `clientes`
- `empleados`

---

### 3. Clientes
Insertar **al menos dos clientes** con la siguiente estructura:

- Nombre
- Apellidos
- Edad
- Teléfono
- Dirección (objeto embebido con):
  - Calle
  - Número
  - Ciudad

| nombre | apellidos      | edad | telefono  | direccion.calle   | direccion.numero | direccion.ciudad |
| ------ | -------------- | ---- | --------- | ----------------- | ---------------- | ---------------- |
| Juan   | Pérez García   | 35   | 600123456 | Gran Vía          | 45               | Madrid           |
| Laura  | Martínez López | 28   | 611987654 | Calle Mayor       | 12               | Valencia         |
| Carlos | Sánchez Ruiz   | 42   | 622555888 | Avenida Andalucía | 78               | Sevilla          |


---

### 4. Empleados
Insertar **al menos dos empleados** con la siguiente estructura:

- Nombre
- Edad
- Departamento
- Puesto
- Salario
- Dirección (objeto embebido con):
  - Ciudad
  - Código Postal
  - Calle

| nombre | edad | departamento     | puesto                | salario | direccion.ciudad | direccion.codigoPostal | direccion.calle    |
| ------ | ---- | ---------------- | --------------------- | ------- | ---------------- | ---------------------- | ------------------ |
| Ana    | 45   | Recursos Humanos | Responsable RRHH      | 42000   | Madrid           | 28013                  | Paseo del Prado    |
| Miguel | 38   | Informática      | Desarrollador Backend | 36000   | Barcelona        | 08010                  | Calle Aragón       |
| Sofía  | 50   | Ventas           | Directora Comercial   | 50000   | Valencia         | 46001                  | Avenida del Puerto |


---

## Consultas a realizar

Realizar las siguientes consultas mediante comandos:

1. Mostrar todos los clientes.
2. Mostrar todos los empleados.
3. Mostrar los clientes con edad mayor de 30.
4. Mostrar los empleados con edad mayor de 40.
5. Mostrar los clientes que viven en una ciudad concreta.
6. Clientes menores de 40 años
7. Empleados del departamento de Informática
8. Clientes cuya ciudad sea Madrid o Valencia
9. Empleados mayores de 35 años y del departamento Ventas
10. Clientes mayores de 30 que viven en Sevilla
11. Empleados ordenados por salario (ascendente)
12. Empleados ordenados por salario (descendente)
13. Mostrar los 2 empleados mejor pagados
14. Contar clientes mayores de 30
15. Contar empleados por departamento (ej. Informática)
16. Mostrar nombre, puesto y salario de los empleados
17. Mostrar solo nombre y ciudad de los clientes
18. Mostrar solo nombre y edad de los empleados

---

## Comandos generales

Durante el ejercicio deberán utilizarse comandos como:

- `show dbs`
- `use`
- `show collections`
- `find()`
- `pretty()`
- `$gt`


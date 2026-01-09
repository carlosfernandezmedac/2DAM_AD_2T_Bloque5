# 🧪 Ejercicio práctico MongoDB — Clientes y Empleados (Enunciado)

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

---

## Consultas a realizar

Realizar las siguientes consultas mediante comandos:

1. Mostrar todos los clientes.
2. Mostrar todos los empleados.
3. Mostrar los clientes con edad mayor de 30.
4. Mostrar los empleados con edad mayor de 40.
5. Mostrar los clientes que viven en una ciudad concreta.
6. Mostrar solo el nombre y la edad de los empleados.

---

## Comandos generales

Durante el ejercicio deberán utilizarse comandos como:

- `show dbs`
- `use`
- `show collections`
- `find()`
- `pretty()`
- `$gt`


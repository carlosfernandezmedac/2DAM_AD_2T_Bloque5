# Tarea práctica MongoDB — Empleados (importación + consultas + índices + RBAC)

## Contexto
Ya existe la base de datos `miBD` y la colección `empleados`.  
Vas a importar un nuevo fichero JSON con empleados que incluye más campos (por ejemplo: `Nombre`, `Telefono`, `Edad` (en algunos documentos), `FechaRegistro`, `Departamento`, `Salario`, `Puesto` y un subdocumento `Dirección`).

El objetivo es practicar:
- Importación y verificación de datos
- Consultas con `find()`, filtros y ordenaciones
- Creación y borrado de índices
- Índices `unique`, `sparse`, compuestos y sobre campos embebidos
- Comprobación de rendimiento con `explain("executionStats")`
- Usuarios y roles (RBAC) si el servidor tiene autenticación habilitada

---

## Requisitos previos
- MongoDB instalado y acceso a `mongosh`
- El fichero de datos `tema13.empleados.json`

---

## Parte 1 — Base de datos e importación

### 1.1 Usar la base de datos
- Comprobar bases de datos existentes.
- Seleccionar la base de datos `miBD`.

### 1.2 Importar el JSON en la colección `empleados`
- Importar el fichero JSON en `miBD.empleados`.
- El fichero es un array JSON, así que debe importarse como JSON array.

### 1.3 Verificar la importación
- Mostrar colecciones.
- Contar documentos.

---

## Parte 2 — Consultas básicas (find)

Realiza las siguientes consultas sobre `miBD.empleados`:

1. Mostrar todos los empleados.
2. Mostrar los empleados de un departamento concreto (ej. `Ventas`).
3. Mostrar empleados con salario mayor o igual a 3000.
4. Mostrar empleados que tengan el campo `Edad` (solo los que lo tengan).
5. Mostrar empleados que NO tengan el campo `Edad`.
6. Buscar empleados por ciudad (campo embebido `Dirección.Ciudad`).


---

## Parte 3 — Índices (crear y probar)

### 3.1 Comprobar índices actuales
- Listar los índices actuales de `empleados`.

### 3.2 Índice monoclave por departamento
- Crear un índice ascendente por `Departamento`.
- Probar una consulta que se beneficie de este índice.

### 3.3 Índice compuesto Departamento + Salario
- Crear un índice compuesto que permita filtrar por `Departamento` y ordenar por `Salario` en orden descendente.
- Probar una consulta con `find + sort` que use este índice.

### 3.4 Índice en campo embebido (ciudad)
- Crear un índice sobre el campo embebido `Dirección.Ciudad`.
- Probar una consulta por ciudad.

### 3.5 Índice UNIQUE por teléfono
- Comprobar si existen teléfonos duplicados.
- Crear un índice `unique` sobre `Telefono`.
- Intentar insertar un documento con un `Telefono` ya existente y comprobar el error.

### 3.6 Índice SPARSE por edad
- Crear un índice `sparse` sobre `Edad`.
- Probar una consulta que filtre por `Edad` (por ejemplo, `Edad >= 30`).
- Explicar en 2-3 líneas qué documentos quedan fuera del índice sparse y por qué.


### 3.7 getIndexes()
- Captura/salida de `getIndexes()` al final.

---

## Parte 4 — Explain (uso de índices)

Ejecuta `explain("executionStats")` en estas consultas y responde:

1. Consulta por `Departamento`.
2. Consulta por `Departamento` + `sort` por `Salario`.
3. Consulta por `Dirección.Ciudad`.
4. Consulta por `Edad` (con el índice `sparse` creado).

Para cada una:
- Indica si aparece `IXSCAN` o `COLLSCAN`.
- Indica `totalDocsExamined` y `nReturned`.

---

## Parte 5 — Borrado de índices y mantenimiento

1. Listar índices.
2. Borrar un índice (por nombre).
3. Volver a listar índices para comprobar que se ha eliminado.

---

## Parte 6 — Usuarios y roles (RBAC) 

> Si tu MongoDB no tiene autenticación habilitada, indica "No disponible en mi entorno" y justifica en una frase.

1. Crear un usuario de solo lectura para la base de datos `miBD`.
2. Crear un usuario con permisos `readWrite` para `miBD`.
3. Crear un rol personalizado que permita:
   - leer (`find`)
   - listar índices
   - crear índices  
   sobre la colección `empleados`.
4. Crear un usuario que use ese rol y mostrar los privilegios del rol.

---



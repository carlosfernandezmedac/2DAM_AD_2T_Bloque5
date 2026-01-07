# 📘 Tema — Bases de Datos NoSQL

## 📑 Índice
- [1. Introducción a NoSQL](#1-introducción-a-nosql)
- [2. ¿Por qué NoSQL?](#2-por-qué-nosql)
- [3. Características principales](#3-características-principales)
- [4. Tipos de bases de datos NoSQL](#4-tipos-de-bases-de-datos-nosql)
  - [4.1. Clave–Valor](#41-clavevalor)
  - [4.2. Documentales](#42-documentales)
  - [4.3. Orientadas a columnas](#43-orientadas-a-columnas)
  - [4.4. Orientadas a grafos](#44-orientadas-a-grafos)
- [5. Comparación SQL vs NoSQL](#5-comparación-sql-vs-nosql)
- [6. Casos de uso habituales](#6-casos-de-uso-habituales)
- [7. Resumen final](#7-resumen-final)

---

## 1. Introducción a NoSQL

Las bases de datos **NoSQL (Not Only SQL)** surgen como alternativa a las bases de datos relacionales tradicionales.

No siguen estrictamente el modelo relacional y están diseñadas para:
- Grandes volúmenes de datos
- Alta escalabilidad
- Sistemas distribuidos

---

## 2. ¿Por qué NoSQL?

Las bases de datos relacionales presentan limitaciones cuando:
- Hay millones de usuarios concurrentes
- Los datos no tienen una estructura fija
- Se requiere alta disponibilidad

👉 NoSQL soluciona estos problemas mediante:
- Escalado horizontal
- Esquemas flexibles
- Alta tolerancia a fallos

---

## 3. Características principales

- ❌ No usan tablas ni JOINs complejos
- ✔ Escalado horizontal
- ✔ Alto rendimiento
- ✔ Esquema flexible
- ✔ Pensadas para sistemas distribuidos

---

## 4. Tipos de bases de datos NoSQL

### 4.1. Clave–Valor

Funcionan como un diccionario:

```
clave → valor
```

Ejemplo:
```
"user_1" → "{nombre: Ana, edad: 25}"
```

📌 Ejemplos:
- Redis
- DynamoDB

---

### 4.2. Documentales

Almacenan documentos (JSON / BSON).

```json
{
  "id": 1,
  "nombre": "Carlos",
  "email": "carlos@mail.com"
}
```

📌 Ejemplos:
- MongoDB
- CouchDB

---

### 4.3. Orientadas a columnas

Almacenan datos por columnas en lugar de filas.

📌 Ideales para:
- Big Data
- Analítica

Ejemplos:
- Cassandra
- HBase

---

### 4.4. Orientadas a grafos

Basadas en nodos y relaciones.

📌 Ideales para:
- Redes sociales
- Recomendaciones

Ejemplos:
- Neo4j
- Amazon Neptune

---

## 5. Comparación SQL vs NoSQL

| SQL | NoSQL |
|----|----|
| Modelo relacional | Modelo no relacional |
| Esquema fijo | Esquema flexible |
| JOINs | Sin JOINs |
| Escalado vertical | Escalado horizontal |
| ACID | BASE |

---

## 6. Casos de uso habituales

- Redes sociales
- Aplicaciones en tiempo real
- Big Data
- IoT
- Videojuegos online

---

## 7. Resumen final

```
NoSQL
 ├─ Clave–Valor
 ├─ Documentos
 ├─ Columnas
 └─ Grafos

Ventajas → escalabilidad, flexibilidad, rendimiento
Uso ideal → grandes volúmenes y sistemas distribuidos
```

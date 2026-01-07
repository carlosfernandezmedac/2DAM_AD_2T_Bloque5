# 📘 Tema 11 — Introducción a las Bases de Datos No‑SQL

## 📑 Índice
- [1. Introducción y contextualización práctica](#1-introducción-y-contextualización-práctica)
- [2. Características de las bases de datos No‑SQL](#2-características-de-las-bases-de-datos-no-sql)
- [3. Fundamentos de las bases de datos No‑SQL](#3-fundamentos-de-las-bases-de-datos-no-sql)
- [4. Beneficios de las bases de datos No‑SQL I](#4-beneficios-de-las-bases-de-datos-no-sql-i)
- [6. Beneficios de las bases de datos No‑SQL II](#6-beneficios-de-las-bases-de-datos-no-sql-ii)
- [7. Beneficios de las bases de datos No‑SQL III](#7-beneficios-de-las-bases-de-datos-no-sql-iii)
- [8. Tipos de bases de datos NoSQL](#8-tipos-de-bases-de-datos-nosql)
- [9. Introducción a Big Data](#9-introducción-a-big-data)
- [10. Tipos de Big Data](#10-tipos-de-big-data)
- [11. Caso práctico 2: Tipos de estructuras Big Data](#11-caso-práctico-2-tipos-de-estructuras-big-data)
- [12. Resumen final](#12-resumen-final)

---

## 1. Introducción y contextualización práctica

Las bases de datos **No‑SQL** surgen para dar respuesta a las limitaciones de las bases de datos relacionales tradicionales en escenarios con grandes volúmenes de datos, alta concurrencia y sistemas distribuidos.

🎯 Objetivos del tema:
- Conocer los fundamentos de las bases de datos No‑SQL
- Entender sus diferencias respecto a SQL
- Introducir el concepto de **Big Data**

---

## 2. Características de las bases de datos No‑SQL

Las bases de datos No‑SQL comparten una serie de características comunes:

- Modelo de datos **no relacional**
- Funcionan correctamente en **clusters**
- Generalmente **open‑source**
- Orientadas a aplicaciones web modernas
- **Ausencia de esquema** (*schemaless*)

### Conceptos clave
- **Cluster**: conjunto de nodos que funcionan como un único sistema
- **Schemaless**: permite almacenar datos no uniformes y evolucionar fácilmente

---

## 3. Fundamentos de las bases de datos No‑SQL

En los últimos años se ha producido un gran aumento en la cantidad de datos que se generan y se almacenan.
Este crecimiento está directamente relacionado con el auge de:

- Redes sociales
- Dispositivos móviles
- Sensores
- Sistemas GPS
- Aplicaciones web distribuidas

Estos sistemas generan **grandes volúmenes de información** de forma continua y, además, muchos de estos datos
no siguen una estructura fija.

Como consecuencia, aparecen tres tipos de datos:
- **Datos estructurados** (tablas tradicionales)
- **Datos semi-estructurados** (XML, JSON)
- **Datos no estructurados** (imágenes, vídeos, texto libre)

Las **bases de datos relacionales** requieren definir previamente un **esquema fijo** (tablas, columnas y tipos de datos),
lo que dificulta su uso cuando:
- La estructura de los datos cambia con frecuencia
- El volumen de información crece de forma masiva
- Se necesita escalar el sistema rápidamente

Para dar respuesta a estas limitaciones surgen las **bases de datos No-SQL**, cuyo objetivo principal es:

- Manejar grandes volúmenes de información
- Facilitar la **escalabilidad horizontal** mediante múltiples nodos
- Permitir trabajar con **datos heterogéneos**
- Ofrecer mayor flexibilidad en la estructura de los datos


| Bases de datos relacionales | Bases de datos No-SQL |
|-----------------------------|----------------------|
| La información se almacena en un modelo relacional con filas y columnas | La información se almacena usando distintos modelos de datos |
| Cada fila contiene información de un elemento y cada columna un atributo | Los datos pueden almacenarse como documentos, clave/valor, columnas o grafos |
| Sigue un esquema fijo definido previamente | Sigue un esquema dinámico (schemaless) |
| Es necesario definir las columnas antes de insertar los datos | Se pueden añadir nuevos campos en cualquier momento |
| Favorece el escalado vertical | Facilita el escalado horizontal mediante múltiples servidores |
| Basadas en los principios ACID | No están orientadas a cumplir estrictamente ACID |


---

## 4. Beneficios de las bases de datos No‑SQL I

### a) Fuente primaria y analítica
- Integración rápida de datos estructurados y no estructurados
- Consultas de alto rendimiento
- Uso en sistemas de *Business Intelligence*


### b) Capacidad Big Data

Las bases de datos No-SQL no se limitan únicamente a trabajar con pequeños conjuntos de datos.
Una solución No-SQL de nivel empresarial puede **escalar para gestionar volúmenes de información muy elevados**, desde **terabytes hasta petabytes**.

Entre sus principales ventajas en entornos Big Data destacan:
- Almacenamiento de grandes volúmenes de datos
- Alto rendimiento en operaciones de lectura y escritura
- Capacidad para manejar datos variados y complejos


### c) Disponibilidad continua

Para que una base de datos sea considerada de nivel empresarial, debe ofrecer **disponibilidad continua**,
evitando cualquier **punto único de fallo**.

Las bases de datos No-SQL integran esta característica directamente en el sistema y deben cumplir que:

1. Todos los nodos del clúster puedan atender peticiones de lectura, incluso si alguno falla.
2. Los datos puedan replicarse y distribuirse fácilmente entre distintos nodos y ubicaciones físicas.
3. Se admita la distribución de datos en **múltiples centros de datos**, tanto locales como en la nube.

Gracias a estas características, las bases de datos No-SQL garantizan un alto nivel de disponibilidad
y tolerancia a fallos.

---

## 6. Beneficios de las bases de datos No‑SQL II

### a) Capacidad de tener múltiples centros de datos

En entornos profesionales, las empresas suelen disponer de sistemas distribuidos
en **varios centros de datos** y ubicaciones geográficas diferentes.

Las bases de datos No-SQL permiten:
- Distribuir los datos entre distintos centros de datos
- Mantener un equilibrio entre **rendimiento y coherencia**
- Evitar problemas de latencia y cuellos de botella

A diferencia de muchas bases de datos relacionales, No-SQL ofrece un modelo
más sencillo y eficiente para la distribución de datos a gran escala.

---

### b) Fácil replicación independientemente de la ubicación

Una base de datos No-SQL proporciona una **alta capacidad de replicación**, lo que garantiza
la disponibilidad y seguridad de los datos.

Entre sus principales características destacan:
- Escritura y lectura de datos desde cualquier nodo del clúster
- Replicación automática de los datos en otros nodos
- Independencia de la ubicación física del usuario

Este modelo asegura que los datos permanezcan accesibles incluso ante
fallos de hardware, cortes eléctricos u otros incidentes.
---

## 7. Beneficios de las bases de datos No‑SQL III

### a) Sin capa de almacenamiento en caché separada

Las bases de datos No-SQL distribuyen los datos entre múltiples nodos,
permitiendo que la memoria de cada nodo actúe como caché.

Esto implica que:
- No es necesaria una capa de caché externa
- Se elimina la necesidad de sincronizar la caché con la base de datos
- Se simplifica la administración del sistema

---

### b) Preparadas para la nube

Las soluciones No-SQL están diseñadas para funcionar en **entornos cloud**,
como infraestructuras públicas, privadas o híbridas.

Permiten:
- Escalar o reducir nodos dinámicamente
- Ejecutarse en plataformas como Amazon EC2
- Combinar infraestructuras locales y en la nube

---

### c) Alto rendimiento con escalabilidad lineal

Las bases de datos No-SQL mejoran su rendimiento a medida que se añaden nodos al clúster.
Este comportamiento se conoce como **escalabilidad lineal**.

Sus ventajas principales son:
- Aumento del rendimiento en lectura y escritura
- Mejor aprovechamiento de los recursos
- Facilidad para crecer sin degradar el sistema

---

### Otros beneficios adicionales

- Soporte de esquemas flexibles
- Compatibilidad con múltiples lenguajes y plataformas
- Facilidad de implementación, mantenimiento y extensión
- Amplio respaldo de comunidades de código abierto

---

## 8. Tipos de bases de datos NoSQL

### Tipos principales

1. **Clave / Valor**
   - Funcionan como un diccionario o una agenda.
   - Redis, Riak, Memcached

Ejemplo cotidiano
   - La clave es el DNI
   - El valor es toda la información de la persona

```text
"user_1" → "Ana, 25 años, Madrid"
```

   

2. **Documentales**
   - Cada registro es como un documento (JSON).
   - MongoDB, CouchDB

Ejemplo:
```json
{
  "nombre": "Ana",
  "email": "ana@mail.com"
}

{
  "nombre": "Luis",
  "telefono": "123456"
}
```


3. **Orientadas a columnas**
   - Guardan los datos por columnas, no por filas
   
   📌 Ideales para:
      - Big Data
      - Analítica

   - Cassandra, HBase

   En vez de guardar:
      Persona 1 → todos sus datos
      Persona 2 → todos sus datos

   Guardan:
      Todos los nombres juntos
      Todas las edades juntas
      Todos los salarios juntos



4. **Orientadas a grafos**
   - Basadas en nodos y relaciones.

   📌 Ideales para:
      - Redes sociales
      - Recomendaciones
   
   - Neo4j

---

## 9. Introducción a Big Data

**Big Data** hace referencia a conjuntos de datos tan grandes que no pueden ser procesados con herramientas tradicionales.

Características:
- Gran volumen
- Crecimiento constante
- Datos heterogéneos

---

## 10. Tipos de Big Data

### a) Datos estructurados
- Tablas, bases de datos tradicionales

### b) Datos no estructurados
- Imágenes, vídeos, texto libre

### c) Datos semi‑estructurados
- XML, JSON

---

## 11. Caso práctico 2: Tipos de estructuras Big Data

Clasificación de ejemplos reales:
- Tablas → estructurados
- XML → semi‑estructurados
- Resultados web → no estructurados

---

## 12. Resumen final

```
No‑SQL
 ├─ Clave / Valor
 ├─ Documentos
 ├─ Columnas
 └─ Grafos

Big Data
 ├─ Estructurados
 ├─ Semi‑estructurados
 └─ No estructurados
```

✔ Pensadas para grandes volúmenes
✔ Escalables horizontalmente
✔ Clave en sistemas modernos

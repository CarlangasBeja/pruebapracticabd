# Prueba Práctica Avanzada — Oracle SQL

## Universidad Técnica de Ambato
Facultad de Ingeniería en Sistemas  
Asignatura: Bases de Datos  
Docente: José Caiza  

---

## Estudiante
Carlos Fabian Bejarano Masabanda

---

## Escenario
Aeropuerto Internacional

---

## Tipo de Integridad
ON DELETE CASCADE

---

# Descripción

Este proyecto corresponde al desarrollo de la prueba práctica avanzada de Oracle SQL, donde se implementa un sistema de gestión para un Aeropuerto Internacional utilizando:

- Modelado lógico
- Restricciones de integridad
- Relaciones entre tablas
- Consultas SQL
- Integridad referencial
- Uso de ON DELETE CASCADE

---

# Entidades Implementadas

- AVION
- AEROLINEA
- PASAJERO
- VUELO
- BOLETO
- EQUIPAJE

---

# Tecnologías Utilizadas

- Oracle SQL Plus
- Oracle Database
- GitHub

---

# Estructura del Proyecto

```text
Proyecto_Oracle_SQL/
│
├── README.md
├── ddl.sql
├── dml.sql
├── consultas.sql
├── analisis.txt
│
├── capturas/
│   ├── tablas_creadas.png
│   ├── inserts.png
│   ├── consultas_join.png
│   └── desarrollo_manual.jpg
```

---

# Funcionalidades Realizadas

## DDL
- Creación de tablas
- Claves primarias
- Claves foráneas
- Restricciones CHECK
- Restricciones UNIQUE
- Restricciones NOT NULL

## DML
- Inserciones válidas
- Actualizaciones seguras
- Eliminaciones con integridad referencial
- Simulación del error ORA-02291

## Consultas SQL
- IN
- LIKE
- BETWEEN
- MAX
- JOIN

---

# Ejemplo de JOIN

```sql
SELECT
    p.nombres,
    p.apellido,
    v.ciudad_destino,
    a.nombre AS aerolinea,
    av.modelo AS avion,
    b.numero_asiento
FROM PASAJERO p
JOIN BOLETO b
    ON p.id_pasajero = b.id_pasajero
JOIN VUELO v
    ON b.id_vuelo = v.id_vuelo
JOIN AEROLINEA a
    ON v.id_aerolinea = a.id_aerolinea
JOIN AVION av
    ON v.id_avion = av.id_avion;
```

---

# Análisis Profesional

## Atomicidad
Garantiza que una transacción se complete totalmente o no se ejecute.

## DELETE sin WHERE
Elimina todos los registros de una tabla y puede causar pérdida masiva de datos.

## ON DELETE CASCADE
Permite eliminar automáticamente los registros hijos relacionados con un registro padre.

---

# Evidencias Incluidas

- Scripts SQL
- Capturas Oracle
- Desarrollo manual
- Consultas ejecutadas
- Evidencias GitHub

---

# Commits Realizados

```bash
git commit -m "Creacion de tablas y restricciones"
git commit -m "Inserciones y pruebas de integridad"
git commit -m "Consultas SQL y evidencias finales"
```

---

# Resultado

Proyecto funcional desarrollado en Oracle SQL aplicando integridad referencial y consultas avanzadas para el escenario Aeropuerto Internacional.

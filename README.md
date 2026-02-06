# Automatización de Datos en Odoo con Python (ETL)

## Descripción

Este proyecto consiste en desarrollar un script en Python que importa datos de centros educativos desde un archivo CSV (`listado.csv`) a la base de datos PostgreSQL utilizada por Odoo en Docker.

El script realiza un proceso ETL:

* **Extracción:** Lee el archivo CSV.
* **Transformación:** Prepara los datos usando Pandas.
* **Carga:** Inserta los datos en PostgreSQL en la tabla `import_centros`.

---

## Tecnologías utilizadas

* Python 3.10+
* Pandas
* psycopg2-binary
* PostgreSQL
* Docker
* Odoo
* pgAdmin
* Git y GitHub

---

## Archivos del proyecto

```
importar.py      → Script que importa los datos
listado.csv     → Archivo con los centros educativos
README.md      → Documentación del proyecto
captura.png    → Captura del resultado
```

---

## Configuración

### 1. Instalar dependencias

Abrir terminal en la carpeta del proyecto y ejecutar:

```
pip install pandas psycopg2-binary
```

---

### 2. Verificar que Docker está activo

Comprobar que PostgreSQL y Odoo están funcionando:

```
docker ps
```

---

## Ejecución

Ejecutar el script:

```
python importar.py
```

Salida esperada:

```
CSV leído correctamente
Datos insertados correctamente
```

---

## Funcionamiento del Script

El script realiza las siguientes acciones:

1. Lee el archivo CSV usando codificación latin1.
2. Se conecta a PostgreSQL usando las credenciales de Odoo.
3. Crea la tabla `import_centros` si no existe.
4. Inserta los datos usando un bucle.
5. Guarda los cambios en la base de datos.

---

## Verificación en pgAdmin

Abrir pgAdmin y ejecutar:

```
SELECT * FROM import_centros;
```

Se deben ver los datos importados correctamente.

# Colecciones CRUD en Postman + JSON Server

Este proyecto contiene un conjunto de **10 colecciones de Postman** junto con una base de datos simulada (`db.json`) diseñada para practicar y validar operaciones **CRUD** (`GET`, `POST`, `PUT`, `PATCH` y `DELETE`) sobre distintas entidades de negocio utilizando **JSON Server**.

---

## 📁 Estructura del Proyecto

```text
10_coleccciones_en_postman_tl-/
├── colecciones/                        # Carpeta con las 10 colecciones de Postman (v2.1)
│   ├── 01 - Productos.postman_collection.json
│   ├── 02 - Usuarios.postman_collection.json
│   ├── 03 - Compañias.postman_collection.json
│   ├── 04 - Empleados.postman_collection.json
│   ├── 05 - Clientes.postman_collection.json
│   ├── 06 - Proveedores.postman_collection.json
│   ├── 07 - Libros.postman_collection.json
│   ├── 08 - Cursos.postman_collection.json
│   ├── 09 - Vehículos.postman_collection.json
│   └── 10 - Pedidos.postman_collection.json
├── db.json                             # Base de datos simulada para JSON Server
└── README.md                           # Documentación del proyecto
```

---

## 📋 Entidades y Endpoints Incluidos

Cada colección cubre los métodos HTTP estándar sobre su respectivo recurso:

| # | Entidad | Endpoint Base | Operaciones Incluidas |
| :- | :--- | :--- | :--- |
| 01 | **Productos** | `/productos` | Listar todos, Buscar por ID, Crear, Reemplazar, Actualizar parcialmente, Eliminar |
| 02 | **Usuarios** | `/usuarios` | Listar todos, Buscar por ID, Crear, Reemplazar, Actualizar parcialmente, Eliminar |
| 03 | **Compañias** | `/companias` | Listar todos, Buscar por ID, Crear, Reemplazar, Actualizar parcialmente, Eliminar |
| 04 | **Empleados** | `/empleados` | Listar todos, Buscar por ID, Crear, Reemplazar, Actualizar parcialmente, Eliminar |
| 05 | **Clientes** | `/clientes` | Listar todos, Buscar por ID, Crear, Reemplazar, Actualizar parcialmente, Eliminar |
| 06 | **Proveedores** | `/proveedores` | Listar todos, Buscar por ID, Crear, Reemplazar, Actualizar parcialmente, Eliminar |
| 07 | **Libros** | `/libros` | Listar todos, Buscar por ID, Crear, Reemplazar, Actualizar parcialmente, Eliminar |
| 08 | **Cursos** | `/cursos` | Listar todos, Buscar por ID, Crear, Reemplazar, Actualizar parcialmente, Eliminar |
| 09 | **Vehículos** | `/vehiculos` | Listar todos, Buscar por ID, Crear, Reemplazar, Actualizar parcialmente, Eliminar |
| 10 | **Pedidos** | `/pedidos` | Listar todos, Buscar por ID, Crear, Reemplazar, Actualizar parcialmente, Eliminar |

---

## 🚀 Requisitos Previos

* [Node.js](https://nodejs.org/) (v18 o superior)
* [JSON Server](https://github.com/typicode/json-server) instalado de forma global o local en el proyecto
* [Postman](https://www.postman.com/) (aplicación de escritorio o versión web)

---

## ⚙️ Cómo Ejecutar el Servidor Local

1. Ubícate en la carpeta donde se encuentra `db.json`:
   ```bash
   cd 10_coleccciones_en_postman_tl-
   ```

2. Levanta la API simulada con `json-server`:
   ```bash
   npx json-server --watch db.json --port 3000
   ```

3. Verifica que el servidor esté corriendo en:
   ```text
   http://localhost:3000
   ```

---

## 🧪 Cómo Importar y Probar en Postman

1. Abre **Postman** y haz clic en **Import** (Importar).
2. Selecciona la carpeta que contiene los 10 archivos `.postman_collection.json`.
3. Crea un **Environment** (entorno) en Postman con la siguiente variable:
   * **Variable:** `baseUrl`
   * **Initial / Current Value:** `http://localhost:3000`
4. Activa el entorno creado en la esquina superior derecha de Postman y ejecuta las peticiones de cada colección.

---

## 💡 Notas Técnicas

* En `db.json`, la colección de compañías está definida bajo la clave `"companias"` (sin `ñ`) y vehículos bajo `"vehiculos"` (sin tilde) para evitar problemas de codificación en las URLs de las peticiones HTTP.
* Al realizar peticiones `POST`, `PUT` o `PATCH`, asegúrate de enviar el cuerpo en formato `raw` -> `JSON` con el encabezado `Content-Type: application/json`.
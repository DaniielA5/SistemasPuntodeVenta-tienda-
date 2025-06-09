# 🎨 Sistema Punto de Venta — "Mas cerca de ti"

Sistema de punto de venta (POS) para una zapatería llamado **"Tienda de tenis"**, desarrollado en **Java** con **Swing (JFrame)** y conectado a **PostgreSQL**. El proyecto se implementó en **NetBeans** y soporta múltiples roles de usuario con permisos específicos.

---

## 📋 Contenido

1. [Descripción](#descripción)
2. [Flujo de Inicio de Sesión](#flujo-de-inicio-de-sesión)
3. [Roles y Permisos](#roles-y-permisos)
4. [Características Principales](#características-principales)
5. [Tecnologías](#tecnologías)
6. [Requisitos Previos](#requisitos-previos)
7. [Instalación y Configuración](#instalación-y-configuración)
8. [Estructura del Proyecto](#estructura-del-proyecto)
9. [Uso](#uso)
10. [Capturas de Pantalla](#capturas-de-pantalla)
11. [Créditos](#créditos)
12. [Estado del Proyecto](#estado-del-proyecto)

---

## 📌 Descripción

"Tienda Tenis" es una aplicación de escritorio para gestionar las operaciones de una zapatería. Permite la administración de productos, clientes, ventas y usuarios, con un sistema robusto de roles y permisos.

## 🔒 Flujo de Inicio de Sesión

1. **Captcha Inicial**: El usuario resuelve un captcha para evitar accesos automatizados.
2. **Formulario de Login**: Tras el captcha, se abre la ventana de inicio de sesión.
3. **Validación de Credenciales**: Si las credenciales son correctas, el sistema verifica el rol y redirige al usuario al panel correspondiente.

## 👥 Roles y Permisos

* **Administrador**

  * Acceso completo al sistema.
  * Gestión de productos: añadir, eliminar, editar y vender.
  * Gestión de usuarios: crear, modificar y eliminar cuentas.
* **Cajero**

  * Solo puede procesar ventas.
* **Bodeguero**

  * Solo puede añadir nuevos productos al inventario.

## ✨ Características Principales

* **Gestión de Productos**: CRUD completo (Crear, Leer, Actualizar, Eliminar).
* **Proceso de Venta**: Selección de productos, cálculo automático de totales e impresión de ticket.
* **Seguridad**: Captcha en login y autenticación por roles.
* **Reportes**: Consulta de historial de ventas.

## 🛠 Tecnologías

* **Lenguaje**: Java 8+
* **IDE**: NetBeans
* **UI**: Swing (JFrame, JPanel)
* **Base de Datos**: PostgreSQL
* **Conexión**: JDBC PostgreSQL Driver

## ⚙️ Requisitos Previos

* Java JDK 8 o superior
* PostgreSQL 9.6 o superior
* NetBeans IDE (o similar)

## 🚀 Instalación y Configuración

1. Clonar el repositorio:

   ```bash
   git clone https://github.com/DaniielA5/SistemasPuntodeVenta-tienda-.git
   ```
2. Abrir el proyecto en NetBeans.
3. Importar el script de la base de datos (`database/schema.sql`) en PostgreSQL:

   ```sql
   CREATE DATABASE tienda_tenis;
   \c tienda_tenis;
   -- Ejecutar tablas: productos, usuarios, ventas, etc.
   ```
4. Configurar la conexión en `Conexion.java`:

   ```java
   private static final String URL = "jdbc:postgresql://localhost:5432/tienda_tenis";
   private static final String USER = "TU_USUARIO";
   private static final String PASS = "TU_CONTRASEÑA";
   ```
5. Ejecutar la clase principal (`Main.java`) para iniciar la aplicación.

## 📂 Estructura del Proyecto

```
├── src
│   ├── app           # Punto de entrada y utilidades
│   ├── ui            # Formularios Swing (.java + .form)
│   ├── model         # Clases de entidad (Producto, Venta, Usuario)
│   └── dao           # Acceso a datos (DAO JDBC)
├── database
│   └── schema.sql    # Script de creación de tablas
└── README.md         # Documentación del proyecto
```

## 🎯 Uso

1. Resuelve el captcha y autentícate.
2. Al ingresar, serás dirigido según tu rol:

   * **Administrador**: Panel completo con módulos de Usuarios y Productos.
   * **Cajero**: Módulo de Ventas.
   * **Bodeguero**: Módulo de Registro de Productos.
3. Navega entre pestañas, completa formularios y confirma acciones.

## 🖼 Capturas de Pantalla

![Captcha](ruta/a/captura_captcha.png)
![Login](ruta/a/captura_login.png)
![Panel Admin](ruta/a/captura_admin.png)

## 👥 Créditos

* **Juarez Ramirez Daniel Alexis**
* **Bautista Centeno Francisco Elias**



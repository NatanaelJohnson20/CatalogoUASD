# Catálogo de Carreras - UASD

Aplicación de escritorio desarrollada en **Java** (Swing/JDBC) conectada a **MySQL** que permite consultar de manera dinámica la oferta académica de la **Universidad Autónoma de Santo Domingo (UASD)** organizada por facultades y escuelas.

---

## 📋 Descripción del Proyecto

Este programa cumple con el requerimiento de gestionar y consultar el catálogo de carreras ofertadas por la UASD almacenadas en una base de datos relacional. A través de una interfaz gráfica intuitiva, el usuario puede filtrar y visualizar las carreras disponibles según su facultad y escuela correspondiente.

### Características principales
* **Conexión a Base de Datos:** Integración mediante JDBC (`mysql-connector-j`) utilizando consultas preparadas (`PreparedStatement`) para mayor seguridad y rendimiento.
* **Filtrado Jerárquico:** Carga dinámica de **Facultades**, **Escuelas** y **Carreras** mediante listas desplegables (`JComboBox`) y tablas/resultados en tiempo real.
* **Base de Datos Relacional:** Estructura normalizada con integridad referencial entre las tablas `Facultades`, `Escuelas` y `Carreras`.

---

## 🛠️ Tecnologías Utilizadas

* **Lenguaje:** Java (JDK 17 / 21)
* **IDE:** Apache NetBeans
* **Interfaz Gráfica:** Java Swing
* **Base de Datos:** MySQL / MySQL Workbench
* **Driver de Conexión:** MySQL Connector/J

---

## 🗄️ Estructura de la Base de Datos

El esquema `CatalogoUASD` está compuesto por tres tablas principales relacionadas mediante llaves foráneas:

1. **`Facultades`**: Almacena las distintas facultades de la universidad (`Facultadid`, `Nombre`).
2. **`Escuelas`**: Contiene las escuelas adscritas a cada facultad (`Escuelaid`, `Nombre`, `Facultadid`).
3. **`Carreras`**: Registra las carreras ofertadas por cada escuela (`Carreraid`, `Nombre`, `Escuelaid`).

---

## 🚀 Instalación y Configuración

Sigue estos pasos para ejecutar el proyecto en tu entorno local:

### 1. Clonar el repositorio
```bash
git clone https://github.com
```

### 2. Configurar la Base de Datos
1. Abre **MySQL Workbench** e inicia sesión en tu servidor local (`localhost:3306`).
2. Abre el archivo `.sql` incluido en el repositorio (dentro de la carpeta `database/` o en la raíz del proyecto).
3. Ejecuta el script completo para crear la base de datos `CatalogoUASD`, sus tablas e insertar los registros iniciales.

### 3. Configurar el Proyecto en NetBeans
1. Abre **Apache NetBeans** y selecciona **File -> Open Project...** para abrir la carpeta clonada.
2. Verifica que el driver **`mysql-connector-j-x.x.x.jar`** esté agregado en la carpeta **Libraries** del proyecto (si aparece con advertencia, haz clic derecho -> *Resolve Reference Problems* y selecciona tu archivo `.jar` local).
3. Abre la clase `Conexion.java` y actualiza las credenciales de acceso a tu servidor MySQL:
   ```java
   private static final String URL = "jdbc:mysql://localhost:3306/CatalogoUASD";
   private static final String USER = "root";
   private static final String PASSWORD = "tu_contraseña_mysql";
   ```


## 👥 Autores

* **Breidy Vasquez Delgado** - *Desarrollo y Base de Datos* - [@Breidy-V ](https://github.com/Breidy-V)
* **Ronald A. Haché Mármol** - *Desarrollo e Interfaz* - [@Dizzzy1](https://github.com/Dizzzy1)
* **Leticia M. Evertsz Mejia** - *Desarrollo y Base de Datos***** - [@](https://github.com)
* **Natanael Johnson** - *Desarrollo e Interfaz* - [@NatanaelJohnson20](https://github.com/NatanaelJohnson20)
* **José M. De La Cruz Almonte** - *Desarrollo y Base de Datos* - [@](https://github.com)


---

## 📄 Licencia

Este proyecto fue desarrollado con fines académicos para la **Universidad Autónoma de Santo Domingo (UASD)**.

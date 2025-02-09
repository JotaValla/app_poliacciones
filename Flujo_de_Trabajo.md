# Flujo de Trabajo

## Roles y Responsabilidades

### Paola Gamboa y Alexander Morales
- Serán responsables del diseño en HTML y la implementación de los estilos CSS para la aplicación.

### Jimmy Valladares
- Será responsable del desarrollo del backend.
- Implementará las funcionalidades principales de la lógica del negocio utilizando Java y el framework Spring Boot.

### Santiago Torres
- Será responsable de la documentación del proyecto, que incluirá:
  - Historias de usuario.
  - Diagramas UML, como el diagrama de clases y el modelo entidad-relación.
  - Documentación técnica de estándares de codificación y mejores prácticas.

---
### Version 2:
   ### Santiago Torres y Paola Gamboa
   - Serán los responsables de la documentación del proyecto, que incluirá:
      - Actualizar los documentos necesarios.
      - Cambios Requeridos
      - Analisis del impacto de las solicitudes de cambio.

## Herramientas y Tecnologías

### Backend:
- **Lenguaje de Programación**: Java.
- **Framework**: Spring Boot.
- **Spring Security**: Para la integración de filtros de seguridad, configuración de accesos (SecurityConfig) y protección de endpoints.
- **JWT (JSON Web Token)**: Se utilizará para la autenticación y autorización, garantizando sesiones seguras a través de tokens.
- **Spring Data**: Se usará la interfaz `Page` para gestionar respuestas paginadas, en lugar de devolver listas completas, mejorando la eficiencia en el manejo de grandes volúmenes de datos.
- **DTO (Data Transfer Object)**: Se implementarán para facilitar la transferencia eficiente de datos entre el backend y el frontend, especialmente en la consolidación de acciones.

### Dependencias:
- **spring-boot-starter-data-jpa**: Para la gestión de datos.
- **spring-boot-starter-web**: Para la construcción de API REST.
- **Lombok**: Para simplificar el código reduciendo el boilerplate.
- **jakarta.validation-api** y **hibernate-validator**: Para validaciones.
- **mysql-connector-j**: Para la conexión a la base de datos MySQL.

### Gestión de Base de Datos:
- **Base de datos relacional** MySQL.

### Frontend:
- HTML y estilos definidos mediante **CSS**.

### Control de Versiones:
- **Git** se utilizará para la gestión del código fuente.
- El repositorio estará alojado en **GitHub**.

### Gestión de Dependencias:
- **Maven** será la herramienta de construcción utilizada para manejar las dependencias y empaquetar la aplicación.

### Integración con APIs Externas:
- **Tiingo API**:
  - Se integrará para obtener datos financieros en tiempo real e históricos sobre precios de acciones.


## Modelo Vista Controlador (MVC)
- El sistema se desarrollará siguiendo el patrón de diseño **Modelo Vista Controlador (MVC)**, lo que permitirá una clara separación de responsabilidades entre la lógica de negocio, la interfaz de usuario y el control del flujo de la aplicación.

## Estructura del Repositorio

El repositorio principal (`app_poliacciones`) cuenta con **dos ramas principales** y utiliza **submódulos** para integrar los componentes del **frontend** y el **backend**.

1. **main**  
   - Contiene los submódulos que apuntan al código fuente del **backend** (`poliacciones_backend`) y del **frontend** (`poliacciones_front`).
   - Es la rama principal para la integración de ambos componentes y para la entrega de la aplicación en producción.

2. **docs**  
   - Contiene los submódulos del **backend** y **frontend**, junto con toda la documentación del proyecto.
   - Aquí se almacenan archivos como:
     - Historias de usuario.
     - Diagramas UML (diagrama de clases, modelo entidad-relación, etc.).
     - Documentación técnica (estándares de codificación, mejores prácticas, etc.).

#### Uso de Submódulos

El repositorio utiliza submódulos para integrar los repositorios independientes del **backend** y el **frontend**. Esto permite una gestión modular del proyecto, facilitando la colaboración y la separación de responsabilidades.

---
## Actualizaciones Clave del Proyecto

- **JWT y Filtros de Seguridad:**  
  Se ha integrado el uso de JWT para la autenticación, permitiendo que el token se envíe en el encabezado de las solicitudes. Además, se ha implementado un filtro de seguridad junto con una clase `SecurityConfig` para controlar y restringir el acceso a los endpoints de la aplicación.

- **Paginación con Page en vez de List:**  
  En el backend, se utiliza la interfaz `Page` de Spring Data para devolver resultados paginados, en lugar de listas completas. Esto mejora el rendimiento y la experiencia del usuario al manejar grandes volúmenes de datos.

- **Uso de DTOs:**  
  Se han implementado Data Transfer Objects (DTO) para la consolidación de acciones y otros procesos de transferencia de datos, asegurando una comunicación eficiente y estructurada entre el backend y el frontend.




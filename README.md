# ProyectoFinal_MoisesR_IIS
# Resumen General del Proyecto de Control de Asistencia

## 1. Propósito y Alcance del Sistema

El propósito principal del sistema es **automatizar el registro de asistencia** de los estudiantes en clases, buscando **reducir errores humanos** y **mejorar la gestión académica**.

* El alcance incluye el registro de asistencia diaria, la identificación de los estudiantes mediante un código o credencial, y la generación de reportes para los docentes.
* No incluye integración con plataformas externas ni funciones de administración de calificaciones.
* Los usuarios principales son los **docentes**, que registrarán la asistencia de manera rápida, y los **administradores académicos**, que podrán consultar reportes globales de asistencia.

---

## 2. Requerimientos del Sistema

El sistema cuenta con requerimientos funcionales (RF) y no funcionales (RNF):

### Requerimientos Funcionales
1.  **RF1**: Permitir el inicio de sesión de los docentes mediante usuario y contraseña.
2.  **RF2**: Registrar la asistencia de los estudiantes por fecha y curso.
3.  **RF3**: Editar o corregir el registro de asistencia de un estudiante.
4.  **RF4**: Generar un reporte de asistencia por estudiante y por curso.
5.  **RF5**: Marcar la asistencia de manera automática mediante código QR o identificación única.

### Requerimientos No Funcionales
1.  **RNF1**: El registro de asistencia debe realizarse en **menos de 3 segundos** por estudiante.
2.  **RNF2**: Proteger las credenciales de usuario mediante **encriptación**.
3.  **RNF3**: La interfaz debe ser **intuitiva y fácil de usar** para docentes sin experiencia técnica.

---

## 3. Resultados de Pruebas y Criterios de Aceptación

Las pruebas realizadas (Unitarias y de Validación) permiten confirmar que el sistema **cumple con los requerimientos definidos**.

* Los resultados obtenidos para el inicio de sesión (RF1) y registro (RF2) fueron correctos.
* La actualización de registros (RF3) fue correcta.
* El registro masivo de asistencia mediante lector QR (CV1, asociado a RF5/RNF1) fue **exitoso**, cumpliendo con el tiempo esperado de menos de 3 segundos.
* La validación de usuario con conexión cifrada (CV2, asociado a RF1/RNF2) fue **exitosa**.

El sistema cumple con los **criterios de aceptación**, permitiendo el ingreso solo a usuarios autenticados y la modificación de registros sin pérdida de información.

---

## 4. Propuesta de Mantenimiento

Se proponen acciones de mantenimiento para abordar la seguridad y la funcionalidad de los reportes:

### Problema de Seguridad Vaga y Riesgosa
El sistema de acceso requiere solo una contraseña, lo que genera una debilidad crítica.

* **Mantenimiento Preventivo**: Implementar **políticas de contraseñas robustas** y gestión segura de sesiones.
* **Mantenimiento Perfectivo**: Añadir **Autenticación Multifactor (2FA)** para optimizar la seguridad.

### Problema de Reportes Tarde y Poco Útiles
El sistema solo genera un reporte simple de porcentaje de asistencia al final del semestre, impidiendo la intervención temprana.

* **Mantenimiento Perfectivo**: Agregar un **Módulo de Reportes de Alerta de Ausencias Frecuentes** (reportes intermedios). Esto optimiza el sistema para ser más útil para los profesores.

---

## 5. Nota sobre Markdown

Markdown es un lenguaje de marcado ligero desarrollado para que el texto sea fácil de leer y escribir. Se ha convertido en un **estándar para la documentación en el desarrollo de software** (como archivos `README.md`) debido a su sencillez y compatibilidad.

* **GitHub Flavored Markdown (GFM)** es una variante que añade funciones como tablas y referencias a usuarios o *issues*.
* Entre sus **ventajas** se encuentra la claridad de lectura en cualquier entorno y la rapidez al redactar.
* Una **desventaja** es su capacidad limitada para diseños muy elaborados, donde se requiere combinarlo con HTML.


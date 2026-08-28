# Sistema Móvil de Control de Asistencia

## M1 – Borrador del proyecto de aplicación Android

### Descripción general

Este proyecto propone el desarrollo de una aplicación móvil para dispositivos Android destinada al control básico de asistencia de participantes en una actividad, reunión o grupo.

La aplicación permitirá registrar temporalmente los nombres de los participantes, indicar si cada persona se encuentra **presente** o **ausente**, modificar la información ingresada, eliminar registros y visualizar un resumen general de la asistencia.

El proyecto está pensado para desarrollarse en un período aproximado de **cinco a seis semanas**, por lo que se ha definido un alcance sencillo y realista. La primera versión **no utilizará base de datos**, servidores externos ni servicios en la nube. La información se mantendrá únicamente durante la sesión activa de la aplicación.

---

## 1. Descripción del proyecto

La aplicación, denominada provisionalmente **Sistema Móvil de Control de Asistencia**, permitirá crear una sesión de asistencia e ingresar manualmente los nombres de los participantes.

Cada participante podrá ser identificado como:

- Presente
- Ausente

La aplicación mostrará automáticamente:

- Total de participantes
- Total de presentes
- Total de ausentes

También permitirá modificar un participante, cambiar su estado de asistencia, eliminar registros ingresados por error y consultar un resumen general de la sesión.

Además, se incluirá una opción para compartir el resumen utilizando las funciones disponibles en Android y otras aplicaciones instaladas en el dispositivo.

La información no será almacenada permanentemente. Los datos existirán únicamente durante la sesión activa y podrán eliminarse al iniciar una nueva sesión.

---

## 2. Exposición del problema

El control de asistencia todavía puede realizarse mediante hojas de papel, listas impresas o anotaciones manuales. Aunque estos métodos pueden funcionar en actividades pequeñas, también pueden generar inconvenientes como:

- Errores al escribir nombres
- Registros duplicados
- Dificultad para realizar conteos rápidos
- Confusión al modificar información
- Pérdida de tiempo al preparar un resumen final

La aplicación propuesta busca facilitar este proceso mediante una interfaz móvil sencilla que permita registrar participantes y obtener automáticamente los resultados de asistencia.

### Problema principal

> **¿Cómo facilitar el registro y conteo de asistencia de los participantes de una actividad mediante una aplicación Android sencilla y fácil de utilizar?**

La solución permitirá realizar estas tareas desde un solo dispositivo, reduciendo cálculos manuales y proporcionando un resumen inmediato de la sesión.

---

## 3. Objetivo general

Desarrollar una aplicación móvil Android sencilla que permita registrar participantes, controlar su asistencia y generar un resumen inmediato de una actividad sin necesidad de utilizar una base de datos.

### Objetivos específicos

- Diseñar una interfaz sencilla y comprensible.
- Permitir el ingreso temporal de participantes.
- Registrar estados de presente y ausente.
- Calcular automáticamente los resultados de asistencia.
- Permitir la modificación de participantes.
- Permitir la eliminación de registros.
- Generar un resumen de la sesión.
- Permitir compartir el resumen mediante las herramientas disponibles en Android.
- Aplicar los conocimientos adquiridos durante el curso.

---

## 4. Plataforma

La aplicación será desarrollada específicamente para **Android**.

### Herramientas y tecnologías

#### Android Studio
Será el entorno de desarrollo utilizado para crear, ejecutar, probar y depurar la aplicación.

#### Kotlin
Será el lenguaje de programación principal utilizado para implementar la lógica de la aplicación.

#### XML
Se utilizará para definir la estructura visual de las pantallas, incluyendo botones, campos de entrada, textos y listas.

#### Android SDK
Proporcionará las herramientas y componentes necesarios para utilizar las funciones del sistema Android.

#### Git y GitHub
GitHub será utilizado para:

- Mantener organizado el proyecto.
- Controlar versiones.
- Documentar el progreso.
- Publicar el archivo `README.md`.
- Mantener evidencia del desarrollo durante el curso.

### Almacenamiento

La primera versión **no utilizará base de datos**.

Los participantes y estados de asistencia se mantendrán temporalmente mientras la aplicación se encuentre en ejecución.

---

## 5. Interfaz de usuario

La interfaz principal permitirá realizar las operaciones básicas de la sesión de asistencia.

El usuario podrá:

- Crear una nueva sesión.
- Ingresar el nombre de un participante.
- Agregar participantes.
- Marcar participantes como presentes o ausentes.
- Visualizar los totales.
- Consultar el resumen.
- Compartir el resumen.

La navegación será sencilla y evitará menús innecesariamente complejos.

---

## 6. Interfaz de administrador

Debido al alcance sencillo de la aplicación, no se implementará un sistema de autenticación o roles.

La interfaz administrativa estará integrada dentro de la misma aplicación y permitirá:

- Agregar participantes.
- Editar nombres.
- Cambiar estados de asistencia.
- Eliminar participantes.
- Consultar resultados.
- Reiniciar completamente la sesión.

Una versión futura podría incorporar usuarios y permisos, pero estas funciones se encuentran fuera del alcance inicial.

---

## 7. Funcionalidad

### Crear sesión

El usuario podrá comenzar una nueva sesión de asistencia.

### Agregar participantes

El usuario ingresará el nombre de una persona mediante un campo de texto.

La aplicación validará que el campo no se encuentre vacío.

### Visualizar participantes

Los participantes aparecerán en una lista dentro de la aplicación.

Cada registro mostrará:

- Nombre
- Estado de asistencia
- Opción de edición
- Opción de eliminación

### Marcar asistencia

Cada participante podrá identificarse como:

- **Presente**
- **Ausente**

### Conteo automático

La aplicación calculará automáticamente:

- Total de participantes
- Total de presentes
- Total de ausentes

### Modificación

Será posible modificar el nombre de un participante o cambiar su estado.

### Eliminación

El usuario podrá eliminar participantes registrados accidentalmente.

### Resumen

Se mostrará una pantalla con los resultados generales de la sesión.

### Compartir

El resumen podrá compartirse utilizando aplicaciones compatibles instaladas en Android.

### Reiniciar sesión

El usuario podrá eliminar la información temporal y comenzar una nueva sesión.

---

## 8. Diseño de la aplicación

La interfaz seguirá tres principios principales:

### Simplicidad
Las funciones principales estarán claramente identificadas.

### Consistencia
Las pantallas utilizarán una estructura visual similar.

### Facilidad de navegación
El usuario podrá desplazarse fácilmente entre las funciones principales.

### Componentes de Android previstos

- `TextView`
- `EditText`
- `Button`
- `RecyclerView`
- `CardView`
- `RadioButton`
- `Toolbar`

---

# Wireframes

## Pantalla 1 – Inicio

```text
┌────────────────────────────────┐
│                                │
│       CONTROL DE ASISTENCIA    │
│                                │
│     Registro sencillo de       │
│        participantes           │
│                                │
│ ┌────────────────────────────┐ │
│ │    NUEVA ASISTENCIA        │ │
│ └────────────────────────────┘ │
│                                │
│ ┌────────────────────────────┐ │
│ │     ADMINISTRACIÓN         │ │
│ └────────────────────────────┘ │
│                                │
└────────────────────────────────┘
```

---

## Pantalla 2 – Registro de asistencia

```text
┌────────────────────────────────┐
│      REGISTRO DE ASISTENCIA    │
│                                │
│ Nombre del participante        │
│ ┌────────────────────────────┐ │
│ │                            │ │
│ └────────────────────────────┘ │
│                                │
│       [ + AGREGAR ]            │
│                                │
│ Ana López          Presente ✓  │
│ Carlos Pérez       Ausente   ✗  │
│ María Gómez        Presente ✓  │
│                                │
│ ────────────────────────────── │
│ Total:       3                 │
│ Presentes:   2                 │
│ Ausentes:    1                 │
│                                │
│       [ VER RESUMEN ]          │
└────────────────────────────────┘
```

---

## Pantalla 3 – Administración

```text
┌────────────────────────────────┐
│        ADMINISTRACIÓN          │
│                                │
│ Ana López                      │
│ [Editar]   [Eliminar]          │
│                                │
│ Carlos Pérez                   │
│ [Editar]   [Eliminar]          │
│                                │
│ María Gómez                    │
│ [Editar]   [Eliminar]          │
│                                │
│ ┌────────────────────────────┐ │
│ │     REINICIAR SESIÓN       │ │
│ └────────────────────────────┘ │
│                                │
└────────────────────────────────┘
```

---

## Pantalla 4 – Resumen de asistencia

```text
┌────────────────────────────────┐
│      RESUMEN DE ASISTENCIA     │
│                                │
│ Total participantes: 3         │
│ Presentes: 2                   │
│ Ausentes: 1                    │
│                                │
│ PRESENTES                      │
│ • Ana López                    │
│ • María Gómez                  │
│                                │
│ AUSENTES                       │
│ • Carlos Pérez                 │
│                                │
│ ┌────────────────────────────┐ │
│ │        COMPARTIR           │ │
│ └────────────────────────────┘ │
│                                │
│ ┌────────────────────────────┐ │
│ │       NUEVA SESIÓN         │ │
│ └────────────────────────────┘ │
└────────────────────────────────┘
```

---

## 9. Alcance del proyecto

### Funciones incluidas

- Registro temporal de participantes.
- Listado de participantes.
- Estado presente o ausente.
- Modificación.
- Eliminación.
- Conteo automático.
- Resumen.
- Compartir información.
- Reinicio de sesión.

### Funciones fuera del alcance

La primera versión no incluirá:

- Base de datos.
- Firebase.
- Servidores externos.
- Inicio de sesión.
- Registro de usuarios.
- GPS.
- Mapas.
- Inteligencia artificial.
- Pagos.
- Reportes PDF.
- Sincronización en la nube.
- Historial permanente.

Estas funciones podrían considerarse como mejoras futuras.

---

## 10. Plan preliminar de desarrollo

| Semana | Actividad principal |
|---|---|
| 1 | Definición del proyecto, README, GitHub y wireframes |
| 2 | Creación del proyecto en Android Studio y diseño de interfaces |
| 3 | Registro y visualización de participantes |
| 4 | Estados de asistencia, modificación y eliminación |
| 5 | Conteos, resumen y función de compartir |
| 6 | Pruebas, correcciones, documentación y entrega |

---

## 11. Resultado esperado

Al finalizar el proyecto se espera disponer de una aplicación Android funcional capaz de:

- Registrar temporalmente participantes.
- Marcar su estado de asistencia.
- Modificar o eliminar registros.
- Calcular automáticamente presentes y ausentes.
- Mostrar un resumen de la actividad.
- Compartir los resultados utilizando las funciones de Android.

El proyecto permitirá demostrar conocimientos fundamentales relacionados con Android Studio, Kotlin, XML, navegación entre pantallas, eventos, manejo de listas y documentación del proyecto mediante GitHub.

---

## 12. Mejoras futuras

En versiones posteriores podrían incorporarse:

- Almacenamiento permanente.
- Base de datos.
- Inicio de sesión.
- Diferentes roles de usuario.
- Sincronización en la nube.
- Exportación de reportes.
- Estadísticas.
- Código QR.
- Notificaciones.

Estas funcionalidades no forman parte del alcance de la primera versión.

---

## Autor

Proyecto académico desarrollado como parte del curso de **Desarrollo de Aplicaciones Android**.

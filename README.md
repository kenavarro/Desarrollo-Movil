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

# M2 – Avance del proyecto

## Semana 2 – Creación del proyecto y diseño de interfaces

Durante el Módulo 2 se inició el desarrollo práctico del Sistema Móvil de Control de Asistencia a partir del borrador elaborado en M1.

### Actividades realizadas

- Instalación y configuración de Git en Windows.
- Clonación del repositorio del proyecto desde GitHub.
- Creación de la rama de trabajo `m2-progreso`.
- Creación del proyecto Android en Android Studio.
- Configuración inicial del proyecto con:
    - Kotlin.
    - XML.
    - Minimum SDK API 24.
    - Kotlin DSL.
- Configuración de un dispositivo virtual Android:
    - Medium Phone.
    - Android 16.
    - API 36.
- Compilación y ejecución exitosa de la aplicación en el emulador.

### Interfaces creadas

Durante esta semana se desarrollaron visualmente las cuatro pantallas definidas en el borrador del proyecto:

1. `MainActivity`
    - Pantalla principal.
    - Título del sistema.
    - Botón Nueva Asistencia.
    - Botón Administración.

2. `RegistroAsistenciaActivity`
    - Campo para nombre del participante.
    - Botón Agregar.
    - Ejemplos visuales de participantes.
    - Total de participantes.
    - Total de presentes.
    - Total de ausentes.
    - Botón Ver Resumen.

3. `AdministracionActivity`
    - Listado visual de participantes.
    - Botones Editar.
    - Botones Eliminar.
    - Botón Reiniciar Sesión.

4. `ResumenActivity`
    - Total de participantes.
    - Presentes.
    - Ausentes.
    - Listado visual de presentes.
    - Listado visual de ausentes.
    - Botón Compartir.
    - Botón Nueva Sesión.

### Navegación implementada

Se utilizó un `Intent` para conectar la pantalla principal con la pantalla de registro de asistencia.

El flujo implementado actualmente es:

MainActivity  
→ Nueva Asistencia  
→ Intent  
→ RegistroAsistenciaActivity

Esta implementación permitió aplicar de forma práctica los conceptos de `Activity`, `Intent` y navegación entre pantallas estudiados durante el módulo.

### Estado actual

Las interfaces creadas durante M2 son principalmente visuales. Los nombres de participantes, estados y conteos mostrados actualmente son datos de ejemplo utilizados para representar los wireframes.

Todavía no se ha implementado:

- Registro dinámico de participantes.
- Modificación de participantes.
- Eliminación de participantes.
- Conteo automático real.
- Generación dinámica del resumen.
- Función de compartir.
- Reinicio de sesión.

Estas funciones se desarrollarán progresivamente en los siguientes módulos.

### Troubleshooting

Durante la configuración inicial se presentó un error de Gradle debido a que la ruta del proyecto contenía un carácter no ASCII en la carpeta `Móviles`.

Ruta con problema:

`Desarrollo de Aps Móviles`

Se corrigió cambiando el nombre de la carpeta a:

`Desarrollo de Aps Moviles`

Después de realizar el cambio, Android Studio pudo sincronizar y compilar correctamente el proyecto.

### Control de versiones

Para el desarrollo de M2 se utilizó la rama:

`m2-progreso`

También se actualizó el archivo `.gitignore` para evitar incluir la carpeta `.idea`, ya que contiene configuraciones locales de Android Studio.

### Próximos pasos

En los siguientes módulos se continuará con la implementación de la lógica funcional del sistema, comenzando con el registro y visualización dinámica de participantes.

## M4 – Actualización del proyecto y registro de cambios

Durante este módulo se realizó una nueva revisión del proyecto **Sistema Móvil de Control de Asistencia**, tomando como referencia el borrador desarrollado durante los módulos anteriores.

El propósito principal continúa siendo desarrollar una aplicación Android sencilla que permita registrar participantes de una actividad, controlar su estado de asistencia y obtener un resumen de los resultados.

Se mantiene el alcance definido originalmente: la primera versión de la aplicación no utilizará una base de datos, Firebase, servidores externos ni sincronización en la nube. Los datos serán manejados temporalmente durante la sesión activa de la aplicación.

### Cambios realizados en el proyecto

Durante los primeros módulos se definieron el problema, los objetivos, el alcance, las tecnologías que se utilizarán y los wireframes de las principales pantallas.

Posteriormente se comenzó a trabajar con los conceptos fundamentales del desarrollo Android, incluyendo Activities, Fragments, Intents, ciclo de vida de las Activities y navegación entre los diferentes componentes de una aplicación.

En este módulo se continúa avanzando hacia la implementación de las funciones principales del sistema de asistencia, especialmente las relacionadas con el manejo de participantes y sus estados.

Las funciones contempladas en esta etapa son:

* Registrar participantes.
* Mostrar los participantes ingresados.
* Marcar a cada participante como presente o ausente.
* Permitir modificar información registrada.
* Permitir eliminar participantes ingresados por error.
* Mantener los datos únicamente durante la sesión activa.
* Preparar la estructura necesaria para implementar posteriormente los conteos y el resumen de asistencia.

## Changelog

| Versión / Módulo | Estado                | Cambios                                                                                                                                                                                       |
| ---------------- | --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| M1               | Completado            | Definición del problema, objetivos, alcance, tecnologías, funciones principales, wireframes y creación del repositorio en GitHub.                                                             |
| M2               | Avance inicial        | Estudio y aplicación de conceptos relacionados con Activities, Fragments, Intents, ciclo de vida y organización del proyecto Android.                                                         |
| M3               | Desarrollo progresivo | Preparación del proyecto para comenzar la implementación funcional y continuar trasladando el diseño planteado en el borrador a la aplicación Android.                                        |
| M4               | Actual                | Continuación del desarrollo del sistema de asistencia, enfocándose en el registro de participantes, estados de presente/ausente y preparación de las funciones de modificación y eliminación. |
| M5               | Futuro                | Implementación de conteos automáticos de participantes, presentes y ausentes, además de la pantalla de resumen y la función para compartir resultados mediante un Intent de Android.          |
| M6               | Futuro                | Ejecución de pruebas funcionales, identificación y corrección de errores y actualización de la documentación técnica.                                                                         |
| M7               | Futuro                | Consolidación de funcionalidades, incorporación de cambios derivados de pruebas o retroalimentación y publicación del código y README actualizado en GitHub Classroom.                        |
| M8               | Futuro                | Preparación y entrega de la versión final de la aplicación, repositorio y documentación del proyecto.                                                                                         |

### Decisiones que se mantienen

La primera versión continúa utilizando un alcance reducido para mantener el proyecto viable dentro del período académico.

Por esta razón se mantienen las siguientes decisiones:

* Utilizar Kotlin como lenguaje principal.
* Utilizar Android Studio como entorno de desarrollo.
* Utilizar XML para la definición de las interfaces.
* Utilizar Git y GitHub para control de versiones y documentación.
* No implementar una base de datos en la primera versión.
* No utilizar Firebase ni servidores externos.
* No implementar autenticación de usuarios.
* Mantener los datos únicamente durante la sesión activa.

Estas decisiones permiten concentrar el desarrollo en los fundamentos principales de Android y en las funciones directamente relacionadas con el control de asistencia.

### Próximos pasos

El siguiente avance del proyecto estará enfocado en completar las funciones de asistencia y posteriormente implementar:

1. Conteo automático de participantes.
2. Conteo de presentes y ausentes.
3. Pantalla de resumen.
4. Función para compartir los resultados utilizando un Intent.
5. Pruebas funcionales de la aplicación.
6. Corrección de errores encontrados.
7. Actualización continua del README y del registro de cambios.
8. Publicación del código actualizado en GitHub.
9. Preparación del proyecto para GitHub Classroom y la entrega final del módulo 8.

El proyecto continuará actualizándose de forma progresiva y cada cambio funcional importante será registrado mediante commits en GitHub.

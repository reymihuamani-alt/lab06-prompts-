# Tarea: Mi prompt profesional

## Funcionalidad elegida

Registro de clientes para una tienda pequeña, en Java con Swing. El vendedor ingresa código, nombre, correo y teléfono, y ve los clientes registrados en una tabla.

## Version 1: prompt basico

```text
Hazme un programa para registrar clientes.
```

**Qué cambié:** nada, es el punto de partida.

**Qué pasó:** la IA eligió por su cuenta el lenguaje, la interfaz y los datos del cliente. Entregó un programa de consola con solo nombre y edad, sin explicación y sin validaciones.

**Qué falta:** no le dije el lenguaje, el tipo de aplicación ni los campos. La IA tuvo que adivinar.

## Version 2

```text
Actua como desarrollador Java. Crea un programa de escritorio con Swing
para registrar clientes de una tienda. El cliente tiene codigo, nombre,
correo y telefono. Explica brevemente el funcionamiento y presenta el codigo.
```

**Qué cambié:** agregué rol (desarrollador Java), contexto (tienda), tecnología (Swing), los cuatro atributos del cliente y la petición de explicar el funcionamiento.

**Por qué:** la v1 era demasiado general y la respuesta no servía para mi caso.

**Qué mejoró:** ahora la respuesta usa Swing, tiene los cuatro campos y viene con una explicación breve. Pero el código quedó casi todo en una sola clase, no validaba nada y los mensajes salían por consola.

## Version 3: prompt final

```text
Actua como desarrollador Java con experiencia en aplicaciones de escritorio.
Crea un modulo de registro de clientes para una tienda pequena usando Java Swing.
Contexto: lo usara un vendedor para registrar clientes nuevos y verlos en una
tabla. Es un proyecto academico y los datos se guardan en memoria con un
ArrayList, sin base de datos.
El cliente tiene los atributos codigo, nombre, correo y telefono.
Restricciones: no uses librerias externas; valida que ningun campo este vacio,
que el correo contenga @ y que el telefono tenga 9 digitos; muestra todos los
mensajes con JOptionPane.
Usa este estilo para los metodos: getNombre(), setNombre(String nombre).
Formato: explica primero la estructura de las clases en maximo 5 lineas y luego
presenta el codigo Java, cada clase en su propio bloque de codigo.
```

**Qué cambié:** agregué restricciones (sin librerías externas, validaciones, JOptionPane), un ejemplo del estilo de los métodos, el detalle de que los datos van en memoria y un formato de respuesta (explicación corta y luego una clase por bloque).

**Por qué:** en la v2 el código funcionaba pero no estaba organizado, no validaba y no seguía mi estilo.

**Qué mejoró:** la respuesta separa las clases (`Cliente`, `ClienteService`, `VentanaRegistro`, `Main`), valida los datos, muestra los errores con JOptionPane, usa getters y setters como en mi ejemplo y sigue el orden que pedí: primero la explicación y después el código.

## Componentes del prompt final

| Componente | Texto de mi prompt |
|------------|--------------------|
| Rol | Actua como desarrollador Java con experiencia en aplicaciones de escritorio. |
| Instruccion | Crea un modulo de registro de clientes para una tienda pequena usando Java Swing. El cliente tiene los atributos codigo, nombre, correo y telefono. |
| Contexto | Lo usara un vendedor para registrar clientes nuevos y verlos en una tabla. Es un proyecto academico y los datos se guardan en memoria con un ArrayList, sin base de datos. |
| Ejemplo | Usa este estilo para los metodos: getNombre(), setNombre(String nombre). |
| Formato | Explica primero la estructura de las clases en maximo 5 lineas y luego presenta el codigo Java, cada clase en su propio bloque de codigo. |

**Restricción del prompt final:** no uses librerias externas; valida que ningun campo este vacio, que el correo contenga @ y que el telefono tenga 9 digitos; muestra todos los mensajes con JOptionPane.

## Evaluacion del resultado

| Criterio | Cumple (Si / No) |
|----------|------------------|
| Esta escrito en Java y usa Swing | Si |
| Pide codigo, nombre, correo y telefono | Si |
| El codigo esta organizado en clases | Si |
| Valida los datos (campos vacios, @ y 9 digitos) | Si |
| Muestra los mensajes con JOptionPane | Si |
| Explica la estructura antes del codigo | Si |
| No usa librerias externas | Si |

## Errores que evite

| Error frecuente | Cómo lo evité |
|-----------------|---------------|
| Ser demasiado general | Pasé de "Hazme un programa para registrar clientes" a un prompt con rol, tecnología (Swing), atributos concretos, restricciones y un ejemplo. |
| No indicar el formato | Pedí explícitamente una explicación de máximo 5 líneas primero y luego el código, con cada clase en su propio bloque. |
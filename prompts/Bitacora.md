# Bitacora de prompts 
  
Laboratorio 06: Fundamentos de Ingenieria de Prompts. 
  
Herramienta de IA usada: (escribe aqui cual usaste) 
  
## Ejercicio 2: Tokens y ventana de contexto 
  
## Ejercicio 3: Temperatura 
  
## Ejercicio 4: Prompt vago vs estructurado 
  
## Ejercicio 5: Anatomia de un prompt 
  
## Ejercicio 6: Del prompt basico al profesional 

| Texto | Caracteres | Tokens | 
|-------|------------|--------| 
| Los estudiantes programan en Java. | | | 
| The students program in Java. | | | 
| desafortunadamente | | |

| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|-----------------|----------------------------|
| 0   | 100.0% | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5 | 65.3%  | PrestaLibro, BiblioTec, BiblioTec, BiblioTec, LibroYa |
| 1   | 44.5%  | BiblioTec, PrestaLibro, BiblioTec, BiblioTec, BiblioTec |
| 1.8 | 32.2%  | LectoGoes, Nobuilar, BiblioTec, BiblioTec, LibroYa |



| Criterio | Prompt vago | Prompt estructurado | 
|----------|-------------|---------------------| 
| Menciona el objetivo del sistema ||no | 
| Menciona a los usuarios principales ||no| 
| Tiene exactamente 3 funcionalidades | si| | 
| Esta en 3 parrafos |si| | 
| Lo usaria en un informe real |si| | 

| Componente | Texto de mi prompt | 
|------------|--------------------| 
| Rol |Actua como desarrollador Java. | 
| Instruccion | usando una clase Producto con los atributos codigo, nombre, precio y stock. | 
| Contexto |Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda.  | 
| Ejemplo |Usa este estilo para los metodos: getPrecio(), setPrecio(double precio).  | 
| Formato |Explica primero la estructura de la clase y luego presenta el codigo Java. | 

| Nivel | Qué cambió en la respuesta |
|-------|----------------------------|
| 1 | La IA respondió con cualquier programa genérico (un "Hola Mundo"); la respuesta era impredecible. |
| 2 | Al agregar el rol, la respuesta tomó el tono y las buenas prácticas de un desarrollador Java profesional. |
| 3 | Al agregar el contexto, dejó de ser "cualquier programa": se enfocó específicamente en la gestión de productos de una tienda. |
| 4 | Al agregar la instrucción, la respuesta creó exactamente la clase Producto con los cuatro atributos pedidos (codigo, nombre, precio y stock). |
| 5 | Al agregar el formato, la IA explicó primero la estructura de la clase en texto y recién después presentó el código Java. |
| 6 (con ejemplo) | Al agregar el ejemplo, los métodos getter y setter siguieron el estilo indicado: getPrecio() y setPrecio(double precio). |

```text 
(Actua como desarrollador Java. Crea un ejemplo de login para una aplicacion de escritorio utilizando Swing. El usuario debe ingresar correo y contrasena. Explica brevemente el funcionamiento y presenta el codigo organizado por clases.
Mejora el codigo anterior con estas restricciones: no uses librerias externas, valida que el correo contenga @ y que la contrasena tenga al menos 8 caracteres, y muestra los mensajes con JOptionPane.)


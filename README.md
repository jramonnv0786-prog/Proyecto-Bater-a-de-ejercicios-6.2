# Proyecto-Bateria-de-ejercicios-6.2
Diagrama de clases


Ejercicio 1
```mermaid
classDiagram
    class Usuario {
        -String nombreUsuario
        -String password
        +String correo
        +cambiarPassword(String nueva)
        -validarEmail()
    }


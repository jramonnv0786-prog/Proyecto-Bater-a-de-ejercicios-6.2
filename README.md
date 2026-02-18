# Proyecto-Bater-a-de-ejercicios-6.2
Diagrama de clases

```mermaid
classDiagram
    class Usuario {
        -String nombreUsuario
        -String password
        +String correo
        +cambiarPassword(String nueva)
        -validarEmail()
    }

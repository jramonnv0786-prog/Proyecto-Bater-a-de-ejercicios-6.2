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
````
Ejercicio 2
```mermaid

classDiagram
    class Persona {
        +String nombre
        +String dni
    }
    class Estudiante {
        +int numeroExpediente
        +float notaMedia
    }
    Persona <|-- Estudiante

```
Ejercicio 3
```mermaid

classDiagram
    class Computadora {
        +String modelo
        +encender()
    }
    class PlacaBase {
        +String chipset
    }
    class Raton {
        +String tipoConector
    }

    Computadora *-- PlacaBase : Composición
    Computadora o-- Raton : Agregación
```

Ejercicio 4

```mermaid

classDiagram
    class CentroComercial {
        +String nombre
        +String direccion
    }
    class Tienda {
        +String nombreTienda
        +String rubro
    }

    CentroComercial "1" -- "1..*" Tienda : alberga
```
Ejercicio 5

```mermaid
classDiagram
    class MetodoPago {
        <<interface>>
        +procesar(double importe)
    }
    class Tarjeta {
        +procesar(double importe)
    }
    class Paypal {
        +procesar(double importe)
    }
    class Carrito {
        +pagar(MetodoPago miMetodo)
    }

    MetodoPago <|.. Tarjeta : Implementa
    MetodoPago <|.. Paypal : Implementa
    Carrito ..> MetodoPago : Usa (Dependencia)
```

Ejercicio 6

```mermaid
classDiagram
    class Recurso {
        -int id
        -String titulo
        +prestar()
        +devolver()
    }
    class Libro {
        +String isbn
    }
    class Revista {
        +int numeroEdicion
    }
    class Usuario {
        +String nombre
        +int numCarnet
    }

    Recurso <|-- Libro : Es un
    Recurso <|-- Revista : Es un
    Usuario "1" --> "0..*" Recurso : tiene prestado
```



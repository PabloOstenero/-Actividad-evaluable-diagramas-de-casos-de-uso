# Actividad-evaluable-diagramas-de-casos-de-uso

Crea el diagrama de uso haciendo uso de platuml, representado los actores y casos de uso que identifiques en los requisitos.

![Diagrama de caso de uso](https://github.com/user-attachments/assets/36710848-e940-425c-ad1a-4416ccf7c1d8)

```Plantuml
@startuml
actor Cliente
actor Cajero

Cliente --> (Validación sistema)
Cliente --> (Sacar dinero)

(Validación sistema) ..> (Ingresar dinero) : <<include>>
(Validación sistema) ..> (Transferencia) : <<include>>
(Validación sistema) ..> (Sacar dinero) : <<include>>
(Sacar dinero) ..> (Comprobar saldo) : <<include>>
(Sacar dinero) ..> (Validar límite diario) : <<include>>

Cajero --> (Comprobar saldo)
Cajero --> (Validar límite diario)

@enduml
```

Describe, haciendo uso de la plantilla, al menos el caso de uso "Sacar dinero", con las interacciones que tiene entre el actor y el caso de uso.

El cliente se valida en el sistema para acceder a las operaciones posibles como sacar dinero, hacer una transferencia e ingresar dinero.
Si saca dinero, el cajero valida si el cliente se ha pasado del límite diario permitido de dinero o si tiene dinero suficiente para sacarlo.

Responde a las siguiente pregunta:¿Para qué me sirve tener/realizar un diagrama de casos de uso modelando el sistema que se representa? ¿Qué aporta?

Un diagrama de caso de uso aporta visibilidad para el usuario para ver que cosas puede hacer en el sistema.

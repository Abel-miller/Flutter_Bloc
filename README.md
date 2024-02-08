# Flutter Bloc

## Introducción

Flutter Bloc es un patrón de arquitectura que facilita la gestión de la lógica de negocio en aplicaciones Flutter. Proporciona una separación eficiente entre la interfaz de usuario y la lógica subyacente, lo que mejora la estructura y mantenimiento del código.

## Estructura del Proyecto

La implementación de Flutter Bloc implica la creación de clases para Eventos, Estados y Bloques.

- **Eventos:** Representan acciones en la aplicación (por ejemplo, tocar un botón).
  
- **Estados:** Reflejan el estado actual de la aplicación.

- **Bloques:** Gestionan la lógica de negocio, procesando eventos y emitiendo estados en respuesta.

## Ejemplo Básico

```dart
// Ejemplo de Evento
class MiEvento extends Equatable {
  @override
  List<Object> get props => [];
}

// Ejemplo de Estado
class MiEstado extends Equatable {
  @override
  List<Object> get props => [];
}

// Ejemplo de Bloque
class MiBloque extends Bloc<MiEvento, MiEstado> {
  @override
  MiEstado get initialState => MiEstado();

  @override
  Stream<MiEstado> mapEventToState(MiEvento event) async* {
    // Lógica de negocio y emisión de nuevos estados
  }
}

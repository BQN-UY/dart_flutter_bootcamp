# ✅ Solución sugerida – Etapa 1: Fundamentos de Clean Architecture

Este documento muestra cómo debería organizarse el código del ejercicio guiado "Separando
responsabilidades" siguiendo los principios de Clean Architecture.

---

## 📂 Estructura final esperada

```bash
lib/
├── features/
│   └── bienvenida/
│       ├── dominio/
│       │   ├── entidades/
│       │   │   └── mensaje_bienvenida.dart
│       │   └── repositorios/
│       │       └── bienvenida_repositorio.dart
│       ├── aplicacion/
│       │   └── obtener_mensaje.dart
│       ├── infraestructura/
│       │   └── bienvenida_repositorio_impl.dart
│       └── presentacion/
│           └── mensaje_widget.dart
└── main.dart
```

---

## 🧠 Explicación por archivo

### dominio/

- `mensaje_bienvenida.dart`: define una entidad pura que representa el mensaje.
- `bienvenida_repositorio.dart`: interfaz abstracta del repositorio, usada por el caso de uso.

### aplicacion/

- `obtener_mensaje.dart`: caso de uso que representa la lógica de negocio para obtener el mensaje.
  Depende de la interfaz del repositorio.

### infraestructura/

- `bienvenida_repositorio_impl.dart`: implementación del repositorio que retorna una instancia de
  `MensajeBienvenida`. Depende del dominio (a través de la interfaz).

### presentacion/

- `mensaje_widget.dart`: widget que muestra el mensaje recibido.

---

## 📌 Consideraciones clave

- La implementación del repositorio **depende del dominio**, y **no al revés**.
- La UI **no conoce los detalles de infraestructura**, sólo invoca el caso de uso.
- El dominio contiene **sólo lógica pura y sin dependencias de Flutter**.

---

Esta solución demuestra una separación clara de responsabilidades y será la base para aplicaciones
más complejas en las siguientes etapas. ✅

# 🧠 Fase 2 – Widget Tree y Ciclo de Vida

## 🎯 Objetivo

Entender cómo Flutter construye y gestiona la UI a través del árbol de widgets, y diferenciar cuándo
usar StatelessWidget o StatefulWidget. Aprender el ciclo de vida de un widget y el rol de
BuildContext.

---

## 📘 Temas a estudiar

### 1. StatelessWidget vs StatefulWidget

- Definición y diferencias principales
- Cuándo usar cada uno: UI estática vs UI dinámica
- Propiedades inmutables y estado interno

### 2. Ciclo de vida de StatefulWidget

- Métodos clave: `createState()`, `initState()`, `build()`, `didUpdateWidget()`, `setState()`,
  `dispose()`
- Orden de ejecución: montaje, actualización, desmontaje
- Importancia de `setState()` para disparar rebuilds

### 3. BuildContext y el árbol de widgets

- Qué es un BuildContext: manejador de ubicación en el widget tree
- Uso para buscar ancestros (ej: `Theme.of(context)`, `Navigator.of(context)`)
- Contexto correcto vs contexto incorrecto (errores comunes)

---

## 📎 Lecturas recomendadas

1. 🧭 [Flutter UI Overview](https://docs.flutter.dev/ui)  
   Introducción general al sistema de widgets de Flutter y cómo se construyen interfaces visuales.
   Punto de partida conceptual.

2. 🧱 [Building Layouts in Flutter](https://docs.flutter.dev/ui/layout/tutorial)  
   Aprende a usar `Row`, `Column`, `Container`, `Padding`, etc. para crear interfaces jerárquicas.

3. 🖱️ [Add Interactivity (Flutter Official Docs)](https://docs.flutter.dev/ui/interactivity)  
   Explica el uso de `StatefulWidget` para convertir una UI estática en interactiva con `setState`.

4. 🎥 [How Flutter Works: The Three Trees (YouTube)](https://youtu.be/xiW3ahr4CRU?si=O2acHkKs5il7WsOV)  
Video esencial que explica el Widget Tree, Element Tree y Render Tree. Fundamenta el rol del
`BuildContext`.

5. n🎥 [How Flutter Works: The State Class (YouTube)](https://youtu.be/FP737UMx7ss?si=GFVCuOag2gTZn5t5)  
Explicación visual del ciclo de vida de los widgets con `State`, `initState`, `dispose`, etc.

6. 🔧 [What is a BuildContext? (FlutterClutter)](https://www.flutterclutter.dev/flutter/basics/what-is-a-buildcontext/2021/71268/)  
Artículo accesible para comprender la función de `BuildContext` y cómo navegar el widget tree.

---

## ✅ ¿Qué deberías poder hacer luego de esta etapa?

- Identificar cuándo usar StatelessWidget vs StatefulWidget
- Explicar en qué momento se llama a `initState()`, `build()`, `dispose()` y otros métodos de ciclo
  de vida
- Utilizar correctamente BuildContext para acceder a ancestros en el widget tree
- Evitar errores comunes relacionados con el uso incorrecto de context (por ejemplo, llamar a
  `context` antes de montarse)

---

## 🧪 Próximamente: Ejercicio práctico

En el archivo `widget_challenge.dart`, se te pedirá que basandose en el un ejemplo de contador:

1. Mostrar mensaje por consola en:

    - initState

    - dispose

    - didUpdateWidget

2. Usar un parámetro showCounter que permita ocultar el contador. Si cambia, usar didUpdateWidget
   para imprimir el cambio.

3. Mostrar un SnackBar al llegar a 5 toques usando BuildContext.

4. Evitar errores comunes (ej: uso de context luego de await).

Instrucciones para comenzar el ejercicio:

1. Elegir un directorio de trabajo (ej:
   `etapa1_fundamentos_flutter_y_dart/02_widget_tree_y_ciclo_de_vida/`).
2. Ejecutar 'flutter create <nombre_del_proyecto>'. Sin '< >' y con el nombre que desees. Por
   ejemplo: `flutter create widget_tree_challenge`.
3. Remplazar el contenido de `lib/main.dart` con el código del ejercicio
   `ejercicios/widget_challenge.dart`.

Para este ejercicio, tienes una solucion de referencia en `solution/widget_challenge_solution.dart`.
Puedes comparar tu implementación con la solución una vez que termines.

### 🧩 Ejercicio de Diagnóstico (previo al libre)

Se te presentará un ejemplo con un error común relacionado al ciclo de vida o al uso incorrecto del
`BuildContext` (por ejemplo, uso de `context` después de un `await`).

Tu objetivo será:

- Identificar el error
- Explicarlo
- Corregirlo respetando buenas prácticas

### 🎯 Challenge libre

Finalmente, se te pedirá crear un pequeño componente desde cero según un comportamiento descripto (
ej: un switch que alterna la visibilidad de un widget interactivo con estado propio).

Este desafío pondrá a prueba tu capacidad de razonar sobre el widget tree, gestionar correctamente
el estado, usar el ciclo de vida y el `BuildContext` de forma segura y efectiva.


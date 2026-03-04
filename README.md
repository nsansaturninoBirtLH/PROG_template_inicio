# PROG_template_inicio

Template de GitHub Classroom para las asignaturas de **Programación** con Java 21, pensado para que el alumnado trabaje en GitHub Codespaces con un entorno controlado.

---

## Contenido del template

| Ruta | Descripción |
|---|---|
| `.devcontainer/devcontainer.json` | Configuración del Dev Container (imagen, extensiones y settings de VS Code) |
| `.github/copilot-instructions.md` | Instrucciones personalizadas para Copilot Chat (modo pedagógico) |
| `lib/junit-platform-console-standalone-1.13.0-M3.jar` | JUnit 5 standalone para ejecutar tests sin Maven/Gradle |

## Entorno de desarrollo

- **Imagen base:** `mcr.microsoft.com/devcontainers/java:21` (Java 21)
- **Extensiones instaladas:**
  - `vscjava.vscode-java-pack` — Soporte completo de Java (Language Server, debugger, test runner…)
  - `GitHub.copilot-chat` — Chat de Copilot para resolver dudas

## Configuración de Copilot

El template restringe el uso de IA para que el alumnado **escriba todo el código manualmente**, pudiendo únicamente usar el chat para consultar dudas:

| Función | Estado |
|---|---|
| Chat de Copilot (preguntar dudas) | ✅ Activo |
| Autocompletado IA (sugerencias inline) | ❌ Desactivado |
| Modo Agente (acciones autónomas) | ❌ Desactivado |
| Inline Chat (`Ctrl+I`) | ❌ Desactivado |
| Copilot Edits (edición directa de ficheros) | ❌ Desactivado |
| Auto-fix de tests | ❌ Desactivado |

### Modo pedagógico del chat

El chat de Copilot está configurado en **modo pedagógico** mediante el fichero `.github/copilot-instructions.md`. En lugar de dar soluciones directas, el chat:

- **Guía al alumno** con preguntas y pistas para que resuelva el problema por sí mismo.
- **Explica conceptos** y lógica, no implementaciones concretas.
- **Usa pseudocódigo o fragmentos parciales** solo cuando es imprescindible ilustrar un concepto.
- **Señala errores sin corregirlos** — indica el tipo y la zona, pero el alumno debe arreglarlo.
- **Sugiere consultar la documentación** oficial de Java.
- **Responde siempre en español.**

## Configuración del editor

Para fomentar que el alumnado practique la escritura de código, se desactivan diversas ayudas automáticas:

- **Sin autocompletado** del editor ni de Java
- **Sin cierre automático** de llaves, paréntesis ni comillas
- **Sin indentación automática**
- **Sin formateo automático** al escribir, pegar o guardar
- **Sin snippets** ni sugerencias en terminal
- **Sin bombillita** de acciones rápidas (Quick Fix)

## Uso

1. Crear una tarea en **GitHub Classroom** usando este repositorio como template.
2. El alumnado acepta la tarea y abre el Codespace.
3. El entorno se configura automáticamente con todas las restricciones.
4. El alumno puede usar el **chat de Copilot** para dudas, pero debe escribir el código él mismo.
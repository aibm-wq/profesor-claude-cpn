# C2 — Introduction to Agent Skills
**Link Skilljar:** https://anthropic.skilljar.com/page/claude-partner-network-learning-path
**Sesión grupal:** Sáb 21 JUN (parte 2)

---

## SECCIÓN 1-2 — ¿Qué es un Skill?

**Concepto:**
Un Skill es una receta guardada que le enseñas a Claude una vez y puede usar siempre. Es un archivo de texto (.md) con instrucciones. Claude lo detecta automáticamente cuando la situación aplica.

**Analogía:**
"Es como crear un SOP — escribes el procedimiento una vez y Claude lo ejecuta cada vez que lo necesita. No tienes que explicarlo de nuevo."

**Estructura de un Skill:**
```
---
name: cierre-dia
description: "Registrar el cierre del día y actualizar el tracker"
---

# Instrucciones
1. Revisa las tareas completadas hoy
2. Actualiza el tracker...
```
El frontmatter (el encabezado entre `---`) es la "etiqueta" — le dice a Claude cuándo activar este Skill.

**Ejemplos:**
- `/cierre-dia` — registra el día, revisa pendientes, actualiza el vault
- `/lunes` — arranca la semana con el resumen de proyectos

**Los 3 puntos del quiz:**
1. Skill = archivo .md con frontmatter + instrucciones.
2. La descripción del frontmatter es lo que activa el Skill — tiene que ser clara.
3. Skills ≠ CLAUDE.md. CLAUDE.md es contexto fijo. Skills son tareas específicas reutilizables.

---

## SECCIÓN 3-4 — Skills Avanzados y Comparación

**Skills multi-archivo:**
Skills más complejos pueden tener múltiples archivos y restricciones de herramientas (allowed-tools) — para que Claude solo use lo necesario para esa tarea específica.

**La comparación más importante (entra en el quiz):**

| | ¿Qué es? | ¿Cuándo está activo? |
|---|---|---|
| **CLAUDE.md** | Contexto general (quién eres) | Siempre, en todo el proyecto |
| **Skill** | Tarea específica reutilizable | Cuando Claude detecta que aplica |
| **Hook** | Acción automática | Antes/después de una acción |
| **Subagente** | Claude delegando a otro Claude | Tareas que necesitan aislamiento |

**Analogía de equipo:**
"CLAUDE.md es quien eres. Un Skill es lo que sabes hacer. Un Hook es tu hábito automático. Un Subagente es cuando delegas a alguien de tu equipo."

**Los 3 puntos del quiz:**
1. allowed-tools limita qué herramientas puede usar Claude en ese Skill.
2. CLAUDE.md es siempre activo. Skills se activan cuando aplican.
3. Subagente = Claude que Claude contrata para una subtarea aislada.

---

## SECCIÓN 5-6 — Compartir Skills y Troubleshooting

**Compartir:**
Los Skills se comparten vía repositorio Git. Todos en el equipo tienen los mismos Skills automáticamente cuando sincronizan el repositorio. También se pueden empaquetar como plugins (.skill).

**Problemas más comunes:**
1. Skill no se activa → la descripción del frontmatter no es clara
2. Conflicto de Skills → dos Skills aplican a la misma situación → gana el más específico
3. Error de herramienta → Claude intenta usar algo no permitido en ese Skill

**Los 3 puntos del quiz:**
1. Skills se comparten vía Git. Todo el equipo los tiene al sincronizar.
2. Si un Skill no se activa → revisa la descripción del frontmatter.
3. Skills se pueden empaquetar como plugins para distribución.

---

## QUIZ FINAL C2

**Repasa antes de intentar el quiz en Skilljar:**
- ¿Qué hace el frontmatter de un Skill?
- Diferencia entre CLAUDE.md, Skill, Hook y Subagente
- ¿Cómo se comparten los Skills con el equipo?
- ¿Qué pasa si un Skill no se activa?

**Puntaje mínimo:** 70% — puedes reintentar sin límite.

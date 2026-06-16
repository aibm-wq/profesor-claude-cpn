# Profesor Claude — CPN

Skill para Claude (Cowork) que actúa como tutor personal del programa **Claude Partner Network (CPN)** de Anthropic.

## Qué hace

- Se activa automáticamente al escribir `buen día profe`
- Muestra un tablero de progreso al inicio de cada sesión
- Guía módulo por módulo los 4 cursos de Skilljar en orden estricto
- Guarda el progreso automáticamente en `PROGRESO_CPN.md`
- Genera ejercicios de práctica estilo quiz real

## Cursos incluidos

| # | Curso |
|---|-------|
| C1 | Claude Code in Action |
| C2 | Introduction to Agent Skills |
| C3 | Introduction to MCP |
| C4 | Building with the Claude API |

## Instalación

### En Cowork (app de escritorio)

**Paso 1 — Crear tu carpeta de estudio**
Crea una carpeta llamada `CPN` en tu Escritorio o Documentos y conéctala a Cowork (botón "Select Folder").

**Paso 2 — Instalar el Skill**
Descarga `profesor-claude-cpn.skill` y ábrelo — aparece el botón **"Save skill"** en Cowork. Haz clic.

### En Claude Code (CLI)

**Opción A — CLAUDE.md (recomendada)**
1. Crea una carpeta `CPN` donde vayas a estudiar
2. Copia el contenido de `SKILL.md` en un archivo `CLAUDE.md` dentro de esa carpeta
3. Abre Claude Code en esa carpeta: `claude`
4. Escribe `buen día profe` para iniciar

**Opción B — Slash command**
1. Dentro de tu proyecto crea la carpeta `.claude/commands/`
2. Copia `SKILL.md` como `.claude/commands/profe.md`
3. En Claude Code escribe `/profe` para activar el tutor

## Uso

En cualquier chat de Cowork o Claude Code:

| Comando | Qué hace |
|---------|----------|
| `buen día profe` | Inicia la sesión con tablero de progreso |
| `save` / `hasta mañana` | Guarda el progreso y cierra la sesión |
| `clear` | Retoma desde donde quedaste |
| `quiz` | Modo práctica estilo Skilljar |
| `glosario` | Explica cualquier término |

## Plataforma de cursos

anthropic.skilljar.com — cuenta gratuita requerida

---
*Programa CPN · Anthropic*
